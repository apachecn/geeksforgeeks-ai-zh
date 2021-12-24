# Python – tensorflow.device（）

> 原文:[https://www.geeksforgeeks.org/python-tensorflow-device/](https://www.geeksforgeeks.org/python-tensorflow-device/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**device()** 用于明确指定应该在其中执行操作的设备。

> **语法:**tensorflow . device(device _ name)
> 
> **参数:**
> 
> *   **设备名称:**指定在此上下文中使用的设备名称。
> 
> **返回:**它返回一个上下文管理器，指定用于新创建的 ops 的默认设备。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="localhost", replica = 0, device_type = "CPU")

# Printing the DeviceSpec
print('Device Spec: ', device_spec.to_string())

# Enabling device logging
tf.debugging.set_log_device_placement(True)

# Specifying the device
with tf.device(device_spec):
  a = tf.constant([[1.0, 2.0, 3.0], [4.0, 5.0, 6.0]])
  b = tf.constant([[1.0, 2.0], [3.0, 4.0], [5.0, 6.0]])
  c = tf.matmul(a, b)
```

**输出:**

```
Device Spec:  /job:localhost/replica:0/device:CPU:*
Executing op MatMul in device /job:localhost/replica:0/task:0/device:CPU:0
```

**示例 2:** 在此示例中，设备规范指定了要使用的 GPU，但系统找不到 GPU，因此它将在 CPU 上运行操作。

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="localhost", replica = 0, device_type = "GPU")

# Printing the DeviceSpec
print('Device Spec: ', device_spec.to_string())

# Enabling device logging
tf.debugging.set_log_device_placement(True)

# Specifying the device
with tf.device(device_spec):
  a = tf.constant([[1.0, 2.0, 3.0], [4.0, 5.0, 6.0]])
  b = tf.constant([[1.0, 2.0], [3.0, 4.0], [5.0, 6.0]])
  c = tf.matmul(a, b)
```

**输出:**

```
Device Spec:  /job:localhost/replica:0/device:GPU:*
Executing op MatMul in device /job:localhost/replica:0/task:0/device:CPU:0
```