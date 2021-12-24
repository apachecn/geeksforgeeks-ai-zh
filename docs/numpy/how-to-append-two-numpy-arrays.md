# 如何追加两个 NumPy 数组？

> 原文:[https://www . geeksforgeeks . org/如何追加两个 numpy 数组/](https://www.geeksforgeeks.org/how-to-append-two-numpy-arrays/)

**先决条件:** [Numpy](https://www.geeksforgeeks.org/python-numpy/)

python 中的两个数组可以以多种方式追加，所有可能的方式都将在下面讨论。

### **方法 1:** 使用 append()方法

此方法用于将值追加到数组的末尾。

> **语法:**
> 
> numpy.append(数组，值，轴=无)
> 
> **参数:**
> 
> *   **数组:**【array _ like】输入数组。
> *   **值:**【array _ like】要在 arr 中添加的值。价值观应该是
>     式的，这样 arr【…，obj，…】=价值观。如果定义了轴，值可以是任何
>     形状，因为它将在使用前展平。
>     
> *   **轴:**我们要沿其插入值的轴。默认情况下，数组是扁平的。
> 
> **返回:**
> 
> 一个数组的副本，其值按照所提到的对象沿着给定的轴附加在末尾。

**示例:**

## 蟒蛇 3

```py
import numpy

array1 = numpy.array([1, 2, 3, 4, 5])
array2 = numpy.array([6, 7, 8, 9, 10])

# Appending both arrays using Append method
array1 = numpy.append(array1, array2)
print(array1)
```

**输出:**

> [ 1  2  3  4  5  6  7  8  9 10]

### 方法 2:使用 concatenate()方法

连接方法沿着现有轴连接一系列数组。

> ***语法:***
> 
> *numpy.concatenate((arr1，arr2，…)，axis=0，out=None)*
> 
> ***参数:***
> 
> *   ***arr1、arr2、…:**【array _ like 序列】数组必须具有相同的形状，除了与轴对应的维度。*
> *   ***轴:**【int，可选】数组将沿其连接的轴。如果轴为“无”，数组在使用前会被展平。默认值为 0。*
> *   ***出:**【ndarray，可选】如果提供，目的地放置结果。形状必须正确，与未指定 out 参数时 concatenate 返回的形状相匹配。*
> 
> ***返回:**【ndarray】串联数组。*

**示例:**

## 蟒蛇 3

```py
import numpy

array1 = numpy.array([1, 2, 3, 4, 5])
array2 = numpy.array([6, 7, 8, 9, 10])

# Appending both Arrays using concatenate() method.
array1 = numpy.concatenate([array1, array2])
print(array1)
```

**输出:**

> [ 1  2  3  4  5  6  7  8  9 10]

### 方法 3:使用 stack()方法

堆栈方法沿着新的轴连接一系列数组。

> ***语法:** numpy.stack(数组，轴)*
> 
> ***参数:***
> 
> *   ***数组:**【类数组】相同形状的数组序列。*
> *   ***轴:**【int】输入数组沿其堆叠的结果数组中的轴。*
> 
> ***返回:**【堆叠数组】输入数组的堆叠数组，比输入数组多一维。*

**示例:**

## 蟒蛇 3

```py
import numpy

array1 = numpy.array([1, 2, 3, 4, 5])
array2 = numpy.array([6, 7, 8, 9, 10])

# Join a sequence of arrays along a new axis.
array1 = numpy.stack([array1, array2])
print(array1)
```

**输出:**

> [[ 1 2 3 4 5]
> 
>  [ 6  7  8  9 10]]

### 方法 4:使用 hstack()方法

hstack 方法水平(按列)按顺序堆叠数组。

> ***语法:**num py . hsack(tup)*
> 
> ***参数:***
> 
> *   ***tup :** 【数组序列】包含要堆叠的数组的元组。除了第二个轴以外，所有的数组都必须具有相同的形状。*
> 
> ***返回:**【堆叠数组】输入数组的堆叠数组。*

**示例:**

## 蟒蛇 3

```py
import numpy

array1 = numpy.array([1, 2, 3, 4, 5])
array2 = numpy.array([6, 7, 8, 9, 10])

# Stack arrays in sequence horizontally (column wise).
array1 = numpy.hstack([array1, array2])
print(array1)
```

**输出:**

> [ 1  2  3  4  5  6  7  8  9 10]

### 方法 5:使用 vstack()方法

vstack 方法垂直(逐行)按顺序堆叠数组。

> **语法:**num py . v ack(tup)
> 
> ***参数:***
> 
> *   ***tup :** 【数组序列】包含要堆叠的数组的元组。除了第一个轴以外，数组必须沿所有轴具有相同的形状。*
> 
> ***返回:**【堆叠数组】输入数组的堆叠数组。*

**示例:**

## 蟒蛇 3

```py
import numpy

array1 = numpy.array([1, 2, 3, 4, 5])
array2 = numpy.array([6, 7, 8, 9, 10])

# Stack arrays in sequence vertically (row wise).
array1 = numpy.vstack([array1, array2])
print(array1)
```

**输出:**

> [[ 1 2 3 4 5]
> 
>  [ 6  7  8  9 10]]

### **方法 6** :使用 column_stack()方法

***column_stack()*** 方法将数组作为列堆叠成二维数组。

> **语法:** column_stack(数组)

## 蟒蛇 3

```py
import numpy

array1 = numpy.array([1, 2, 3, 4, 5])
array2 = numpy.array([6, 7, 8, 9, 10])

# Stack 1-D arrays as columns into a 2-D array.
array1 = numpy.column_stack([array1, array2])
print(array1)
```

**输出:**

```py
*[[ 1  6]*
 *[ 2  7]*
 *[ 3  8]*
 *[ 4  9]*
 *[ 5 10]]*
```