# python–tensorlow。梯度胶带()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-gradienttape/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**GradientTape()** 用于记录自动微分的操作。

> **语法:**张量流。GradientTape(持久，watch _ accessed _ variables)
> 
> **参数:**
> 
> *   **持久(可选):**可以是真，也可以是假，默认值为假。它定义是否创建持久渐变带。
> *   **watch _ access _ variables:**它是一个布尔值，定义了磁带是否会自动观察磁带活动时访问的任何(可训练的)变量。

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

# Computing gradient
res  = gfg.gradient(y, x)

# Printing result
print("res: ",res)
```

**输出:**

```
res:  tf.Tensor(48.0, shape=(), dtype=float32)

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

  # Using nested GradientTape for calculating higher order derivative
  with tf.GradientTape() as gg:
    gg.watch(x)
    y = x * x * x
  # Computing first order gradient
  first_order = gg.gradient(y, x)

# Computing Second order gradient
second_order  = gfg.gradient(first_order, x) 

# Printing result
print("first_order: ",first_order)
print("second_order: ",second_order)
```

**输出:**

```
first_order:  tf.Tensor(48.0, shape=(), dtype=float32)
second_order:  tf.Tensor(24.0, shape=(), dtype=float32)

```