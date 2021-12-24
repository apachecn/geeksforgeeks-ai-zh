# Tensorflow | TF . data . dataset . reduce()

> 原文:[https://www . geesforgeks . org/tensorflow-TF-data-dataset-reduce/](https://www.geeksforgeeks.org/tensorflow-tf-data-dataset-reduce/)

借助`**tf.data.Dataset.reduce()**`方法，利用`tf.data.Dataset.reduce()`方法可以得到数据集中所有元素的约简变换。

> **语法:** `tf.data.Dataset.reduce()`
> **返回:**转换后返回组合单结果。

**注意:**
这些给定的示例将演示 tensorflow 2.0 新版本的使用，因此如果您想要运行这些示例，请在命令提示符下运行以下命令。

```
pip install tensorflow==2.0.0-rc2
```

**示例#1 :**
在这个示例中，我们可以看到，通过使用`tf.data.Dataset.reduce()`方法，我们能够从数据集获得所有元素的简化变换。

```
# import tensorflow
import tensorflow as tf

# using tf.data.Dataset.reduce() method
gfg = tf.data.Dataset.from_tensor_slices([1, 2, 3, 4, 5])

print(gfg.reduce(0, lambda x, y: x + y).numpy())
```

**输出:**

> Fifteen

**例 2 :**

```
# import tensorflow
import tensorflow as tf

# using tf.data.Dataset.reduce() method
gfg = tf.data.Dataset.from_tensor_slices([[5, 10], [3, 6]])

print(gfg.reduce(0, lambda x, y: x * y).numpy())
```

**输出:**

> [15, 60]