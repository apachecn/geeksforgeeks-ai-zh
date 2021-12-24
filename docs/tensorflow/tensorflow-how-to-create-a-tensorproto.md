# 张量流–如何创建张量原型

> 原文:[https://www . geesforgeks . org/tensorflow-如何创建-a-tensorproto/](https://www.geeksforgeeks.org/tensorflow-how-to-create-a-tensorproto/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

TensorProto 主要用于生成 numpy 数组。

> **使用的功能:**
> 
> *   **make_tensor_proto:** 这个函数接受需要和其他可选参数一起放入 TensorProto 的值。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing Input
value = tf.constant([1, 15], dtype = tf.float64)

# Printing the Input
print("Value: ", value)

# Getting TensorProto
res = tf.make_tensor_proto(value)

# Printing the resulting tensor
print("Result: ", res)
```

**输出:**

```

Value:  tf.Tensor([ 1\. 15.], shape=(2, ), dtype=float64)
Result:  dtype: DT_DOUBLE
tensor_shape {
  dim {
    size: 2
  }
}
tensor_content: "\000\000\000\000\000\000\360?\000\000\000\000\000\000.@"

```

**示例 2:** 本示例使用 python 数组生成 TensorProto。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing Input
value = [1, 2, 3, 4]

# Printing the Input
print("Value: ", value)

# Getting TensorProto
res = tf.make_tensor_proto(value)

# Printing the resulting tensor
print("Result: ", res)
```

**输出:**

```

Value:  [1, 2, 3, 4]
Result:  dtype: DT_INT32
tensor_shape {
  dim {
    size: 4
  }
}
tensor_content: "\001\000\000\000\002\000\000\000\003\000\000\000\004\000\000\000"

```