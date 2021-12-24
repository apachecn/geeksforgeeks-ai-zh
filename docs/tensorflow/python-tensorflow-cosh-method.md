# Python | Tensorflow cosh()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-cosh-method/](https://www.geeksforgeeks.org/python-tensorflow-cosh-method/)

[Tensorflow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌开发的开源机器学习库。其应用之一是开发深度神经网络。
模块 **tensorflow.math** 为许多基本的数学运算提供支持。函数 TF . cosh()[别名 tf.math.cosh]为 Tensorflow 中的*双曲余弦*函数提供支持。它需要弧度形式的输入。输入类型是张量，如果输入包含一个以上的元素，则按元素计算双曲余弦。

> **语法** : tf.cosh(x，name=None)或 tf.math.cosh(x，name=None)
> **参数** :
> **x** :以下任一类型的张量:float16、float32、float64、complex64 或 complex128。
> **名称**(可选):操作的名称。
> **返回类型**:与 x 类型相同的张量。

**代码#1:**

## 蟒蛇 3

```py
# Importing the Tensorflow library
import tensorflow as tf

# A constant vector of size 6
a = tf.constant([1.0, -0.5, 3.4, -2.1, 0.0, -6.5],
                               dtype = tf.float32)

# Applying the cosh function and
# storing the result in 'b'
b = tf.cosh(a, name ='cosh')

# Initiating a Tensorflow session
with tf.Session() as sess:
    print('Input type:', a)
    print('Input:', sess.run(a))
    print('Return type:', b)
    print('Output:', sess.run(b))
```

**输出:**

```py
Input type: Tensor("Const_2:0", shape=(6, ), dtype=float32)
Input: [ 1\.  -0.5  3.4 -2.1  0\.  -6.5]
Return type: Tensor("cosh_1:0", shape=(6, ), dtype=float32)
Output: [  1.5430806   1.127626   14.998738    4.144313    1\.        332.5716   ]
```

**代码#2:** 可视化

## 蟒蛇 3

```py
# Importing the Tensorflow library
import tensorflow as tf

# Importing the NumPy library
import numpy as np

# Importing the matplotlib.pyplot function
import matplotlib.pyplot as plt

# A vector of size 15 with values from -1 to 1
a = np.linspace(-1, 1, 15)

# Applying the hyperbolic cosine function and
# storing the result in 'b'
b = tf.cosh(a, name ='cosh')

# Initiating a Tensorflow session
with tf.Session() as sess:
    print('Input:', a)
    print('Output:', sess.run(b))
    plt.plot(a, sess.run(b), color = 'red', marker = "o")
    plt.title("tensorflow.cosh")
    plt.xlabel("X")
    plt.ylabel("Y")

    plt.show()
```

**输出:**

```py
Input: [-1\.         -0.85714286 -0.71428571 -0.57142857 -0.42857143 -0.28571429
 -0.14285714  0\.          0.14285714  0.28571429  0.42857143  0.57142857
  0.71428571  0.85714286  1\.        ]
Output: [1.54308063 1.39039564 1.26613436 1.16775654 1.09325103 1.04109475
 1.01022145 1\.         1.01022145 1.04109475 1.09325103 1.16775654
 1.26613436 1.39039564 1.54308063]
```

![](img/3b59fe23b4e28cec932c8999197428d2.png)