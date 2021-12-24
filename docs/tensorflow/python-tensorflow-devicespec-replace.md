# Python–张量流。设备规格更换()

> 原文:[https://www . geesforgeks . org/python-tensorflow-device spec-replace/](https://www.geeksforgeeks.org/python-tensorflow-devicespec-replace/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**replace()** 用于覆盖 DeviceSpec 对象的规格，得到新的对象。

> **语法:**张量流。DeviceSpec.replace(**kwargs)
> 
> **参数:**
> 
> *   ****kwargs:** 此方法接受 DeviceSpec 构造函数接受的所有参数。
> 
> **返回:**返回一个 DeviceSpec 对象。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", replica = 5)

# Printing the DeviceSpec 
print('Device Spec: ', device_spec.to_string())

# Getting new DeviceSpec object
new_device_spec = device_spec.replace(job = "gfg2")

# Printing the result
print('New Device Spec: ', new_device_spec.to_string())
```

**输出:**

```py

Device Spec:  /job:gfg/replica:5
New Device Spec:  /job:gfg2/replica:5

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", replica = 5)

# Printing the DeviceSpec 
print('Device Spec: ', device_spec.to_string())

# Getting new DeviceSpec object
new_device_spec = device_spec.replace(job = "gfg2", device_type = "CPU")

# Printing the result
print('New Device Spec: ', new_device_spec.to_string())
```

**输出:**

```py

Device Spec:  /job:gfg/replica:5
New Device Spec:  /job:gfg2/replica:5/device:CPU:*

```