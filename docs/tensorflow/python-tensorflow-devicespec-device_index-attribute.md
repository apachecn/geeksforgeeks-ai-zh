# Python–张量流。设备规格设备索引属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-device spec-device _ index-attribute/](https://www.geeksforgeeks.org/python-tensorflow-devicespec-device_index-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**device_index** 用于获取 DeviceSpec 的设备索引。

> **语法:**张量流。设备规格.设备 _ 索引
> 
> **返回:**返回设备索引。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", device_type ="CPU", device_index = 0)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting device index
device_index = device_spec.device_index

# Printing the result
print('Device Index: ', device_index)
```

**输出:**

```py

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba96aee8>
Device Index:  0

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", device_type ="CPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting device index
device_index = device_spec.device_index

# Printing the result
print('Device Index: ', device_index)
```

**输出:**

```py

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba97f048>
Device Index:  1

```