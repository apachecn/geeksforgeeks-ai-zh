# ML |利用卷积神经网络的转移学习

> 原文:[https://www . geesforgeks . org/ml-传递-学习-带卷积-神经网络/](https://www.geeksforgeeks.org/ml-transfer-learning-with-convolutional-neural-networks/)

迁移学习作为一个通用术语，是指将从一项任务中学到的知识再用于另一项任务。特别是对于卷积神经网络(CNNs)，许多图像特征对于各种数据集是共同的(例如，几乎在每幅图像中都可以看到线、边缘)。正是因为这个原因，特别是对于大型结构，CNNs 很少完全从头开始训练，因为大数据集和繁重的计算资源很难获得。
常用的预处理数据集是 **ImageNet 数据集**，由 120 万张图像组成。实际使用的模型因任务而异(很多时候，人们只是选择在 ImageNet 挑战中表现最好的)，但本文中使用的 **ResNet50** 模型。预训练的模型通常可以通过正在使用的任何库找到，在这种情况下，就是 Keras。

**ResNet 简介**
ResNet 最初是作为一种解决消失梯度问题的方法而设计的。这是一个反向传播梯度变得非常小的问题，因为它们一次又一次地相乘，限制了神经网络的大小。ResNet 架构试图通过使用跳过连接来解决这个问题，即添加允许数据跳过层的快捷方式。

该模型包括一系列卷积层+跳跃连接，然后是平均池，然后是输出完全连接(密集)层。对于迁移学习，我们只希望卷积层包含我们感兴趣的特征，因此在导入模型时，我们希望省略它们。最后，因为我们要移除输出层，所以我们需要用我们自己的一系列层来替换它们。

**问题陈述**
为了展示迁移学习的过程，我将使用[加州理工学院-101 数据集](http://www.vision.caltech.edu/Image_Datasets/Caltech101/)，一个包含 101 个类别和每个类别大约 40-800 个图像的图像数据集。

**数据处理**

首先在这里下载并提取数据集[。确保提取后删除“背景 _ 谷歌”文件夹。](http://www.vision.caltech.edu/Image_Datasets/Caltech101/101_ObjectCategories.tar.gz)

**代码:**为了正确评估，我们还需要将数据拆分为训练集和测试集。这里，我们需要在每个类别中进行划分，以确保测试集中的适当表示。

```
TEST_SPLIT = 0.2
VALIDATION_SPLIT = 0.2

import os
import math

# stores test data
os.mkdir("caltech_test") 

for cat in os.listdir("101_ObjectCategories/"):
  # moves x portion of images per category into test images
  # new category folder
  os.mkdir("caltech_test/"+cat) 
  imgs = os.listdir("101_ObjectCategories/"+cat) 
  # all image filenames
  split = math.floor(len(imgs)*TEST_SPLIT) 
  test_imgs = imgs[:split]
  # move test portion
  for t_img in test_imgs: 
    os.rename("101_ObjectCategories/"+cat+"/"+t_img, 
              "caltech_test/"+cat+"/"+t_img)
```

**输出:**

```
This above code creates the file structure:

101_ObjectCategories/
-- accordion
-- airplanes
-- anchor
-- ...
caltech_test/
-- accordion
-- airplanes
-- anchor
-- ...

```

第一个文件夹包含列车图像，第二个包含测试图像。每个子文件夹都包含属于该类别的图像。为了输入数据，我们将使用 Keras 的 ImageDataGenerator 类。ImageDataGenerator 允许轻松处理图像数据，并具有增强选项。

```
# make sure to match original model's preprocessing function
from keras.applications.resnet50 import preprocess_input 
from keras.preprocessing.image import ImageDataGenerator

train_gen = ImageDataGenerator(
        validation_split = 0.2, 
        preprocessing_function = preprocess_input)
train_flow = train_gen.flow_from_directory("101_ObjectCategories/", 
                                           target_size =(256, 256), 
                                           batch_size = 32, 
                                           subset ="training")

valid_flow = train_gen.flow_from_directory("101_ObjectCategories/", 
                                           target_size =(256, 256), 
                                           batch_size = 32, 
                                           subset ="validation")

test_gen = ImageDataGenerator(
        preprocessing_function = preprocess_input)
test_flow = test_gen.flow_from_directory("caltech_test", 
                                         target_size =(256, 256), 
                                         batch_size = 32)
```

上面的代码采用了图像目录的文件路径，并为数据生成创建了一个对象。

**模型构建**
**代码:**添加基础预训练模型。

```
from keras.applications.resnet50 import ResNet50
from keras.layers import GlobalAveragePooling2D, Dense
from keras.layers import BatchNormalization, Dropout
from keras.models import Model

# by default, the loaded model will include the original CNN 
#classifier designed for the ImageNet dataset
# since we want to reuse this model for a different problem,
# we need to omit the original fully connected layers, and 
# replace them with our own setting include_top = False will
# load the model without the fully connected layer

# load resnet model, with pretrained imagenet weights.
res = ResNet50(weights ='imagenet', include_top = False, 
               input_shape =(256, 256, 3)) 
```

分割后，该数据集相对较小，约为 5628 幅图像，大多数类别只有 50 幅图像，因此微调卷积层可能会导致过度拟合。我们的新数据集与 ImageNet 数据集非常相似，因此我们可以确信许多预先训练的权重也具有正确的特征。因此，我们可以冻结那些经过训练的卷积层，这样当我们训练分类器的其余部分时，它们就不会改变。如果您有一个与原始数据集明显不同的较小数据集，微调可能仍会导致过度拟合，但后面的图层不会包含正确的要素。因此，您可以再次冻结卷积层，但只使用早期层的输出，因为这些层包含更一般的特征。对于大数据集，您不需要担心过度拟合，因此您可以经常微调整个网络。

```
from keras.applications.resnet50 import ResNet50
from keras.layers import GlobalAveragePooling2D, Dense
from keras.layers import BatchNormalization, Dropout
from keras.models import Model

# by default, the loaded model will include the original CNN 
#classifier designed for the ImageNet dataset
# since we want to reuse this model for a different problem,
# we need to omit the original fully connected layers, and 
# replace them with our own setting include_top = False will
# load the model without the fully connected layer

# load resnet model, with pretrained imagenet weights.
res = ResNet50(weights ='imagenet', include_top = False, 
               input_shape =(256, 256, 3)) 
```

现在，我们可以添加剩余的分类器。这将从预先训练的卷积层获得输出，并将其输入到单独的分类器中，该分类器在新的数据集上进行训练。

```
# get the output from the loaded model
x = res.output 

# avg. pools across the spatial dimensions (rows, columns) 
# until it becomes zero. Reshapes data into a 1D, allowing 
# for proper input shape into Dense layers 
# (e.g. (8, 8, 2048) -> (2048)).
x = GlobalAveragePooling2D()(x) 

# subtracts batch mean and divides by batch standard deviation
# to reduce shift in input distributions between layers. 
x = BatchNormalization()(x) 

# dropout allows layers to be less dependent on
# certain features, reducing overfitting
x = Dropout(0.5)(x) 
x = Dense(512, activation ='relu')(x)
x = BatchNormalization()(x)
x = Dropout(0.5)(x)

# output classification layer, we have 101 classes, 
# so we need 101 output neurons
x = Dense(101, activation ='softmax')(x) 

# create the model, setting input / output
model = Model(res.input, x) 

# compile the model - we're training using the Adam Optimizer
# and Categorical Cross Entropy as the loss function
model.compile(optimizer ='Adam', 
              loss ='categorical_crossentropy', 
              metrics =['accuracy']) 

# structure of our model
model.summary() 
```

**代码:**训练模型

```
model.fit_generator(train_flow, epochs = 5, validation_data = valid_flow)
```

 **输出:**

```
Epoch 1/5
176/176 [==============================] - 27s 156ms/step - loss: 1.6601 - acc: 0.6338 - val_loss: 0.3799 - val_acc: 0.8922
Epoch 2/5
176/176 [==============================] - 19s 107ms/step - loss: 0.4637 - acc: 0.8696 - val_loss: 0.2841 - val_acc: 0.9225
Epoch 3/5
176/176 [==============================] - 19s 107ms/step - loss: 0.2777 - acc: 0.9211 - val_loss: 0.2714 - val_acc: 0.9225
Epoch 4/5
176/176 [==============================] - 19s 107ms/step - loss: 0.2223 - acc: 0.9327 - val_loss: 0.2419 - val_acc: 0.9284
Epoch 5/5
176/176 [==============================] - 19s 106ms/step - loss: 0.1784 - acc: 0.9461 - val_loss: 0.2499 - val_acc: 0.9239

```

**代码:评估测试集**

```
result = model.evaluate(test_flow)

print('The model achieved a loss of %.2f and,'
      'accuracy of %.2f%%.' % (result[0], result[1]*100))
```

**输出:**

```
53/53 [==============================] - 5s 95ms/step
The model achieved a loss of 0.23 and accuracy of 92.80%.

```

对于 101 类数据集，我们仅用了 5 个时期就达到了 92.8%的准确率。对于透视，[原始 ResNet 在约 100 万个图像数据集上训练，用于 120 个时代。](https://github.com/tensorpack/tensorpack/issues/544)
有几件事可以改进。首先，查看上一个时期验证损失和训练损失之间的差异，您可以看到模型开始过度拟合。解决这个问题的一个方法是增加图像增强。使用[图像数据生成器类](https://keras.io/preprocessing/image/)，可以轻松实现简单的图像增强。您还可以尝试添加/移除图层或更改超参数，例如缺失或密集图层的大小。
用谷歌 Colab 的免费 GPU 计算资源在这里运行这段代码[。](https://colab.research.google.com/drive/12RmL0L_5LeK32VqPUFkoBJhMtpcoxEqt)