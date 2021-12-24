# python–tensorlow . math . soft plus()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-soft plus/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**softplus()** 用于计算元素方向日志(exp(特征)+ 1)。

> **语法:** tensorflow.math.softplus(功能、名称)
> 
> **参数:**
> 
> *   **特征:**是张量。允许的数据类型有 half、bfloat16、float32 和 float64。
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
res = tf.math.softplus(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 5\.  7\.  9\. 15.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([ 5.00671535  7.00091147  9.0001234  15.00000031], shape=(4, ), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf
import matplotlib.pyplot as plt

# Initializing the input tensor
a = tf.constant([ 5, 7, 9, 15], dtype = tf.float64)

# Calculating tangent
res = tf.math.softplus(a)

# Plotting the graph
plt.plot(a, res, color ='green')
plt.title('tensorflow.math.softplus')
plt.xlabel('Input')
plt.ylabel('Result')
plt.show()
```

**输出:**

![](img/8ffb2fa2cb1eb5a3d08a84aea38b162c.png)