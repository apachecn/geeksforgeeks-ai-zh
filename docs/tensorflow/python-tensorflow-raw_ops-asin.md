# python–tensorlow . raw _ ops。Asin()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-raw _ ops-asin/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。TensorFlow raw_ops 提供对所有 TensorFlow 操作的低级访问。 **Asin()** 用于求 x 的元素反正弦。

> **语法:** tf.raw_ops.Asin(x，name)
> 
> **论据:**
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
a = tf.constant([.2, .5, .7, 1], dtype=tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating inverse sine
res = tf.raw_ops.Asin(x=a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([0.2 0.5 0.7 1\. ], shape=(4,), dtype=float64)
Result:  tf.Tensor([0.20135792 0.52359878 0.7753975  1.57079633], shape=(4,), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([.2, .5, .7, 1], dtype=tf.float64)

# Calculating inverse sine
res = tf.raw_ops.Asin(x=a)

# Plotting the graph
plt.plot(a, res, color='green')
plt.title('tensorflow.raw_ops.Asin')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/48478466c941c61061a551e921df4bb4.png)