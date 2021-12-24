# Python | Tensorflow logic _ not()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-logic _ not-method/](https://www.geeksforgeeks.org/python-tensorflow-logical_not-method/)

[Tensorflow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌开发的开源机器学习库。其应用之一是开发深度神经网络。

模块`**tensorflow.math**`为许多基本逻辑操作提供支持。功能`tf.logical_not()`【别名`tf.math.logical_not`或`tf.Tensor.__invert__`】支持 Tensorflow 中的*逻辑非*功能。它需要布尔类型的输入。输入类型是张量，如果输入包含一个以上的元素，则计算元素逻辑非，![ $ NOT x $ ](img/5559dd31e6d0343ed9e911c51cc3e081.png "Rendered by QuickLaTeX.com")。

> **语法**:TF . logic _ not(x，name=None)或 TF . math . logic _ not(x，name=None)或 tf.Tensor.__invert__(x，name=None)
> 
> **参数** :
> **x** :布尔型张量。
> **名称**(可选):操作的名称。
> 
> **返回型**:与 x 大小相同的布尔型张量。

**代码:**

```py
# Importing the Tensorflow library
import tensorflow as tf

# A constant vector of size 4
a = tf.constant([True, False, False, True], dtype = tf.bool)

# Applying the NOT function and
# storing the result in 'b'
b = tf.logical_not(a, name ='logical_not')

# Initiating a Tensorflow session
with tf.Session() as sess:
    print('Input type:', a)
    print('Input a:', sess.run(a))
    print('Return type:', b)
    print('Output:', sess.run(b))
```

**输出:**

```py
Input type: Tensor("Const:0", shape=(4, ), dtype=bool)
Input: [ True False False True]
Return type: Tensor("logical_and:0", shape=(4, ), dtype=bool)
Output: [ False True True False]

```