# Python 中 pandas.array()函数

> 原文:[https://www . geesforgeks . org/pandas-数组-python 中的函数/](https://www.geeksforgeeks.org/pandas-array-function-in-python/)

此方法用于根据所需数据类型的序列创建数组。

> **语法:** pandas.array(数据:Sequence[object]，dtype: Union[str，numpy.dtype，pandas . core . dtypes . base . extension dtype，NoneType] = None，copy: bool = True)
> 
> **参数:**
> 
> *   **数据:**对象的序列。“data”中的标量应该是“type”的标量类型的实例。预计“数据”代表一维数据阵列。当“数据”是索引或序列时，将从“数据”中提取底层数组。
> *   **dtype :** tr、np.dtype 或 ExtensionDtype，可选。用于数组的数据类型。这可能是一个 NumPy 数据类型，也可能是熊猫注册的扩展类型。
> *   **复制:** bool，默认 True。是否复制数据，即使没有必要。根据“数据”的类型，创建新阵列可能需要复制数据，即使“复制=假”。

下面是上述方法的实现，并附有一些例子:

**例 1 :**

## 蟒蛇 3

```py
# importing packages
import pandas

# create Pandas array with dtype string
pd_arr = pandas.array(data=[1,2,3,4,5],dtype=str)

# print the formed array
print(pd_arr)
```

**输出:**

```py
<PandasArray>
['1', '2', '3', '4', '5']
Length: 5, dtype: str32

```

**例 2 :**

## 蟒蛇 3

```py
# importing packages
import pandas
import numpy

# create Pandas array with dtype from numpy
pd_arr = pandas.array(data=['1', '2', '3', '4', '5'],
                      dtype=numpy.int8)

# print the formed array
print(pd_arr)
```

**输出:**

```py
<PandasArray>
[1, 2, 3, 4, 5]
Length: 5, dtype: int8

```