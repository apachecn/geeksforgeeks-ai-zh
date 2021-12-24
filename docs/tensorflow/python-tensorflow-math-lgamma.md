# python–tensorlow . math . lgamma()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-lgamma/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**γ()**用于计算γ(x)绝对值的元素对数。

> **语法:**tensorlow . math . lgamma(x，name)
> 
> **参数:**
> 
> *   **x:** It is a tensor. Allowed dtypes are bfloat16, half, float32, float64.
>     
>     <
>     
>     
> *   **名称(可选):**定义操作的名称
> 
> **返回:**它将数据类型的张量返回为 x。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.lgamma(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([ 6.57925121  8.52516136 19.9872145  15.10441257], shape=(4, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```
# Importing the libraray
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([2, 8, 14, 5], dtype = tf.float32)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.lgamma(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 2\.  8\. 14\.  5.], shape=(4, ), dtype=float32)
Result:  tf.Tensor([ 0\.         8.525162  22.552166   3.1780539], shape=(4, ), dtype=float32)
```