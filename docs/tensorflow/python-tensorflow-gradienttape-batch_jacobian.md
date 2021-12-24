# python–tensorlow。gradienttape . batch _ Jacobian()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-gradienttape-batch _ Jacobian/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**batch_jacobian()** 用于计算和堆叠每个示例的 jacobian。

> **语法:** batch_jacobian(目标、源、未连接 _ 渐变、并行 _ 迭代、实验 _ 使用 _pfor)
> 
> **参数:**
> 
> *   **目标:**是最小秩为 2 的张量。
> *   **来源:**是最小秩为 2 的张量。
> *   **未连接 _ 渐变(可选):**它的值可以为零或无。默认值为无。
> *   **parallel_iterations(可选):**用于控制并行迭代和内存使用。
> *   **experial _ use _ pfor(可选):**为布尔值，默认值为 True。当设置为 true 时，它使用 pfor 计算雅可比，否则使用 tf.while_loop。
> 
> **返回:**返回张量。**T3】**

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

x = tf.constant([[4, 2],[1, 3]], dtype=tf.dtypes.float32)

# Using GradientTape
with tf.GradientTape() as gfg:
  gfg.watch(x)
  y = x * x * x

# Computing jacobian
res  = gfg.batch_jacobian(y, x) 

# Printing result
print("res: ",res)
```

**输出:**

```
res:  tf.Tensor(
[[[48\.  0.]
  [ 0\. 12.]]

 [[ 3\.  0.]
  [ 0\. 27.]]], shape=(2, 2, 2), dtype=float32)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

x = tf.constant([[4, 2],[1, 3]], dtype=tf.dtypes.float32)

# Using GradientTape
with tf.GradientTape() as gfg:
  gfg.watch(x)

  # Using nested GradientTape for calculating higher order jacobian
  with tf.GradientTape() as gg:
    gg.watch(x)
    y = x * x * x
  # Computing first order jacobian
  first_order = gg.batch_jacobian(y, x)

# Computing Second order jacobian
second_order  = gfg.batch_jacobian(first_order, x) 

# Printing result
print("first_order: ",first_order)
print("second_order: ",second_order)
```

**输出:**

```
first_order:  tf.Tensor(
[[[48\.  0.]
  [ 0\. 12.]]

 [[ 3\.  0.]
  [ 0\. 27.]]], shape=(2, 2, 2), dtype=float32)
second_order:  tf.Tensor(
[[[[24\.  0.]
   [ 0\.  0.]]

  [[ 0\.  0.]
   [ 0\. 12.]]]

 [[[ 6\.  0.]
   [ 0\.  0.]]

  [[ 0\.  0.]
   [ 0\. 18.]]]], shape=(2, 2, 2, 2), dtype=float32)

```