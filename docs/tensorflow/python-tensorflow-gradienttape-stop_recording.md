# Python–张量流。gradienttape . stop _ recording()

> 原文:[https://www . geesforgeks . org/python-tensorflow-gradienttape-stop _ recording/](https://www.geeksforgeeks.org/python-tensorflow-gradienttape-stop_recording/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**stop_recording()** 用于暂时停止记录操作。如果磁带没有录制，将会出现错误。

> **语法:**张量流。GradientTape.stop_recording()
> 
> **参数:**不接受任何参数。
> 
> **返回:**无
> 
> **加注:**
> 
> *   **运行时间错误:**如果磁带没有正确记录，它将引发运行时间错误。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

x = tf.constant(4.0)

# Using GradientTape
with tf.GradientTape() as gfg:
  gfg.watch(x)

  # Stop recording
  with gfg.stop_recording():
    y = x * x * x

# Computing gradient
res = gfg.gradient(y, x) 

# Printing result
print("res: ", res)
```

**输出:**

```

res:  None

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

x = tf.constant(4.0)

# Using GradientTape
with tf.GradientTape() as gfg:
  gfg.watch(x)

  # Stop recording
  with gfg.stop_recording():
    y = x * x * x

  # Starting the recording again
  gfg.watch(x)
  y = x * x

# Computing gradient
res = gfg.gradient(y, x) 

# Printing result
print("res: ", res)
```

**输出:**

```

res:  tf.Tensor(8.0, shape=(), dtype=float32)

```