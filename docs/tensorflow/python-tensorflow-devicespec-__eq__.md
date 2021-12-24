# python–tensorlow . devicespec . _ _ _ eq _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-devicespec-_ _ _ eq _/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**__eq__()** 用于检查两个 DeviceSpec 对象的相等性。

> **语法:**tensorflow . device spec . _ _ eq _ _(其他)
> 
> **参数:**
> 
> *   **其他:**是 DeviceSpec 对象。
> 
> **返回:**如果设备规格对象规格相同，则返回真，否则返回假。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg2", replica = 5, task = 2, device_type ="GPU", device_index = 1)
device_spec2 = tf.DeviceSpec(job ="gfg2", replica = 5, task = 2, device_type ="GPU", device_index = 1)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec.to_string())
print('Device Spec2: ', device_spec2.to_string())

# Finding the result
res = device_spec.__eq__(device_spec2)

# Printing the result
print('Res: ', res)
```

**输出:**

```

Device Spec:  /job:gfg2/replica:5/task:2/device:GPU:1
Device Spec2:  /job:gfg2/replica:5/task:2/device:GPU:1
Res:  True

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing Device Specification
device_spec = tf.DeviceSpec(job ="gfg2", replica = 5, task = 2, device_type ="GPU", device_index = 1)
device_spec2 = tf.DeviceSpec(job ="gfg2", replica = 5, task = 2, device_type ="CPU", device_index = 2)

# Printing the DeviceSpec object
print('Device Spec: ', device_spec.to_string())
print('Device Spec2: ', device_spec2.to_string())

# Finding the result
res = device_spec.__eq__(device_spec2)

# Printing the result
print('Res: ', res)
```

**输出:**

```

Device Spec:  /job:gfg2/replica:5/task:2/device:GPU:1
Device Spec2:  /job:gfg2/replica:5/task:2/device:CPU:2
Res:  False

```