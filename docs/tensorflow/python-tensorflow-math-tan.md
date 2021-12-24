# Python–tensorflow . math . tan()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-tan/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。
**tan()** 用来求 x 的素切线。

> **语法:** tf.math.tan(x，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 bfloat16，half，float32，float64。
> *   **名称(可选):**定义操作的名称。
>     
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

# Calculating tangent
res = tf.math.tan(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([ 1.55740772 -2.18503986 -0.14254654  1.15782128 -3.38051501], shape=(5, ), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype = tf.float64)

# Calculating tangent
res = tf.math.tan(x = a)

# Plotting the graph
plt.plot(a, res, color ='green')
plt.title('tensorflow.math.tan')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/2b066406c1f1b30637b142c9a9ef3d8f.png)