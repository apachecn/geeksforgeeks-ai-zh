# Python–Tensorflow bitwise . invert()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-bitwise-invert-method/](https://www.geeksforgeeks.org/python-tensorflow-bitwise-invert-method/)

张量流`bitwise.invert()`方法执行反转操作，结果将反转位，如 0 到 1 和 1 到 0。运算是在 a.
的表示上完成的，这个方法属于按位模块。

> **语法:** `tf.bitwise.invert( a, name=None)`
> 
> **论据**
> 
> *   **a:** 这一定是张量。它应该来自以下类型之一:int8、int16、int32、int64、uint8、uint16、uint32、uint64。
> *   **名称:**这是可选参数，这是操作的名称。
> 
> **Return:** 它返回一个与 a 类型相同的张量

Let’s see this concept with the help of few examples:**Example 1:**

```py
import tensorflow as tf 

# A constant a 
a = tf.constant(6, dtype = tf.int32)  

# Applying the invert function 
# storing the result in 'c' 
c = tf.bitwise.invert(a) 

# Initiating a Tensorflow session 
with tf.Session() as sess:
    print("Input 1", a)
    print(sess.run(a))
    print("Output: ", c)
    print(sess.run(c))
```

**输出:**

```py
Input 1 Tensor("Const_40:0", shape=(), dtype=int32)
6
Output:  Tensor("Invert_4:0", shape=(), dtype=int32)
-7

```

**例 2:**

```py
import tensorflow as tf 

# A constant a 
a = tf.constant([1, 4, 7], dtype = tf.int32)  

# Applying the invert function 
# storing the result in 'c' 
c = tf.bitwise.invert(a) 

# Initiating a Tensorflow session 
with tf.Session() as sess:
    print("Input 1", a)
    print(sess.run(a))
    print("Output: ", c)
    print(sess.run(c))
```

**输出:**

```py
Input 1 Tensor("Const_39:0", shape=(3, ), dtype=int32)
[1 4 7]
Output:  Tensor("Invert_3:0", shape=(3, ), dtype=int32)
[-2 -5 -8]

```