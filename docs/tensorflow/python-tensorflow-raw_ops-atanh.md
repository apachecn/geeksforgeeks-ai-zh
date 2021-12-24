# python–tensorlow . raw _ ops。Atanh()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-raw _ ops-atanh/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。TensorFlow raw_ops 提供对所有 TensorFlow 操作的低级访问。 **Atanh()** 用于求 x 的元素反双曲正切。

> **语法:** tf.raw_ops。阿坦(x，名字)
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

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([.1, .2, .3, .4, .5], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating inverse hyperbolic tangent
res = tf.raw_ops.Atanh(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([0.1 0.2 0.3 0.4 0.5], shape=(5, ), dtype=float64)
Result:  tf.Tensor([0.10033535 0.20273255 0.3095196  0.42364893 0.54930614], shape=(5, ), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([.1, .2, .3, .4, .5], dtype = tf.float64)

# Calculating inverse hyperbolic tangent
res = tf.raw_ops.Atanh(x = a)

# Plotting the graph
plt.plot(a, res, color ='green')
plt.title('tensorflow.raw_ops.Atanh')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/5566adf01079a6b41ff2027a237ea97c.png)