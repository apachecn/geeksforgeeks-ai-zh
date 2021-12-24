# python–tensorlow . argsort()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-argsort-method/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。张量流有一种方法 argsort()，用于按排序顺序查找张量的索引。

> **语法:** tf.argsort(值、轴、方向、稳定、名称)
> 
> **参数:**
> 
> *   **值:**是任意维度的数值张量。
> *   **轴:**定义需要进行短路的轴。如果没有给定值，默认值为-1，并根据最后一个轴进行排序。
> *   **方向:**或者*上升*或者*下降*。
> *   **稳定:**要么*真*要么*假。*如果是真的，那么在平等的情况下，维持原有的秩序。
> *   **名称:**这是一个可选参数，用于定义操作的名称。
> 
> **Return:** 它返回 int32 类型的张量，其形状与值相同。这个张量包含给出给定值排序顺序的索引。
> 
> *如果轴或方向无效，将产生值错误。*

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow

# initializing value
a= [1,5,2.5,10,7,8.5]

# getting the indices for sorted values
b = tensorflow.argsort(a,axis=-1,direction='ASCENDING',stable=False)

# printing the result
print('Indices:'b)

print('Sorted values')
#printing the sorted value
for i in b:
  print(a[i])
```

**输出:**

```
Indices: tf.Tensor([0 2 1 4 5 3], shape=(6,), dtype=int32)
Sorted Values
1
2.5
5
7
8.5
10

```

**示例 2:** 在此示例中，错误的值传递到方向。这将引发值错误。

## 蟒蛇 3

```
# importing the library
import tensorflow

# initializing value
a= [1,5,2.5,10,7,8.5]

# getting the indices for sorted values
b = tensorflow.argsort(a,axis=-1,direction='ASC',stable=False)
```

**输出:**

```
ValueError: ASC should be one of ASCENDING, DESCENDING

```