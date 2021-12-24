# 毫升|使用 TensorFlow 2.0 的自动编码器

> 原文:[https://www . geesforgeks . org/ml-auto encoder-with-tensorflow-2-0/](https://www.geeksforgeeks.org/ml-autoencoder-with-tensorflow-2-0/)

本教程通过训练自动编码器，演示了如何在 TensorFlow 2.0 中使用图形模式执行生成手写数字图像。
自动编码器是用神经网络和/或[卷积神经网络](https://www.geeksforgeeks.org/introduction-convolution-neural-network/)实现的数据压缩和解压缩算法。数据被压缩到比初始输入更低维度的瓶颈。解压缩使用中间表示再次生成相同的输入图像。让我们使用 TensorFlow 2.0 编写一个好的自动编码器，默认情况下，TensorFlow 2.0 渴望理解该算法的机制。自动编码器被认为是更高级的创成式模型(如 GANs 和 CVAEs)的良好先决条件。
首先，根据可用硬件下载 TensorFlow 2.0。如果你正在使用谷歌可乐，请跟随这个 [IPython 笔记本](https://github.com/Vishal-V/GSoC/blob/master/autoencoder/notebook/autoencoder.ipynb)或这个[可乐演示](https://colab.research.google.com/drive/1aZ0mEFEui1A7FPWMylvjiVZ5XZIX7S9w)。确保为 GPU 安装提供了适当版本的 CUDA 和 CUDNN。访问 TensorFlow 页面[上的官方下载说明，点击此处](https://www.tensorflow.org/install)。
**代码:导入库**

## 蟒蛇 3

```py
# Install TensorFlow 2.0 by using the following command
# For CPU installation
# pip install -q tensorflow == 2.0
# For GPU installation (CUDA and CuDNN must be available)
# pip install -q tensorflow-gpu == 2.0

from __future__ import absolute_import
from __future__ import division
from __future__ import print_function

import tensorflow as tf
print(tf.__version__)
```

确认适当的 TF 下载后，导入其他依赖项进行数据扩充，并定义如下所示的自定义函数。标准缩放器通过转换列来缩放数据。当使用 ***tf 时，get_random_block_from_data 函数很有用。渐变带*** 执行自动渐变(自动微分)获得渐变。

## 蟒蛇 3

```py
import numpy as np
import sklearn.preprocessing as prep
import tensorflow.keras.layers as layers

def standard_scale(X_train, X_test):
    preprocessor = prep.StandardScaler().fit(X_train)
    X_train = preprocessor.transform(X_train)
    X_test = preprocessor.transform(X_test)
    return X_train, X_test

def get_random_block_from_data(data, batch_size):
    start_index = np.random.randint(0, len(data) - batch_size)
    return data[start_index:(start_index + batch_size)]
```

自动编码器可能具有有损中间表示，也称为压缩表示。这种降维在存在无损图像数据压缩的大量用例中是有用的。因此，我们可以说自动编码器的编码器部分对数据的密集表示进行编码。这里我们将使用 **TensorFlow 子类化 API** 为编码器和解码器定义自定义层。

## 蟒蛇 3

```py
class Encoder(tf.keras.layers.Layer):
    '''Encodes a digit from the MNIST dataset'''

    def __init__(self,
                n_dims,
                name ='encoder',
                **kwargs):
        super(Encoder, self).__init__(name = name, **kwargs)
        self.n_dims = n_dims
        self.n_layers = 1
        self.encode_layer = layers.Dense(n_dims, activation ='relu')

    @tf.function       
    def call(self, inputs):
        return self.encode_layer(inputs)

class Decoder(tf.keras.layers.Layer):
    '''Decodes a digit from the MNIST dataset'''

    def __init__(self,
                n_dims,
                name ='decoder',
                **kwargs):
        super(Decoder, self).__init__(name = name, **kwargs)
        self.n_dims = n_dims
        self.n_layers = len(n_dims)
        self.decode_middle = layers.Dense(n_dims[0], activation ='relu')
        self.recon_layer = layers.Dense(n_dims[1], activation ='sigmoid')

    @tf.function       
    def call(self, inputs):
        x = self.decode_middle(inputs)
        return self.recon_layer(x)
```

然后我们扩展 ***来定义一个自定义模型，该模型利用我们之前定义的自定义层来形成自动编码器模型。当数据可用于模型对象时，调用函数被覆盖，这是前向传递。请注意 ***@tf.function*** 函数装饰器。它确保函数的执行发生在一个图形中，这加快了我们的执行速度。*** 

## 蟒蛇 3

```py
class Autoencoder(tf.keras.Model):
    '''Vanilla Autoencoder for MNIST digits'''

    def __init__(self,
                 n_dims =[200, 392, 784],
                 name ='autoencoder',
                 **kwargs):
        super(Autoencoder, self).__init__(name = name, **kwargs)
        self.n_dims = n_dims
        self.encoder = Encoder(n_dims[0])
        self.decoder = Decoder([n_dims[1], n_dims[2]])

    @tf.function       
    def call(self, inputs):
        x = self.encoder(inputs)
        return self.decoder(x)
```

下面的代码块准备数据集，并在训练自动编码器之前准备好要输入函数预处理流水线的数据。

## 蟒蛇 3

```py
mnist = tf.keras.datasets.mnist

(X_train, _), (X_test, _) = mnist.load_data()
X_train = tf.cast(np.reshape(
        X_train, (X_train.shape[0],
                  X_train.shape[1] * X_train.shape[2])), tf.float64)
X_test = tf.cast(
        np.reshape(X_test,
                   (X_test.shape[0],
                    X_test.shape[1] * X_test.shape[2])), tf.float64)

X_train, X_test = standard_scale(X_train, X_test)
```

TensorFlow 的最佳实践是使用 ***tf.data.Dataset*** 从数据集快速获取混洗批次的张量切片进行训练。下面的代码块演示了 tf.data 的使用，并定义了用于训练 AutoEncoder 模型的超参数。

## 蟒蛇 3

```py
train_data = tf.data.Dataset.from_tensor_slices(
        X_train).batch(128).shuffle(buffer_size = 1024)
test_data = tf.data.Dataset.from_tensor_slices(
        X_test).batch(128).shuffle(buffer_size = 512)

n_samples = int(len(X_train) + len(X_test))
training_epochs = 20
batch_size = 128
display_step = 1

optimizer = tf.optimizers.Adam(learning_rate = 0.01)
mse_loss = tf.keras.losses.MeanSquaredError()
loss_metric = tf.keras.metrics.Mean()
```

我们已经完成了训练自动编码器模型的所有先决条件！我们剩下要做的就是定义一个 AutoEncoder 对象，并在调用 model 之前用优化器和 loss 编译模型。瞧啊。您可以看到损耗降低，自动编码器性能提高！

## 蟒蛇 3

```py
ae = Autoencoder([200, 392, 784])
ae.compile(optimizer = tf.optimizers.Adam(0.01),
           loss ='categorical_crossentropy')
ae.fit(X_train, X_train, batch_size = 64, epochs = 5)
```

你可以在这里查看 IPython 笔记本[，在这里](https://github.com/Vishal-V/GSoC/blob/master/autoencoder/notebook/autoencoder.ipynb)查看我提交给 TensorFlow [的 colab 演示。跟着我上](https://colab.research.google.com/drive/1aZ0mEFEui1A7FPWMylvjiVZ5XZIX7S9w) [GitHub](https://github.com/Vishal-V) 。