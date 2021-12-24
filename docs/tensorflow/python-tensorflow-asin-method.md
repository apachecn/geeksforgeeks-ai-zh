# Python | Tensorflow asin()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-asin 方法/

[Tensorflow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌开发的开源机器学习库。其应用之一是开发深度神经网络。
模块 **tensorflow.math** 为许多基本的数学运算提供支持。函数 TF . asin()[别名 tf.math.asin]为 Tensorflow 中的*逆正弦*函数提供支持。它期望输入在[-1，1]范围内，并以弧度形式给出输出。如果输入不在范围[-1，1]内，则返回 *nan* 。输入类型是张量，如果输入包含一个以上的元素，则计算元素反正弦。

> **语法** : tf.asin(x，name=None)或 tf.math.asin(x，name=None)
> **参数** :
> **x** :以下任一类型的张量:bfloat16、half、float32、float64、int32、int64、complex64 或 complex128。
> **名称**(可选):操作的名称。
> **返回类型**:与 x 类型相同的张量。

**代码#1:**

## 蟒蛇 3

```
# Importing the Tensorflow library
import tensorflow as tf

# A constant vector of size 6
a = tf.constant([1.0, -0.5, 3.4, 0.2, 0.0, -2],
                            dtype = tf.float32)

# Applying the asin function and
# storing the result in 'b'
b = tf.asin(a, name ='asin')

# Initiating a Tensorflow session
with tf.Session() as sess:
    print('Input type:', a)
    print('Input:', sess.run(a))
    print('Return type:', b)
    print('Output:', sess.run(b))
```

**输出:**

```
Input type: Tensor("Const_6:0", shape=(6, ), dtype=float32)
Input: [ 1\.  -0.5  3.4  0.2  0\.  -2\. ]
Return type: Tensor("asin_2:0", shape=(6, ), dtype=float32)
Output: [ 1.5707964  -0.5235988          nan  0.20135793  0\.                 nan]
```

**代码#2:** 可视化

## 蟒蛇 3

```
# Importing the Tensorflow library
import tensorflow as tf

# Importing the NumPy library
import numpy as np

# Importing the matplotlib.pyplot function
import matplotlib.pyplot as plt

# A vector of size 15 with values from -1 to 1
a = np.linspace(-1, 1, 15)

# Applying the inverse sine function and
# storing the result in 'b'
b = tf.asin(a, name ='asin')

# Initiating a Tensorflow session
with tf.Session() as sess:
    print('Input:', a)
    print('Output:', sess.run(b))
    plt.plot(a, sess.run(b), color = 'red', marker = "o")
    plt.title("tensorflow.asin")
    plt.xlabel("X")
    plt.ylabel("Y")

    plt.show()
```

**输出:**

```
Input: [-1\.         -0.85714286 -0.71428571 -0.57142857 -0.42857143 -0.28571429
 -0.14285714  0\.          0.14285714  0.28571429  0.42857143  0.57142857
  0.71428571  0.85714286  1\.        ]
Output: [-1.57079633 -1.0296968  -0.79560295 -0.60824558 -0.44291104 -0.2897517
 -0.14334757  0\.          0.14334757  0.2897517   0.44291104  0.60824558
  0.79560295  1.0296968   1.57079633]
```

![](img/c09704690022910c2d03c90b0d7ed046.png)