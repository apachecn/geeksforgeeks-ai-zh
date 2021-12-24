# Python–张量流。设备规格任务属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-device spec-task-attribute/](https://www.geeksforgeeks.org/python-tensorflow-devicespec-task-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**任务**用于获取 DeviceSpec 的任务索引。

> **语法:**张量流。DeviceSpec.task
> 
> **返回:**返回 DeviceSpec 的任务索引

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg2", replica = 5, device_type ="GPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting task index
task = device_spec.task

# Printing the result
print('Task Index: ', task)
```

**输出:**

```py
Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba981d08>
Task Index:  None

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg2", replica = 5, task = 2, device_type ="GPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting task index
task = device_spec.task

# Printing the result
print('Task Index: ', task)
```

**输出:**

```py
Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba91a708>
Task Index:  2

```