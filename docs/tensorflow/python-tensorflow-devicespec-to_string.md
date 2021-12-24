# Python–张量流。DeviceSpec.to_string()

> 原文:[https://www . geesforgeks . org/python-tensorflow-device spec-to _ string/](https://www.geeksforgeeks.org/python-tensorflow-devicespec-to_string/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**to_string()** 用于获取 DeviceSpec 对象规范的字符串表示。

> **语法:**张量流。DeviceSpec.to_string()
> 
> **返回:**返回一个字符串。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", replica = 5)

# Printing the DeviceSpec 
print('Device Spec: ', device_spec.to_string())
```

**输出:**

```

Device Spec:  /job:gfg/replica:5

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", replica = 5, device_type = "CPU")

# Printing the DeviceSpec 
print('Device Spec: ', device_spec.to_string())
```

**输出:**

```

Device Spec:  /job:gfg/replica:5/device:CPU:*

```