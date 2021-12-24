# python–tensorlow . math . bincount()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-bincount/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。 **bincount()** 存在于 TensorFlow 的数学模块中。它用于计算整数数组中每个数字的出现次数。

> **语法:**tensorlow . math . bincount(arr，weights，minlength，maxlength，dtype，name)
> 
> **参数:**
> 
> *   **arr:** 是非负值的 dtype int32 的张量。
> *   **权重(可选):**这是一个与 arr 形状相同的张量。arr 中每一个值的计数按其对应的权重递增。
> *   **最小长度(可选):**定义返回输出的最小长度。
> *   **最大长度(可选):**定义返回输出的最大长度。不计算 arr 中大于或等于 maxlength 的值的 Bin。
> *   **数据类型(可选):**如果权重为无，则确定返回输出的数据类型。
> *   **名称(可选):**这是一个可选参数，用于定义操作的名称。
>     
> 
> **返回:**
> 返回一个与权值或给定数据类型具有相同数据类型的向量。向量的索引定义了值，它的值定义了 arr 中索引的 bin。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([1,2,3,4,5,1,7,3,1,1,5], dtype = tf.int32)

# printing the input
print('a: ',a)

# evaluating bin
r = tf.math.bincount(a)

# printing result
print("Result: ",r)
```

**输出:**

```py
a:  tf.Tensor([1 2 3 4 5 1 7 3 1 1 5], shape=(11,), dtype=int32)
Result:  tf.Tensor([0 4 1 2 1 2 0 1], shape=(8,), dtype=int32)

# bin of 0 in input is 0, bin of 1 in input is 4 and so on

```

**示例 2:** 此示例提供了权重，因此值将增加相应的权重，而不是 1。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([1,2,3,4,5,1,7,3,1,1,5], dtype = tf.int32)
weight = tf.constant([0,2,1,0,2,1,3,3,1,0,5], dtype = tf.int32)

# printing the input
print('a: ',a)
print('weight: ',weight)

# evaluating bin
r = tf.math.bincount(arr = a,weights = weight)

# printing result
print("Result: ",r)
```

**输出:**

```py
a:  tf.Tensor([1 2 3 4 5 1 7 3 1 1 5], shape=(11,), dtype=int32)
weight:  tf.Tensor([0 2 1 0 2 1 3 3 1 0 5], shape=(11,), dtype=int32)
Result:  tf.Tensor([0 2 2 4 0 7 0 3], shape=(8,), dtype=int32)

```