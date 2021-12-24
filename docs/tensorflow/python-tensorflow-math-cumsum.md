# python–tensorlow . math . cusum()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-cum sum/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。 **cumsum()** 用于计算输入张量的累计和。

> **语法:** tensorflow.math.cumsum(x，轴，独占，反转，名称)
> 
> **参数:**
> 
> *   **x:** 是输入张量。此张量允许的数据类型是 float32、float64、int64、int32、uint8、uint16、int16、int8、complex64、complex128、qint8、quint8、qint32、half。
> *   **轴(可选):**是 int32 类型的张量。它的值应该在 int32 类型的张量范围内(默认值:0)。必须在[-rank(x)，rank(x)]范围内。默认值为 0。
> *   **独占(可选):**属于 bool 类型。默认值为假，如果设置为真，则输入[a，b，c]的输出将为[0，a，a+b]。
> *   **反转(可选):**是 bool 类型。默认值为 False，如果设置为 true，则输入[a，b，c]的输出将为[a+b+c，a+b，a]。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([1, 2, 4, 5], dtype = tf.int32) 

# Printing the input
print("Input: ",a)

# Cumulative sum
res  = tf.math.cumsum(a)

# Printing the result
print("Output: ",res)
```

**输出:**

```
Input:  tf.Tensor([1 2 4 5], shape=(4,), dtype=int32)
Output:  tf.Tensor([ 1  3  7 12], shape=(4,), dtype=int32)
```

**示例 2:** 在此示例中，反向和排他都设置为真。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([2, 3, 4, 5], dtype = tf.int32) 

# Printing the input
print("Input: ",a)

# Cumulative sum
res  = tf.math.cumsum(a, reverse = True, exclusive = True)

# Printing the result
print("Output: ",res)
```

**输出:**

```
Input:  tf.Tensor([2 3 4 5], shape=(4,), dtype=int32)
Output:  tf.Tensor([12  9  5  0], shape=(4,), dtype=int32)
```