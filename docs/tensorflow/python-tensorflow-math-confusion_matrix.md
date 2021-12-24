# Python–tensorflow . math . muffusion _ matrix()

> 原文:[https://www . geeksforgeeks . org/python-tensorflow-math-mission _ matrix/](https://www.geeksforgeeks.org/python-tensorflow-math-confusion_matrix/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。**混淆 _ 矩阵()**用于从预测和标签中找到混淆矩阵。

> **语法:**tensorflow . math . muffusion _ matrix(标签、预测、num _ classes、权重、数据类型、名称)
> 
> **参数:**
> 
> *   **标签:**这是一个一维张量，包含分类任务的真实标签。
> *   **预测:**也是和标签形状一样的一维张量。它的值代表预测的类别。
> *   **num _ class(可选):**这是分类任务可能具有的标签/类的数量。如果没有提供，那么 num _ classes 将比预测或标签中的最大值多一个。
> *   **权重(可选):**这是一个与预测形状相同的张量，其值定义了每个预测的相应权重。
> *   **dtype(可选):**定义返回混淆矩阵的 dtype。如果是 tensor flow . dt types . int 32，则为默认值。
> *   **名称(可选):**定义操作的名称。
>     
> 
> **返回:**
> 它返回形状[n，n]的混淆矩阵，其中 n 是标签的可能数量。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
labels = tf.constant([1,3,4],dtype = tf.int32)
predictions = tf.constant([1,2,3],dtype = tf.int32)

# Printing the input tensor
print('labels: ',labels)
print('Predictions: ',predictions)

# Evaluating confusion matrix
res = tf.math.confusion_matrix(labels,predictions)

# Printing the result
print('Confusion_matrix: ',res)
```

**输出:**

```py
labels:  tf.Tensor([1 3 4], shape=(3,), dtype=int32)
Predictions:  tf.Tensor([1 2 3], shape=(3,), dtype=int32)
Confusion_matrix:  tf.Tensor(
[[0 0 0 0 0]
 [0 1 0 0 0]
 [0 0 0 0 0]
 [0 0 1 0 0]
 [0 0 0 1 0]], shape=(5, 5), dtype=int32)
```

**示例 2:** 本示例为所有预测提供权重。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
labels = tf.constant([1,3,4],dtype = tf.int32)
predictions = tf.constant([1,2,4],dtype = tf.int32)
weights = tf.constant([1,2,2], dtype = tf.int32)

# Printing the input tensor
print('labels: ',labels)
print('Predictions: ',predictions)
print('Weights: ',weights)

# Evaluating confusion matrix
res = tf.math.confusion_matrix(labels, predictions, weights=weights)

# Printing the result
print('Confusion_matrix: ',res)
```

**输出:**

```py
labels:  tf.Tensor([1 3 4], shape=(3,), dtype=int32)
Predictions:  tf.Tensor([1 2 4], shape=(3,), dtype=int32)
Weights:  tf.Tensor([1 2 2], shape=(3,), dtype=int32)
Confusion_matrix:  tf.Tensor(
[[0 0 0 0 0]
 [0 1 0 0 0]
 [0 0 0 0 0]
 [0 0 2 0 0]
 [0 0 0 0 2]], shape=(5, 5), dtype=int32)
```