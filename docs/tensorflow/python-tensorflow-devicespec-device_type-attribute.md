# Python–张量流。设备规格设备类型属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-device spec-device _ type-attribute/](https://www.geeksforgeeks.org/python-tensorflow-devicespec-device_type-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**设备类型**用于获取设备规格的设备类型。

> **语法:**张量流。设备规格设备类型
> 
> **返回:**返回设备类型。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", device_type ="CPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting device type
device_type = device_spec.device_type

# Printing the result
print('Device Type: ', device_type)
```

**输出:**

```

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba96af48>
Device Type:  CPU

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", device_type ="GPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting device type
device_type = device_spec.device_type

# Printing the result
print('Device Type: ', device_type)
```

**输出:**

```

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba96aee8>
Device Type:  GPU

```