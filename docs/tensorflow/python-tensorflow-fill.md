# Python – tensorflow.fill（）

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-fill/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**fill()** 用于生成具有标量值的张量。

> **语法:** tensorflow.fill( dims，value，name)
> 
> **参数:**
> 
> *   **dims:** 它是 int32 或 int64 数据类型的一维序列，非负整数表示结果张量的形状。
> *   **值:**是需要填充的值。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回形状模糊的张量。
> 
> **加注:**
> 
> *   **InvalidArgumentError:** 当 dim 包含负值时，会引发此错误。
> *   **NotFoundError:** 当 dim 包含非整数值时，会引发此错误。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
dim = [4, 5]
value = 5

# Printing the input
print('dim: ', dim)
print('value: ', value)

# Calculating result
res = tf.fill(dim, value)

# Printing the result
print('res: ', res)
```

**输出:**

```

dim:  [4, 5]
value:  5
res:  tf.Tensor(
[[5 5 5 5 5]
 [5 5 5 5 5]
 [5 5 5 5 5]
 [5 5 5 5 5]], shape=(4, 5), dtype=int32)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
dim = [4, 2, 5]
value = 5

# Printing the input
print('dim: ', dim)
print('value: ', value)

# Calculating result
res = tf.fill(dim, value)

# Printing the result
print('res: ', res)
```

**输出:**

```

dim:  [4, 2, 5]
value:  5
res:  tf.Tensor(
[[[5 5 5 5 5]
  [5 5 5 5 5]]

 [[5 5 5 5 5]
  [5 5 5 5 5]]

 [[5 5 5 5 5]
  [5 5 5 5 5]]

 [[5 5 5 5 5]
  [5 5 5 5 5]]], shape=(4, 2, 5), dtype=int32)

```