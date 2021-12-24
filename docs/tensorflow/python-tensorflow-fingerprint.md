# python–tensorlow . fingerprint()

> 原文:[https://www . geesforgeks . org/python-tensorflow-指纹/](https://www.geeksforgeeks.org/python-tensorflow-fingerprint/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**指纹()**用于生成指纹值。

> **语法:** tensorflow .指纹(数据、方法、名称)
> 
> **参数:**
> 
> *   **数据:**是秩为 1 或更高的张量。
> *   **方法:**定义生成指纹要用到的算法。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**它返回一个数据类型为 unit32 的二维张量。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([1, 2, 3, 4])
method = 'farmhash64'

# Printing the input
print('data: ', data)
print('method: ', method)

# Calculating result
res = tf.fingerprint(data, method)

# Printing the result
print('res: ', res)
```

**输出:**

```py
data:  tf.Tensor([1 2 3 4], shape=(4, ), dtype=int32)
method:  farmhash64
res:  tf.Tensor(
[[ 84  24  96  84 195  82 124 105]
 [ 15 219 106 105  88 163  17  93]
 [ 92   8   0 238 168 146  54  37]
 [178 113  27   7 149 125 165 247]], shape=(4, 8), dtype=uint8)

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2], [ 3, 4]])
method = 'farmhash64'

# Printing the input
print('data: ', data)
print('method: ', method)

# Calculating result
res = tf.fingerprint(data, method)

# Printing the result
print('res: ', res)
```

**输出:**

```py
data:  tf.Tensor(
[[1 2]
 [3 4]], shape=(2, 2), dtype=int32)
method:  farmhash64
res:  tf.Tensor(
[[ 76  18 253 133 168 204 240  10]
 [254 162  60 240 103 244  53 255]], shape=(2, 8), dtype=uint8)

```