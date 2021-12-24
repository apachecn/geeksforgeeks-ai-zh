# Python | tensorflow . math . arg min()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-arg min-method/](https://www.geeksforgeeks.org/python-tensorflow-math-argmin-method/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。argmin()是 tensorflow 数学模块中的一种方法。此方法用于找到轴上的最小值。

```py
Syntax:
tensorflow.math.argmin(
    input,axes,output_type,name
)

Arguments:
1\. input: It is a tensor. Allowed dtypes for this tensor are float32,
          float64, int32, uint8, int16, int8, complex64, int64, qint8, quint8,
          qint32, bfloat16, uint16, complex128, half, uint32, uint64\. 
2\. axes: It is also a vector. It describes the axes to reduce the tensor.
         Allowed dtype are int32 and int64\. Also [-rank(input),rank(input)) is the range allowed.
         axes=0 is used for vector.
3\. output_type: It defines the dtype in which returned result should be.
                Allowed values are int32, int64 and the default value is int64.
4\. name: It is an optional argument which defines name for the operation.

Return:
A tensor of output_type which contains the indices of the minimum value along the axes. 
```

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# initializing the constant tensor
a = tf.constant([5,10,5.6,7.9,1,50]) # 1 is the minimum value at index 4

# getting the minimum value index tensor
b = tf.math.argmin(input = a)

# printing the tensor
print('tensor: ',b)

# Evaluating the value of tensor
c = tf.keras.backend.eval(b)

#printing the value
print('value: ',c)
```

**输出:**

```py
tensor:  tf.Tensor(4, shape=(), dtype=int64)
value: 4
```

**例 2:**

这个例子使用了形状张量(3，3)。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# initializing the constant tensor
a = tf.constant(value = [9,8,7,3,5,4,6,2,1],shape = (3,3))

# printing the initialized tensor
print(a)

# getting the minimum value indices tensor
b = tf.math.argmin(input = a)

# printing the tensor
print('Indices Tensor: ',b)

# Evaluating the tensor value
c = tf.keras.backend.eval(b)

# printing the value
print('Indices: ',c)
```

**输出:**

```py
tf.Tensor(
[[9 8 7]
 [3 5 4]
 [6 2 1]], shape=(3, 3), dtype=int32)
 Indices tensor: tf.Tensor([1 2 2], shape=(3,), dtype=int64)
 Indices: [1 2 2]
```