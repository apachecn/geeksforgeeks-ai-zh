# python–tensorlow . math . erfc()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-erfc/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 Python 库。

**erfc()** 用于计算单元式互补高斯误差函数。

> **语法:**tensorlow . math . erfc(x，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。允许的数据类型有 bfloat16、half、float32、float64。
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

# Calculating complementary Gauss error
res = tf.math.erfc(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
Input:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5, ), dtype=float64)
Result:  tf.Tensor(
[1.57299207e-01 4.67773498e-03 2.20904970e-05 1.54172579e-08
 1.53745979e-12], shape=(5, ), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype = tf.float64)

# Calculating complementary Gauss error
res = tf.math.erfc(x = a)

# Plotting the graph
plt.plot(a, res, color ='green')
plt.title('tensorflow.math.erfc')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/9e9066848c9e89bbc285ff389da33eaa.png)