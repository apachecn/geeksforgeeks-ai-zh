# Python–Tensorflow bitwise . bitwise _ and()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-bitwise-bitwise _ and-method/](https://www.geeksforgeeks.org/python-tensorflow-bitwise-bitwise_and-method/)

Tensorflow `bitwise.bitwise_and()`方法执行按位“与”运算，并返回在 a 和 b 中都设置为(1)的那些位集合。该运算是在 a 和 b 的表示上完成的。
该方法属于按位模块。

> **语法:** `tf.bitwise.bitwise_and( a, b, name=None)`
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
a = tf.constant(4, dtype = tf.int32)
b = tf.constant(6, dtype = tf.int32)  

# Applying the bitwise_and() function 
# storing the result in 'c' 
c = tf.bitwise.bitwise_and(a, b) 

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
Input 1 Tensor("Const_41:0", shape=(), dtype=int32)
4
Input 2 Tensor("Const_42:0", shape=(), dtype=int32)
6
Output:  Tensor("BitwiseAnd_5:0", shape=(), dtype=int32)
4

```

**例 2:**

```py
# Importing the Tensorflow library 
import tensorflow as tf 

# A constant a and b
a = tf.constant([1, 2, 7], dtype = tf.int32)
b = tf.constant([1, 5, 8], dtype = tf.int32)  

# Applying the bitwise_and() function 
# storing the result in 'c' 
c = tf.bitwise.bitwise_and(a, b) 

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
Input 1 Tensor("Const_43:0", shape=(3, ), dtype=int32)
[1 2 7]
Input 2 Tensor("Const_44:0", shape=(3, ), dtype=int32)
[1 5 8]
Output:  Tensor("BitwiseAnd_6:0", shape=(3, ), dtype=int32)
[1 0 0]

```