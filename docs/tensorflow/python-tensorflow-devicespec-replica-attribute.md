# Python–张量流。设备规格副本属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-device spec-replica-attribute/](https://www.geeksforgeeks.org/python-tensorflow-devicespec-replica-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**副本**用于获取 DeviceSpec 的副本索引。

> **语法:**张量流。DeviceSpec.replica
> 
> **返回:**返回设备规格的副本索引。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg2", device_type ="GPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting replica index
replica = device_spec.replica

# Printing the result
print('Replica: ', replica)
```

**输出:**

```py

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba981b88>
Replica:  None

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg2", replica = 5, device_type ="GPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting replica index
replica = device_spec.replica

# Printing the result
print('Replica: ', replica)
```

**输出:**

```py

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba981d08>
Replica:  5

```