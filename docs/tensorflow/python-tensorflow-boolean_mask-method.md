# Python–tensorflow . boolean _ mask()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-boolean _ mask-method/](https://www.geeksforgeeks.org/python-tensorflow-boolean_mask-method/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。**布尔 _ 遮罩()**是用于将布尔遮罩应用于张量的方法。

> **语法:** tensorflow.boolean_mask(张量、掩码、轴、名称)
> 
> **参数:**
> 
> *   **张量:**是 N 维输入张量。
> *   **mask:** 是 k 维的布尔张量，其中 k < =N，k 是静态已知的。
> *   **轴:**它是一个 0 维张量，表示应该应用遮罩的轴。轴的默认值为零，k+轴< =N。
> *   **名称:**定义操作名称的可选参数。
> 
> **Return:** 它返回(N-K+1)维张量，其值与掩码中的真值相匹配。

**示例 1:** 在本示例中，输入为一维

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the inputs
tensor = [1,2,3]
mask = [False, True, True]

# printing the input
print('Tensor: ',tensor)
print('Mask: ',mask)

# applying the mask
result = tf.boolean_mask(tensor, mask)

# printing the result
print('Result: ',result)
```

**输出:**

```
Tensor:  [1, 2, 3]
Mask:  [False, True, True]
Result:  tf.Tensor([2 3], shape=(2,), dtype=int32)
```

**示例 2:** 在该示例中，采用二维输入。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the inputs
tensor = [[1, 2], [10, 14], [9, 7]]
mask = [False, True, True]

# printing the input
print('Tensor: ',tensor)
print('Mask: ',mask)

# applying the mask
result = tf.boolean_mask(tensor, mask)

# printing the result
print('Result: ',result)
```

**输出:**

```
Tensor:  [[1, 2], [10, 14], [9, 7]]
Mask:  [False, True, True]
Result:  tf.Tensor(
[[10 14]
 [ 9  7]], shape=(2, 2), dtype=int32)
```