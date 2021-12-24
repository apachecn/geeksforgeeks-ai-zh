# python–tensorlow . index dslicesspec()

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slicespec/](https://www.geeksforgeeks.org/python-tensorflow-indexedslicesspec/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**索引策略类别**继承自类型类别，并为索引策略提供类型规范。

> **语法:**张量流。IndexedSlicesSpec(形状、数据类型、索引 _ 数据类型、密集 _ 形状 _ 数据类型、索引 _ 形状)
> 
> **参数:**
> 
> *   **形状(可选):**定义索引切片的密集形状。默认值为“无”，允许任何密集形状。
> *   **数据类型(可选):**定义 IndexedSlices 值的数据类型。默认值为 float32。
> *   **indexes _ dt type(可选):**定义 IndexedSlices 中索引的数据类型。它可以是 int32 或 int64，默认值为 int64。
> *   **dense_shape_dtye(可选):**定义 IndexedSlices 中密集形状的数据类型。它可以是 int32、int64 或 None，默认值为 None。
> *   **indexes _ shape(可选):**它定义了 indexes 组件的形状，表示 IndexedSlices 中有多少切片。

**示例 1:** 本示例使用所有默认值。

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Calculating result
res = tf.IndexedSlicesSpec()

# Printing the result
print('IndexedSlicesSpec: ', res)
```

**输出:**

```
IndexedSlicesSpec:  IndexedSlicesSpec(TensorShape(None), tf.float32, tf.int64, None, TensorShape([None]))
```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Calculating result
res = tf.IndexedSlicesSpec((2, 3))

# Printing the result
print('IndexedSlicesSpec: ', res)
```

**输出:**

```
IndexedSlicesSpec:  IndexedSlicesSpec(TensorShape([2, 3]), tf.float32, tf.int64, None, TensorShape([None]))
```