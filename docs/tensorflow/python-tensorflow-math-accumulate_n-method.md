# Python–Tensorflow math . aggregate _ n()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-grade _ n-method/](https://www.geeksforgeeks.org/python-tensorflow-math-accumulate_n-method/)

张量流`math.accumulate_n()`方法执行传递的张量列表的元素求和。结果是执行操作后的张量。运算是在 a 和 b 的表示上完成的，这种方法属于数学模块。

> **语法:** `tf.math.accumulate_n( inputs, shape=None, tensor_dtype=None, name=None)` 
> 
> **论据**
> 
> *   **输入:**该参数取 Tensor 对象的列表，每个对象的形状和类型相同。
> *   **形状:**这是可选参数，它定义了输入元素的预期形状。
> *   **数据类型:**这是可选参数，它定义了输入的预期数据类型。
> *   **名称:**这是可选参数，这是操作的名称。
> 
> **Return:** 它返回一个与输入元素具有相同形状和类型的张量。

Let’s see this concept with the help of few examples:**Example 1:**

```py
# Importing the Tensorflow library 
import tensorflow as tf 

# A constant a and b
a = tf.constant([[1, 3], [6, 7]])
b = tf.constant([[5, 2], [3, 8]])  

# Applying the accumulate_n() function 
# storing the result in 'c' 
c = tf.math.accumulate_n([a, b, b])

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
Input 1 Tensor("Const_67:0", shape=(2, 2), dtype=int32)
[[1 3]
 [6 7]]
Input 2 Tensor("Const_68:0", shape=(2, 2), dtype=int32)
[[5 2]
 [3 8]]
Output:  Tensor("AccumulateNV2_2:0", shape=(2, 2), dtype=int32)
[[11  7]
 [12 23]]

```

**例 2:**

```py
# Importing the Tensorflow library 
import tensorflow as tf 

# A constant a and b
a = tf.constant([[2, 4], [1, 3]])
b = tf.constant([[5, 3], [4, 6]])  

# Applying the accumulate_n() function 
# storing the result in 'c' 
c = tf.math.accumulate_n([b, a, b], shape =[2, 2], tensor_dtype = tf.int32)

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
Input 1 Tensor("Const_73:0", shape=(2, 2), dtype=int32)
[[2 4]
 [1 3]]
Input 2 Tensor("Const_74:0", shape=(2, 2), dtype=int32)
[[5 3]
 [4 6]]
Output:  Tensor("AccumulateNV2_5:0", shape=(2, 2), dtype=int32)
[[12 10]
 [ 9 15]]

```