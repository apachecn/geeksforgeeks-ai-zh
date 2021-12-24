# python–tensorlow . math . sqrt()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-sqrt/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**sqrt()** 用于计算元素方向的平方根。

> **语法:**tensorlow . math . sqrt(x，name)
> 
> **参数:**
> 
> *   **x:** 是张量。允许的数据类型有 bfloat16、half、float32、float64、complex64、complex128。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ 5, 7, 9, 15], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.sqrt(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 5\.  7\.  9\. 15.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([2.23606798 2.64575131 3\.         3.87298335], shape=(4, ), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```
# import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([ 5, 7, 9, 15], dtype = tf.float64)

# Calculating tangent
res = tf.math.sqrt(a)

# Plotting the graph
plt.plot(a, res, color ='green')
plt.title('tensorflow.math.sqrt')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/e7cb1d0bc8aec6d72840b891ad057fc4.png)