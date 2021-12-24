# python–tensorlow。gradienttape . gradients()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-gradienttape 梯度/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**渐变()**用于使用在该磁带上下文中记录的操作来计算渐变。

> **语法:**渐变(目标、源、输出 _ 渐变、未连接 _ 渐变)
> 
> **参数:**
> 
> *   **目标:**是待区分张量或张量列表。
> *   **来源:**是 Tensor 或 Tensor 列表。目标值与来源不同。
> *   **output_gradients:** 是一个梯度列表，默认值为无。
> *   **未连接 _ 渐变:**其值可以是无，也可以是零，默认值为无。
> 
> **返回:**返回张量的列表或嵌套结构。

**例 1:**

## 蟒蛇 3

```py
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

```py

res:  tf.Tensor(48.0, shape=(), dtype=float32)

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

x = tf.constant(4.0)

# Using GradientTape
with tf.GradientTape() as gfg:
  gfg.watch(x)

  # Using nested GradientTape for 
  # calculating higher order derivative
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

```py

first_order:  tf.Tensor(48.0, shape=(), dtype=float32)
second_order:  tf.Tensor(24.0, shape=(), dtype=float32)

```