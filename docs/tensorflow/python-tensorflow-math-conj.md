# Python–tensorflow . math . conj()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-conj/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 Python 库。 **conj()** 用于求复输入张量的元复共轭。

> **语法:** tensorflow.math.conj( x，name)
> 
> **参数:**
> 
> *   **x:** 是张量，必须有数值。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 它返回与 x 相同数据类型的张量。
> 如果输入的不是数值张量，它将引发类型错误。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1+5j,3+2j,4+1j],dtype = tf.complex128)

# Printing the input tensor
print('a: ',a)

# Finding the complex conjugate
res = tf.math.conj(a)

# Printing the result
print('Complex Conjugate: ',res)
```

**输出:**

```py
a:  tf.Tensor([1.+5.j 3.+2.j 4.+1.j], shape=(3,), dtype=complex128)
Complex Conjugate:  tf.Tensor([1.-5.j 3.-2.j 4.-1.j], shape=(3,), dtype=complex128)

```

**示例 2:** 本示例使用带有 dtype float64 的输入。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3],dtype = tf.float64)

# Printing the input tensor
print('a: ',a)

# Finding the complex conjugate
res = tf.math.conj(a)

# Printing the result
print('Complex Conjugate: ',res)
```

**输出:**

```py
a:  tf.Tensor([1\. 2\. 3.], shape=(3,), dtype=float64)
Complex Conjugate:  tf.Tensor([1\. 2\. 3.], shape=(3,), dtype=float64)

```