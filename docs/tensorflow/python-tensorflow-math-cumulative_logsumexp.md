# Python–tensorflow . math . cumulative _ logsumexp()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-累计 _logsumexp/](https://www.geeksforgeeks.org/python-tensorflow-math-cumulative_logsumexp/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**累计 _logsumexp()** 用于计算输入张量的累计 log-sum-exp。这个操作相当于**张量流.数学.对数(张量流.数学. cumsum(张量流.数学. exp(x)))** 但是数值上更稳定。

> **语法:**tensorflow . math . cumulative _ logsumexp(x，轴，独占，反转，名称)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 float16，float32，float64。
> *   **轴(可选):**是 int32 类型的张量。它的值应该在 int32 类型的张量范围内(默认值:0)。必须在[-rank(x)，rank(x)]范围内。默认值为 0。
> *   **独占(可选):**属于 bool 类型。默认值为假。
> *   **反转(可选):**是 bool 类型。默认值为假。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 
> 它返回与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([1, 2, 4, 5], dtype = tf.float64) 

# Printing the input
print("Input: ",a)

# Cumulative log-sum-exp
res  = tf.math.cumulative_logsumexp(a)

# Printing the result
print("Output: ",res)
```

**输出:**

```
Input:  tf.Tensor([1\. 2\. 4\. 5.], shape=(4,), dtype=float64)
Output:  tf.Tensor([1\.         2.31326169 4.16984602 5.36184904], shape=(4,), dtype=float64)
```

**示例 2:** 在此示例中，反向和排他都设置为真。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([2, 3, 4, 5], dtype = tf.float64) 

# Printing the input
print("Input: ",a)

# Cumulative log-sum-exp
res  = tf.math.cumulative_logsumexp(a, reverse = True, exclusive = True)

# Printing the result
print("Output: ",res)
```

**输出:**

```
Input:  tf.Tensor([2\. 3\. 4\. 5.], shape=(4,), dtype=float64)
Output:  tf.Tensor([ 5.40760596e+000  5.31326169e+000  5.00000000e+000 -1.79769313e+308], shape=(4,), dtype=float64)
```