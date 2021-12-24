# python–tensorlow . raw _ ops。Asinh()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-raw _ ops-asinh/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。TensorFlow raw_ops 提供对所有 TensorFlow 操作的低级访问。 **Asinh()** 用于求 x 的元素反双曲正弦。

> **语法:** tf.raw_ops。Asinh(x，名称)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 bfloat16，half，float32，float64。
> *   **名称(可选):**定义操作的名称。
>     
> 
> **返回:**返回与 x 相同数据类型的张量。

**注意:**只接受关键字参数。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype=tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating inverse hyperbolic sine
res = tf.raw_ops.Asinh(x=a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
Input:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5,), dtype=float64)
Result:  tf.Tensor([0.88137359 1.44363548 1.81844646 2.09471255 2.31243834], shape=(5,), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype=tf.float64)

# Calculating inverse hyperbolic sine
res = tf.raw_ops.Asinh(x=a)

# Plotting the graph
plt.plot(a, res, color='green')
plt.title('tensorflow.raw_ops.Asinh')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/df228acbc077cc046e215bfdc08ffc49.png)