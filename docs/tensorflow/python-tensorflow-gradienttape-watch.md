# python–tensorlow。渐变色带. watch()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-gradienttape watch/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**手表()**用于开始通过磁带追踪张量。

> **语法:**手表(张量)
> 
> **参数:**
> 
> *   **张量:**是要观察的张量或张量列表。
> 
> **返回:**无
> 
> **加注:**
> 
> *   **值错误:**如果传递参数不是 Tensor，它将引发值错误。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

x = tf.constant(4.0)

# Using GradientTape
with tf.GradientTape() as gfg:

  # Starting the recording x
  gfg.watch(x)
  y = x * x

# Computing gradient
res = gfg.gradient(y, x) 

# Printing result
print("res: ", res)
```

**输出:**

```py
res:  tf.Tensor(8.0, shape=(), dtype=float32)

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

x = tf.constant(4.0)
z = tf.constant(5.0)

# Using GradientTape
with tf.GradientTape(persistent = True) as gfg:

  # Starting the recording x and z
  gfg.watch([x, z])
  y = z * z
  u = x * x

# Computing gradient
grad_y = gfg.gradient(y, z) 
grad_u = gfg.gradient(u, x)

# Printing result
print("grad_y: ", grad_y)
print("grad_u: ", grad_u)
```

**输出:**

```py
grad_y:  tf.Tensor(10.0, shape=(), dtype=float32)
grad_u:  tf.Tensor(8.0, shape=(), dtype=float32)

```