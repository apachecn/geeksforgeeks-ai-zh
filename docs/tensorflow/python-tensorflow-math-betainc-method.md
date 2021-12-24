# Python–tensorflow . math . beta Inc()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-beta Inc-method/](https://www.geeksforgeeks.org/python-tensorflow-math-betainc-method/)

TensorFlow 是谷歌设计的开源 python 库，用于开发机器学习模型和深度学习神经网络。**βInc()**是张量流数学模块中用于计算正则化不完全β积分的方法 **I <sub>x</sub> (a，b)** 。

> **正则化** **不完全贝塔积分 Ix(a，b)定义为:**
> 
> Ix(a，b)= b(x)；a，b)/B(a，b)
> 
> **在哪里，**
> 
> b(x；a，b)是不完全β函数，定义为:
> 
> b(x；(a)、(b) = ？<sup>x</sup>【dt】
> 
> 而 B(a，B)是完全β函数。

> **语法:** tensorflow.math.betainc( a，b，x，name)
> 
> **参数:**
> 
> *   **a:** 是张量。允许的类型有 float32 和 float64。
> *   **b:** 是一个与 a 类型相同的张量。
> *   **x:** 也是一个与 a 类型相同的张量
> *   **名称:**定义操作名称的可选参数。
>     
> 
> **Return:** 返回一个与 a.
> 类型相同的张量

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the constant tensors
a = tf.constant([1,2,3,4,5], dtype = tf.float64)
b = tf.constant([1.5,2.7,3.4,4.9,5.6], dtype = tf.float64)
x = tf.constant( [1,1,1,1,1], dtype = tf.float64)

# printing the input tensors
print('Input a: ',a)
print('Input b: ',b)
print('Input x: ',x)

# calculating the regularized incomplete beta integral 
ribi = tf.math.betainc(a,b,x)

# printing the result
print('regularized incomplete beta integral: ',ribi)
```

**输出:**

```
Input a:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5,), dtype=float64)
Input b:  tf.Tensor([1.5 2.7 3.4 4.9 5.6], shape=(5,), dtype=float64)
Input x:  tf.Tensor([1\. 1\. 1\. 1\. 1.], shape=(5,), dtype=float64)
regularized incomplete beta integral:  tf.Tensor([1\. 1\. 1\. 1\. 1.], shape=(5,), dtype=float64)

```

**例子 2:** 这个例子试图用不允许的数据类型张量来评估正则化的不完全β积分。这将引发 NotFoundError。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the constant tensors
a = tf.constant([1,2,3,4,5], dtype = tf.complex128)
b = tf.constant([1.5,2.7,3.4,4.9,5.6], dtype = tf.complex128)
x = tf.constant( [1,1,1,1,1], dtype = tf.complex128)

# printing the input tensors
print('Input a: ',a)
print('Input b: ',b)
print('Input x: ',x)

# calculating the regularized incomplete beta integral 
ribi = tf.math.betainc(a,b,x)
```

**输出:**

```
Input a:  tf.Tensor([1.+0.j 2.+0.j 3.+0.j 4.+0.j 5.+0.j], shape=(5,), dtype=complex128)
Input b:  tf.Tensor([1.5+0.j 2.7+0.j 3.4+0.j 4.9+0.j 5.6+0.j], shape=(5,), dtype=complex128)
Input x:  tf.Tensor([1.+0.j 1.+0.j 1.+0.j 1.+0.j 1.+0.j], shape=(5,), dtype=complex128)

NotFoundError                             Traceback (most recent call last)

<ipython-input-16-904ce11d62af> in <module>()
      1 # calculating the regularized incomplete beta integral
----> 2 ribi = tf.math.betainc(a,b,x)

2 frames

/usr/local/lib/python3.6/dist-packages/six.py in raise_from(value, from_value)

NotFoundError: Could not find valid device for node.
Node:{{node Betainc}}
All kernels registered for op Betainc :
  device='XLA_CPU_JIT'; T in [DT_FLOAT, DT_DOUBLE]
  device='XLA_GPU_JIT'; T in [DT_FLOAT, DT_DOUBLE]
  device='XLA_CPU'; T in [DT_FLOAT, DT_DOUBLE]
  device='XLA_GPU'; T in [DT_FLOAT, DT_DOUBLE]
  device='GPU'; T in [DT_DOUBLE]
  device='GPU'; T in [DT_FLOAT]
  device='CPU'; T in [DT_DOUBLE]
  device='CPU'; T in [DT_FLOAT]

```