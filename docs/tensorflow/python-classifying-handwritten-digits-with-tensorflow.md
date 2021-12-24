# Python |用张量流分类手写数字

> 原文:[https://www . geesforgeks . org/python-分类-手写-数字-with-tensorflow/](https://www.geeksforgeeks.org/python-classifying-handwritten-digits-with-tensorflow/)

对手写数字进行分类是机器学习的基本问题，可以通过多种方式来解决这里我们将通过使用 TensorFlow
**使用具有 tf.contrib.learn**
的线性分类器算法来实现它们。线性分类器通过基于特征的线性组合(也称为特征值)的值进行选择来实现手写数字的分类，并且通常以称为特征向量的向量呈现给机器。
**所需模块:**
[NumPy](https://www.geeksforgeeks.org/python-numpy/) :

```py
$ pip install numpy 
```

[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/) :

```py
$ pip install matplotlib 
```

[张量流](https://www.geeksforgeeks.org/introduction-to-tensorflow/) ：

```py
$ pip install tensorflow 
```

## **后续步骤**

**第一步:**导入所有依赖

## 蟒蛇 3

```py
import numpy as np
import matplotlib.pyplot as plt
import tensorflow as tf

learn = tf.contrib.learn

tf.logging.set_verbosity(tf.logging.ERROR)
```

**步骤 2 :** 使用 MNIST 数据
导入数据集

## 蟒蛇 3

```py
mnist = learn.datasets.load_dataset('mnist')
data = mnist.train.images
labels = np.asarray(mnist.train.labels, dtype=np.int32)
test_data = mnist.test.images
test_labels = np.asarray(mnist.test.labels, dtype=np.int32)
```

在此步骤之后，将下载 mnist 数据集。
**输出:**

```py
Extracting MNIST-data/train-images-idx3-ubyte.gz
Extracting MNIST-data/train-labels-idx1-ubyte.gz
Extracting MNIST-data/t10k-images-idx3-ubyte.gz
Extracting MNIST-data/t10k-labels-idx1-ubyte.gz
```

**第三步:**制作数据集

## 蟒蛇 3

```py
max_examples = 10000
data = data[:max_examples]
labels = labels[:max_examples]
```