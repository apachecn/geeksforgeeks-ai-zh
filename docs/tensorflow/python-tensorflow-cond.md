# python–tensorlow . cond()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-cond/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**cond()** 如果谓词 pred 为真，则返回 true_fn()，否则返回 false_fn()。

> **语法:**tensorlow . cond(pred，true_fn，false_fn，name)
> 
> **参数:**
> 
> *   **pred:** 它是一个标量，决定了要返回的可调用
> *   **true_fn(可选):【pred 为真时返回。**
> *   **false_fn(可选):【pred 为 false 时返回。**
> *   **名称(可选):**定义操作的名称。
> 
> **Return:** 返回可调用的求值结果。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
x = 5
y = 10

# Printing the input
print('x: ', x)
print('y: ', y)

# Calculating result
res = tf.cond(x < y, lambda: tf.add(x, y), lambda: tf.square(y))

# Printing the result
print('Result: ', res)
```

**输出:**

```py
x:  5
y:  10
Result:  tf.Tensor(15, shape=(), dtype=int32)

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
x = 5
y = 10

# Printing the input
print('x: ', x)
print('y: ', y)

# Calculating result
res = tf.cond(x > y, lambda: tf.add(x, y), lambda: tf.square(y))

# Printing the result
print('Result: ', res)
```

**输出:**

```py
x:  5
y:  10
Result:  tf.Tensor(100, shape=(), dtype=int32)
```