# TensorFlow 中的 tf .转置()函数

> 原文:[https://www . geesforgeks . org/TF-transpose-function-in-tensorflow/](https://www.geeksforgeeks.org/tf-transpose-function-in-tensorflow/)

`tf.transpose()`是 TensorFlow 中提供的函数。该函数用于转置输入张量。

> **语法:** tf .转置(input_tensor，perm，共轭)
> 
> **参数:**
> **input_tensor:** 顾名思义就是要转置的张量。
> **类型:**张量
> 
> **perm:** 该参数指定了 input_tensor 将被转置的置换。
> T3】型:矢量
> 
> **共轭:**如果输入张量类型为复数，该参数设置为**真**。
> T5】类型:布尔型

**例 1:**

```py
import tensorflow as geek

x = geek.constant([[1, 2, 3, 4],
                   [5, 6, 7, 8]])
transposed_tensor = geek.transpose(x)
```

**输出:**

```py
array([[1, 5],
       [2, 6],
       [3, 7],
       [4, 8]])

```

**示例 2:** **使用烫发参数:**

当这个参数通过时，张量沿着给定的轴被转置。简单地说，它定义了转置张量的输出形状。

```py
import tensorflow as geek

x = geek.constant([[[ 1, 2, 3],
                    [ 4, 5, 6]],
                   [[ 7, 8, 9],
                    [ 10, 11, 12]],
                   [[ 13, 14, 15],
                    [ 16, 17, 18]],
                   [[ 19, 20, 21],
                    [ 22, 23, 24]]])
transposed_tensor = geek.transpose(x, perm = [0, 2, 1])
```

**输出:**

```py
array([[[ 1,  4],
        [ 2,  5],
        [ 3,  6]],

       [[ 7, 10],
        [ 8, 11],
        [ 9, 12]],

       [[13, 16],
        [14, 17],
        [15, 18]],

       [[19, 22],
        [20, 23],
        [21, 24]]])
shape (4, 3, 2)

```

形状是(4，3，2)，因为我们的烫发是[0，2，1]。下面是从 perm 到输入张量形状的映射。

```py
0 => 4
2 => 3
1 => 2
```

**例 3:** **现在我们来研究共轭参数**
当我们的张量中有复变量时，它被设置为 **True** 。

```py
import tensorflow as geek

x = geek.constant([[1 + 1j, 2 + 2j, 3 + 3j],
                   [4 + 4j, 5 + 5j, 6 + 6j]])
transposed_tensor = geek.transpose(x)
```

**输出:**

```py
array([[1 + 1j, 4 + 4j],
       [2 + 2j, 5 + 5j],
       [3 + 3j, 6 + 6j]])

```