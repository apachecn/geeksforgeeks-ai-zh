# Python–张量流。device spec . make _ merged _ spec()

> 原文:[https://www . geesforgeks . org/python-tensorflow-device spec-make _ merged _ spec/](https://www.geeksforgeeks.org/python-tensorflow-devicespec-make_merged_spec/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**make_merged_spec** 用于合并两个 DeviceSpec 的规格。

> **语法:**张量流。device spec . make _ merged _ spec(dev)
> 
> **参数:**
> 
> *   **dev:** 是 DeviceSpec。
> 
> **返回:**返回合并规格的设备规格对象。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", replica = 5)
device_spec2 = tf.DeviceSpec(device_type ="CPU")

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)
print('Device Spec2: ', device_spec2)

# Getting new DeviceSpec object
new_device_spec = device_spec.make_merged_spec(device_spec2)

# Printing the result
print('New Device Spec: ', new_device_spec)
```

**输出:**

```

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fad779e4d08>
Device Spec2:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fadb9428228>
New Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fad779e4ca8>

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", replica = 5)
device_spec2 = tf.DeviceSpec(device_type ="CPU", device_index = 2)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)
print('Device Spec2: ', device_spec2)

# Getting new DeviceSpec object
new_device_spec = device_spec.make_merged_spec(device_spec2)

# Printing the result
print('New Device Spec: ', new_device_spec)
```

**输出:**

```

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fad779e4e28>
Device Spec2:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fad779e4d08>
New Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fadb9428228>

```