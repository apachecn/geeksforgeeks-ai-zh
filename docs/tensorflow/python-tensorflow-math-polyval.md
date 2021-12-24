# python–tensorlow . math . poly val()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-poly val/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**polyval()** 用于计算多项式的元素方向值。

> **语法:**tensorlow . math . poly val(coffs，x，name)
> 
> **参数:**
> 
> *   **系数:**它是表示多项式系数的列表张量。
> *   **x:** 它是表示多项式变量的张量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回张量。

如果系数是一个有 n 个值的张量，x 是一个张量，那么 P(x)是 n 次多项式，定义为:

```py
p(x) = coeffs[n-1] + coeffs[n-2] * x + ... + coeffs[0] * x**(n-1)
```

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
coeffs = [-1, 2, 3]
x = tf.constant([7], dtype = tf.int32)

# Printing the input tensor
print('coeffs: ', coeffs)
print('x: ', x)

# Calculating Result
res = tf.math.polyval(coeffs, x)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
coeffs:  [-1, 2, 3]
x:  tf.Tensor([7], shape=(1, ), dtype=int32)
Result:  tf.Tensor([-32], shape=(1, ), dtype=int32)

```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
coeffs = [-1, 2, 3]
x = tf.constant([7, 2], dtype = tf.int32)

# Printing the input tensor
print('coeffs: ', coeffs)
print('x: ', x)

# Calculating Result
res = tf.math.polyval(coeffs, x)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
coeffs:  [-1, 2, 3]
x:  tf.Tensor([7 2], shape=(2, ), dtype=int32)
Result:  tf.Tensor([-32   3], shape=(2, ), dtype=int32)
```