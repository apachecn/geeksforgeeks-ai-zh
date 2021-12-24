# Python–张量流。设备规格作业属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-device spec-job-attribute/](https://www.geeksforgeeks.org/python-tensorflow-devicespec-job-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**作业**用于从设备规格中获取作业。

> **语法:**张量流。DeviceSpec .作业
> 
> **返回:**返回设备规格的作业。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg", device_type ="GPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting the job
job = device_spec.job

# Printing the result
print('Job: ', job)
```

**输出:**

```

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba9810a8>
Job:  gfg

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg2", device_type ="GPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec)

# Getting the job
job = device_spec.job

# Printing the result
print('Job: ', job)
```

**输出:**

```

Device Spec:  <tensorflow.python.framework.device_spec.DeviceSpecV2 object at 0x7fe5ba981108>
Job:  gfg2

```