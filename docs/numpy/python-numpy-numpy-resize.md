# python | num py . resize()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-resize/

借助 **Numpy numpy.resize()** ，我们可以调整数组的大小。阵列可以是任何形状，但要调整大小，我们只需要大小，即 **(2，2)** 、 **(2，3)** 和更多。在调整 numpy 的大小时，如果特定位置的值丢失，则追加**个零**。

> **参数:**
> **new_shape :** 【整数元组，或 n 个整数】调整大小数组的 Shape
> **refcheck:**【bool，可选】此参数用于检查引用计数器。默认情况下，它为真。
> 
> **返回:**无

你们大多数人现在都在想**重塑**和**调整**有什么区别。当我们谈论重塑时，一个数组改变它的形状是暂时的，但是当我们谈论调整大小时，这些改变是永久的。

**示例#1:**
在这个示例中我们可以看到，借助`**.resize()**`方法，我们已经将数组的形状从 **1×6** 更改为 **2×3** 。

```py
# importing the python module numpy
import numpy as np

# Making a random array
gfg = np.array([1, 2, 3, 4, 5, 6])

# Reshape the array permanently
gfg.resize(2, 3)

print(gfg)
```

**Output:**

```py
[[1 2 3]
 [4 5 6]]

```

**示例#2:**
在这个示例中，我们可以看到，我们正在尝试调整该形状数组的大小，该形状属于越界值类型。但是当数组中没有值时，numpy 会处理这种情况，在后面加上**零**。

```py
# importing the python module numpy
import numpy as np

# Making a random array
gfg = np.array([1, 2, 3, 4, 5, 6])

# Required values 12, existing values 6
gfg.resize(3, 4)

print(gfg)
```

**Output:**

```py
[[1 2 3 4]
 [5 6 0 0]
 [0 0 0 0]]

```