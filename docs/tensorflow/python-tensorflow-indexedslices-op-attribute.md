# Python–张量流。索引策略操作属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slices-op-attribute/](https://www.geeksforgeeks.org/python-tensorflow-indexedslices-op-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**op** 用于查找产生输出值的操作。它只在紧急执行被禁用时起作用。

> **语法:**张量流。IndexedSlices.op
> 
> **返回:**返回产生输出值的运算。

**示例 1:** 在此示例中，禁用了紧急执行。

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Disable Eager execution
tf.compat.v1.disable_eager_execution()

# Initializing the input
data = tf.constant([[1, 2, 3], [4, 5, 6]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0], 1)

# Finding operation
op = res.op

# Printing the result
print('Operation: ', op)
```

**输出:**

```py

data:  Tensor("Const:0", shape=(2, 3), dtype=int32)
Operation:  name: "Const"
op: "Const"
attr {
  key: "dtype"
  value {
    type: DT_INT32
  }
}
attr {
  key: "value"
  value {
    tensor {
      dtype: DT_INT32
      tensor_shape {
        dim {
          size: 2
        }
        dim {
          size: 3
        }
      }
      tensor_content: "\001\000\000\000\002\000\000\000\003\000\000\000\004\000\000\000\005\000\000\000\006\000\000\000"
    }
  }
}

```

**示例 2:** 在此示例中，启用了紧急执行，因此它将引发属性错误。

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [4, 5, 6]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0], 1)

# Finding operation
op = res.op

# Printing the result
print('Operation: ', op)
```

**输出:**

```py

data:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)

---------------------------------------------------------------------------

AttributeError                            Traceback (most recent call last)

<ipython-input-1-8dd32836815c> in <module>()
     12 
     13 # Finding operation
---> 14 op = res.op
     15 
     16 # Printing the result

1 frames

/usr/local/lib/python3.6/dist-packages/tensorflow/python/framework/ops.py in op(self)
   1111   def op(self):
   1112     raise AttributeError(
-> 1113         "Tensor.op is meaningless when eager execution is enabled.")
   1114 
   1115   @property

AttributeError: Tensor.op is meaningless when eager execution is enabled.

```