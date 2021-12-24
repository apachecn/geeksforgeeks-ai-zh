# python–tensorlow . gradients()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-gradients/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**梯度()**用于得到 xs 中 ys w.r.t. x 之和的符号导数。当启用紧急执行时，它不起作用。

> **Syantx:**tensorflow . gradients(ys，xs，grad_ys，name，gate_gradients，aggregation_method，stop_gradients，unconnected_gradients)
> 
> **参数:**
> 
> *   **ys:** 需要区分的是张量或张量列表。
> *   **xs:** 是张量或张量列表，用于微分。
> *   **grad_ys(可选):**它是张量或张量列表，用于计算 y 的梯度
> *   **名称(可选):**一起用于组梯度运算。它的默认值是渐变。
> *   **gate_gradients(可选):**用于避免比赛状态。如果为真，它将在操作返回的梯度周围添加一个元组。
> *   **aggregation_method(可选):**它的值是在 AggregationMethod 类中定义的常数。
> *   **stop_gradients(可选):**这是一个张量或张量列表，无法区分。
> *   **unconnected_gradients(可选):**指定给定输入张量未连接时返回的梯度值。接受的值是在非连接类中定义的常数。
> 
> **返回:**长度张量(xs)的列表，其中每个张量是 y 在 ys 中的和 x 在 xs 中的和(dy/dx)。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Defining function
@tf.function
def gfg():
  a = tf.ones([1, 2])
  b = 5*a

  # Calculating gradient
  g1 = tf.gradients([b+a], [a])

  # Printing result
  print("res: ",g1)

# Calling the  function
gfg()
```

**输出:**

```py
res:  [<tf.Tensor 'gradients/AddN:0' shape=(1, 2) dtype=float32>]
```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Defining function
@tf.function
def gfg():
  a = tf.ones([1, 2])
  b = 5*a

  # Calculating gradient
  g1 = tf.gradients([b], [a])

  # Printing result
  print("res: ",g1)

# Calling the  function
gfg()
```

**输出:**

```py
res:  [<tf.Tensor 'gradients/mul_grad/Mul_1:0' shape=(1, 2) dtype=float32>]
```