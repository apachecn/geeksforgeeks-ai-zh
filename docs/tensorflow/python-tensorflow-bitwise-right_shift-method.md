# Python–Tensorflow bitwise . right _ shift()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-bitwise-right _ shift-method/](https://www.geeksforgeeks.org/python-tensorflow-bitwise-right_shift-method/)

Tensorflow `bitwise.right_shift()`方法对由输入 b 定义的输入 a 执行 right_shift 操作，并返回新的常数。操作是在 a 和 b 的表示上完成的。
这个方法属于按位模块。

> **语法:** `tf.bitwise.right_shift( a, b, name=None)`
> 
> **论据**
> 
> *   **a:** 这一定是张量。它应该来自以下类型之一:int8、int16、int32、int64、uint8、uint16、uint32、uint64。
> *   **b:** 这也应该是张量，类型和 a 一样
> *   **名称:**这是可选参数，这是操作的名称。
> 
> **Return:** 它返回一个与 a 和 b 类型相同的张量。

Let’s see this concept with the help of few examples:**Example 1:**

```py
# Importing the Tensorflow library 
import tensorflow as tf 

# A constant a and b
a = tf.constant(256, dtype = tf.int32)
b = tf.constant(1, dtype = tf.int32)  

# Applying the right_shift() function 
# storing the result in 'c' 
c = tf.bitwise.right_shift(a, b) 

# Initiating a Tensorflow session 
with tf.Session() as sess:
    print("Input 1", a)
    print(sess.run(a))
    print("Input 2", b)
    print(sess.run(b))
    print("Output: ", c)
    print(sess.run(c))
```

**输出:**

```py
Input 1 Tensor("Const_57:0", shape=(), dtype=int32)
256
Input 2 Tensor("Const_58:0", shape=(), dtype=int32)
1
Output:  Tensor("RightShift_3:0", shape=(), dtype=int32)
128

```

**例 2:**

```py
# Importing the Tensorflow library 
import tensorflow as tf 

# A constant a and b
a = tf.constant([8, 16, 32], dtype = tf.int32)
b = tf.constant([2, 2, 3], dtype = tf.int32)  

# Applying the right_shift() function 
# storing the result in 'c' 
c = tf.bitwise.right_shift(a, b) 

# Initiating a Tensorflow session 
with tf.Session() as sess:
    print("Input 1", a)
    print(sess.run(a))
    print("Input 2", b)
    print(sess.run(b))
    print("Output: ", c)
    print(sess.run(c))
```

**输出:**

```py
Input 1 Tensor("Const_53:0", shape=(3, ), dtype=int32)
[ 8 16 32]
Input 2 Tensor("Const_54:0", shape=(3, ), dtype=int32)
[2 2 3]
Output:  Tensor("RightShift_1:0", shape=(3, ), dtype=int32)
[2 4 4]

```