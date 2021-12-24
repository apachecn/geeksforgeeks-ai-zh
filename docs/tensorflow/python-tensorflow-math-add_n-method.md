# Python–Tensorflow math . add _ n()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-add _ n-method/](https://www.geeksforgeeks.org/python-tensorflow-math-add_n-method/)

张量流`math.add_n()`方法逐元素添加所有传递的张量。对 a 和 b 的表示进行运算。
该方法属于数学模块。

> **语法:** `tf.math.add_n(inputs, name=None)`
> 
> **论据**
> 
> *   **输入:**指定 tf 的列表。张量或 tf。IndexedSlices 对象，每个对象的形状和类型必须相同。tf。在应用方法之前，IndexedSlices 对象会自动转换为密集张量。
> *   **名称:**这是可选参数，这是操作的名称。
> 
> **Return:** 它返回一个与传递的输入元素具有相同形状和类型的张量。

**注意:**该方法执行与 TF . math . aggregate _ n 相同的操作，但是该方法在开始求和之前等待输入准备就绪。因此，当输入可能没有同时准备好时，这种缓冲会导致更多的内存消耗。

Let’s see this concept with the help of few examples:**Example 1:**

```
# Importing the Tensorflow library 
import tensorflow as tf 

# A constant a and b
a = tf.constant([[1, 3], [2, 8]])
b = tf.constant([[2, 1], [6, 7]])  

# Applying the math.add_n() function 
# storing the result in 'c' 
c = tf.math.add_n([a, b])

# Initiating a Tensorflow session 
with tf.Session() as sess:
    print("Input 1", a)
    print(sess.run(a))
    print("Input 2", b)
    print(sess.run(b))
    print("Output: ", c)
```

**输出:**

```
Input 1 Tensor("Const_99:0", shape=(2, 2), dtype=int32)
[[1 3]
 [2 8]]
Input 2 Tensor("Const_100:0", shape=(2, 2), dtype=int32)
[[2 1]
 [6 7]]
Output:  Tensor("AddN:0", shape=(2, 2), dtype=int32)
[[ 3  4]
 [ 8 15]]

```

**例 2:**

```
# Importing the Tensorflow library 
import tensorflow as tf 

# A constant a and b
a = tf.constant([[1, 1], [2, 6]])
b = tf.constant([[5, 1], [8, 7]])  

# Applying the math.add_n() function 
# storing the result in 'c' 
c = tf.math.add_n([a, b], name = "Add_N")

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
Input 1 Tensor("Const_101:0", shape=(2, 2), dtype=int32)
[[1 1]
 [2 6]]
Input 2 Tensor("Const_102:0", shape=(2, 2), dtype=int32)
[[5 1]
 [8 7]]
Output:  Tensor("Add_N:0", shape=(2, 2), dtype=int32)
[[ 6  2]
 [10 13]]

```