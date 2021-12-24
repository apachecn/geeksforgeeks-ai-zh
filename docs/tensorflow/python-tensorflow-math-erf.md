# Python–tensorflow . math . ERF()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-ERF/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 Python 库。

**erf()** 用于计算单元式高斯误差函数。

> **语法:** tensorflow.math.erf( x，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。允许的数据类型有 bfloat16、half、float32、float64。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating Gauss error
res = tf.math.erf(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([0.84270079 0.99532227 0.99997791 0.99999998 1\.        ], shape=(5, ), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype = tf.float64)

# Calculating Gauss error
res = tf.math.erf(x = a)

# Plotting the graph
plt.plot(a, res, color ='green')
plt.title('tensorflow.math.erf')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/26bfd1de038a9cf3e11719e868825ecf.png)