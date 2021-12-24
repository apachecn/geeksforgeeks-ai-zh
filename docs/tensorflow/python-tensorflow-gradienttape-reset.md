# python–tensorlow。GradientTape.reset()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow 梯度胶带复位/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**复位()**用于清除磁带存储的所有信息。

> **语法:**重置()
> 
> **参数:**不接受任何参数。
> 
> **返回:**不返回。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

x = tf.constant(4.0)

# Using GradientTape
with tf.GradientTape() as gfg:
  gfg.watch(x)
  y = x * x * x
  y+=x*x

# Computing gradient without reset
res  = gfg.gradient(y, x) 

# Printing result
print("res(y = x*x*x + x*x): ",res)

# Using GradientTape
with tf.GradientTape() as gfg:
  gfg.watch(x)
  y = x * x * x

  # Resetting the Tape
  gfg.reset()

  gfg.watch(x)
  y+=x*x

# Computing gradient with reset
res  = gfg.gradient(y, x) 

# Printing result
print("res(y = x*x): ",res)
```

**输出:**

```

res(y = x*x*x + x*x):  tf.Tensor(56.0, shape=(), dtype=float32)
res(y = x*x):  tf.Tensor(8.0, shape=(), dtype=float32)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

x = tf.constant(3.0)

# Using GradientTape
with tf.GradientTape() as gfg:
  gfg.watch(x)
  y = x * x
  y+=x*x

# Computing gradient without reset
res  = gfg.gradient(y, x) 

# Printing result
print("res(y = x*x + x*x): ",res)

# Using GradientTape
with tf.GradientTape() as gfg:
  gfg.watch(x)
  y = x * x

  # Resetting the Tape
  gfg.reset()
  gfg.watch(x)
  y+=x

# Computing gradient with reset
res  = gfg.gradient(y, x) 

# Printing result
print("res(y = x): ",res)
```

**输出:**

```

res(y = x*x + x*x):  tf.Tensor(12.0, shape=(), dtype=float32)
res(y = x):  tf.Tensor(1.0, shape=(), dtype=float32)

```