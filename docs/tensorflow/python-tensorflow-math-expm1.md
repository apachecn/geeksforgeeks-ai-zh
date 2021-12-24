# python–tensorlow . math . expm 1()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-expm 1/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 Python 库。

**expm1()** 用于计算元素方向 exp(x)-1。

> **语法:**tensorlow . math . expm 1(x，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。允许的数据类型有 bfloat16、half、float32、float64、complex64、complex128。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.expm1(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
Input:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([  1.71828183   6.3890561   19.08553692  53.59815003 147.4131591 ], shape=(5, ), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype = tf.float64)

# Calculating result
res = tf.math.expm1(x = a)

# Plotting the graph
plt.plot(a, res, color ='green')
plt.title('tensorflow.math.expm1')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/81222df91abbee6648156f4c1000a380.png)