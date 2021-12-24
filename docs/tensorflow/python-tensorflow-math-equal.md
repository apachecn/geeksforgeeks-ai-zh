# python–tensorlow . math . equal()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-equal/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**equal()** 用于通过等式比较来执行元素。它在应用比较之前执行参数广播。

> **语法:** tensorflow.math.equal( x，y，name)
> 
> **参数:**
> 
> *   **x:** 可以是张量或稀疏张量或索引切片。
> *   **y:** 可以是张量或稀疏张量或索引切片。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回布尔张量。

**示例 1:** 在该示例中，执行广播。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([6, 8, 12, 2], dtype = tf.float64)
b = (2)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Performing equality comparison
res = tf.math.equal(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 6\.  8\. 12\.  2.], shape=(4, ), dtype=float64)
b:  2
Result:  tf.Tensor([False False False  True], shape=(4, ), dtype=bool)
```

**例 2:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([6, 8, 12, 4], dtype = tf.float64)
b = tf.constant([2, 8, 12, 7],  dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Performing equality comparison
res = tf.math.equal(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 6\.  8\. 12\.  4.], shape=(4, ), dtype=float64)
b:  tf.Tensor([ 2\.  8\. 12\.  7.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([False  True  True False], shape=(4, ), dtype=bool)
```