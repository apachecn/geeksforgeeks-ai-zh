# Python–tensorflow . math . sign()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-sign/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**符号()**用于寻找数字符号的元素方向指示。具体来说，

y =符号(x) = -1 如果 x < 0; 0 if x == 0; 1 if x >为 0。

对于复数，y =符号(x) = x / |x| if x！= 0，否则 y = 0。

> **语法** : tensorflow.math.sign(x，name)
> 
> **参数:**
> 
> *   **x:** 是张量。允许的数据类型有 bfloat16、half、float32、float64、int32、int64、complex64、complex128。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**它返回一个与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([0, 1, -2, 3, -4], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.sign(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 0\.  1\. -2\.  3\. -4.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([ 0\.  1\. -1\.  1\. -1.], shape=(5, ), dtype=float64)
```

**例 2:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ 1-5j, -2 + 3j, -3-7j, -4 + 8j], dtype = tf.complex128)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.sign(x = a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 1.-5.j -2.+3.j -3.-7.j -4.+8.j], shape=(4, ), dtype=complex128)
Result:  tf.Tensor(
[ 0.19611614-0.98058068j -0.5547002 +0.83205029j -0.3939193 -0.91914503j
 -0.4472136 +0.89442719j], shape=(4, ), dtype=complex128)
```