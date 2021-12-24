# Python–tensorflow . math . log1p()

> 原文:[https://www.geeksforgeeks.org/python-tensorflow-math-log1p/](https://www.geeksforgeeks.org/python-tensorflow-math-log1p/)

TensorFlow 是谷歌设计的开源 python 库，用于开发机器学习模型和深度学习神经网络。TensorFlow raw_ops 提供对所有 TensorFlow 操作的低级访问。 **Log1p()** 用于求输入 x 的(1+x)的元素方向对数。

> **语法:** tf.math.log1p(x，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 bfloat16，half，float32，float64，complex64，complex128。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating logarithm(1 + x)
res = tf.math.log1p(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([0.69314718 1.09861229 1.38629436 1.60943791 1.79175947], shape=(5, ), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype = tf.float64)

# Calculating logarithm(1 + x)
res = tf.math.log1p(x = a)

# Plotting the graph
plt.plot(a, res, color ='green')
plt.title('tensorflow.math.log1p')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/ea94dd04c7911d65b1d49eda886d38d6.png)