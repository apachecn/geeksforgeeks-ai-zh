# python–tensorlow . math . acosh()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-acosh/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。
**acosh()** 用于寻找 x 的元素态双曲 acos。

> **语法:** tf.math.acosh(x，name)
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

```py
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ 1, 2, 3, 4, 5], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating tangent
res = tf.math.acosh(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
Input:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([0\.         1.3169579  1.76274717 2.06343707 2.29243167], shape=(5, ), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```py
# Importing the libraray
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype = tf.float64)

# Calculating tangent
res = tf.math.acosh(x = a)

# Plotting the graph
plt.plot(a, res, color ='green')
plt.title('tensorflow.math.acosh')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/b76f2afa97da4b073e783849d9166606.png)