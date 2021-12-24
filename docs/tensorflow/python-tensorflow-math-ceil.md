# Python–tensorflow . math . ceil()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-ceil/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。 **ceil()** 用于查找输入的元素式 ceil 值。

> **语法:** tensorflow.math.ceil( x，name)
> 
> **参数:**
> 
> *   **x:** 它是一个张量，这个张量允许的数据类型是 bfloat16，half，float32，float64。国际 32 号。
> *   **名称:**这是一个可选参数，用于定义操作的名称。
>     
> 
> **返回:**
> 它返回一个与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([1.5, 2.7, 3.9, 1.2, 1.8], dtype = tf.float64)

# printing the input
print('a: ',a)

# Finding the ceil value
r = tf.math.ceil(a)

# printing the result
print("Result: ",r)
```

**输出:**

```
a:  tf.Tensor([1.5 2.7 3.9 1.2 1.8], shape=(5,), dtype=float64)
Result:  tf.Tensor([2\. 3\. 4\. 2\. 2.], shape=(5,), dtype=float64)
```

**示例 2:** 在该示例中，使用二维张量。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([[1.5, 2.7], [3.9, 1.2]], dtype = tf.float64)

# printing the input
print('a: ',a)

# Finding the ceil value
r = tf.math.ceil(a)

# printing the result
print('Result: ',r)
```

**输出:**

```
a:  tf.Tensor(
[[1.5 2.7]
 [3.9 1.2]], shape=(2, 2), dtype=float64)
Result:  tf.Tensor(
[[2\. 3.]
 [4\. 2.]], shape=(2, 2), dtype=float64)
```

**示例 3:** 在此示例中，使用了无效的数据类型张量。它将引发 NotFoundError。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([1.5, 2.7, 3.9, 1.2, 1.8], dtype = tf.complex128)

# printing the input
print('a: ',a)

# Finding the ceil value
r = tf.math.ceil(a)
```

**输出:**

```
a:  tf.Tensor([1.5+0.j 2.7+0.j 3.9+0.j 1.2+0.j 1.8+0.j], shape=(5,), dtype=complex128)

---------------------------------------------------------------------------

NotFoundError                             Traceback (most recent call last)

<ipython-input-49-e349e3adf9c3> in <module>()
      6 
      7 # Finding the ceil value
----> 8 r = tf.math.ceil(a)

4 frames

/usr/local/lib/python3.6/dist-packages/six.py in raise_from(value, from_value)

NotFoundError: Could not find valid device for node.
Node:{{node Ceil}}
All kernels registered for op Ceil :
  device='XLA_GPU'; T in [DT_FLOAT, DT_DOUBLE, DT_BFLOAT16, DT_HALF]
  device='XLA_CPU'; T in [DT_FLOAT, DT_DOUBLE, DT_BFLOAT16, DT_HALF]
  device='XLA_CPU_JIT'; T in [DT_FLOAT, DT_DOUBLE, DT_BFLOAT16, DT_HALF]
  device='XLA_GPU_JIT'; T in [DT_FLOAT, DT_DOUBLE, DT_BFLOAT16, DT_HALF]
  device='GPU'; T in [DT_DOUBLE]
  device='GPU'; T in [DT_HALF]
  device='GPU'; T in [DT_FLOAT]
  device='CPU'; T in [DT_DOUBLE]
  device='CPU'; T in [DT_HALF]
  device='CPU'; T in [DT_FLOAT]
 [Op:Ceil]
```