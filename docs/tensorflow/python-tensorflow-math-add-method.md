# Python–Tensorflow math . add()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-add-method/](https://www.geeksforgeeks.org/python-tensorflow-math-add-method/)

Tensorflow math.add()方法返回传递输入的 a + b。运算是在 a 和 b 的表示上完成的，这种方法属于数学模块。

> **语法:** tf.math.add(a，b，name=None)
> **参数**
> 
> *   **a:** 这个参数应该是 Tensor，也可以是以下类型之一:bfloat16，half，float32，float64，uint8，int8，int16，int32，int64，complex64，complex128，string
>     
> *   **b:** 这也应该是张量，并且必须与 a 的类型相同。
>     
> *   **名称:**这是可选参数，这是操作的名称。
>     
> 
> **返回:**返回一个与输入 a 形状相同的张量

我们借助几个例子来看看这个概念:
**例 1:**

## 蟒蛇 3

```
# Importing the Tensorflow library
import tensorflow as tf

# A constant a and b
a = tf.constant(3)
b = tf.constant(6) 

# Applying the math.add() function
# storing the result in 'c'
c = tf.math.add(a, b)

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
Input 1 Tensor("Const_79:0", shape=(), dtype=int32)
3
Input 2 Tensor("Const_80:0", shape=(), dtype=int32)
6
Output:  Tensor("Add_1:0", shape=(), dtype=int32)
9
```

**例 2:**

## 蟒蛇 3

```
# Importing the Tensorflow library
import tensorflow as tf

# A constant a and b
a = tf.constant(u"This is ")
b = tf.constant(u"GeeksForGeeks") 

# Applying the math.add() function
# storing the result in 'c'
c = tf.math.add(a, b)

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
Input 1 Tensor("Const_87:0", shape=(), dtype=string)
b'This is '
Input 2 Tensor("Const_88:0", shape=(), dtype=string)
b'GeeksForGeeks'
Output:  Tensor("Add_5:0", shape=(), dtype=string)
b'This is GeeksForGeeks'
```