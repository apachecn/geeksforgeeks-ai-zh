# Python–tensorflow . get _ logger()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-get _ logger/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**get_logger()** 用于获取 logger 实例。

> **语法:** tensorflow.get_logger()
> 
> **参数:**不接受任何参数。
> 
> **返回:**返回记录器实例。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Fetting logger instance 
logger = tf.get_logger()

# Checking if propagation is enabled
res = logger.propagate

# Printing the result
print('res: ',res)
```

**输出:**

```
res:  True

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Fetting logger instance 
logger = tf.get_logger()

# Disabling the propagation
logger.propagate = False

# Checking if propagation is enabled
res = logger.propagate

# Printing the result
print('res: ',res)
```

**输出:**

```
res:  False

```