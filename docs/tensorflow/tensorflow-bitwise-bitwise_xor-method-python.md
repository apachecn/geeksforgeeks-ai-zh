# Tensorflow bitwise . bitwise _ xor()方法–Python

> 原文:[https://www . geesforgeks . org/tensorflow-bitwise-bitwise _ xor-method-python/](https://www.geeksforgeeks.org/tensorflow-bitwise-bitwise_xor-method-python/)

Tensorflow `bitwise.bitwise_xor()`方法执行 bitwise_xor 运算，结果将设置 a 和 b 中不同的那些位，运算是在 a 和 b 的表示上完成的，这个方法属于 bitwise module。

> **语法:** `tf.bitwise.bitwise_xor(a, b, name=None)`
> 
> **论据**
> 
> *   **a:** 这一定是张量。它应该来自以下类型之一:int8、int16、int32、int64、uint8、uint16、uint32、uint64。
> *   **b:** 这也应该是张量，类型和 a 一样
> *   **名称:**这是可选参数，这是操作的名称。
> 
> **Return:** 它返回一个与 a 和 b 类型相同的张量。

Let’s see this concept with the help of few examples:**Example 1:**

```
# Importing the Tensorflow library 
import tensorflow as tf 

# A constant a and b 
a = tf.constant(43, dtype = tf.int32) 
b = tf.constant(5, dtype = tf.int32) 

# Applying the bitwise_xor function 
# storing the result in 'c' 
c = tf.bitwise.bitwise_xor(a, b) 

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

```
Input 1 Tensor("Const_36:0", shape=(), dtype=int32)
43
Input 2 Tensor("Const_37:0", shape=(), dtype=int32)
5
Output:  Tensor("BitwiseXor_4:0", shape=(), dtype=int32)
46

```

**例 2:**

```
# Importing the Tensorflow library 
import tensorflow as tf 

# A constant vector of size 2 
a = tf.constant([10, 6], dtype = tf.int32) 
b = tf.constant([12, 5], dtype = tf.int32) 

# Applying the bitwise_xor function 
# storing the result in 'c' 
c = tf.bitwise.bitwise_xor(a, b) 

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

```
Input 1 Tensor("Const_34:0", shape=(2, ), dtype=int32)
[10  6]
Input 2 Tensor("Const_35:0", shape=(2, ), dtype=int32)
[12  5]
Output:  Tensor("BitwiseXor_3:0", shape=(2, ), dtype=int32)
[6 3]

```