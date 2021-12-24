# 熊猫数据帧中浅拷贝和深拷贝的区别

> 原文:[https://www . geeksforgeeks . org/difference-in-pandas-data frames/](https://www.geeksforgeeks.org/difference-between-shallow-copy-vs-deep-copy-in-pandas-dataframes/)

[熊猫](https://www.geeksforgeeks.org/pandas-tutorial/)库主要有两个数据结构[数据帧](https://www.geeksforgeeks.org/python-pandas-dataframe/)和[系列](https://www.geeksforgeeks.org/python-pandas-series/)。这些数据结构在内部用标记数据的索引数组和包含实际数据的数据数组来表示。现在，当我们试图复制这些数据结构(数据帧和系列)时，我们实际上复制了对象的索引和数据，有两种方法可以做到这一点，即浅拷贝和深拷贝。

这些操作是在库函数*熊猫的帮助下完成的。浅拷贝和 T2 熊猫的数据帧拷贝(深=假)*。数据框.拷贝(深度=真)用于数据框和系列中的深度拷贝。

现在，让我们来理解什么是浅层复制。

## 浅拷贝

当创建数据框或系列对象的浅拷贝时，它不会拷贝原始对象的索引和数据，而只是拷贝对其索引和数据的引用。因此，对其中一个所做的更改会反映在另一个中。

它指的是构造一个新的集合对象，然后用在原始集合中找到的子对象的引用填充它。复制过程不会重复，因此不会创建子对象本身的副本。

**示例:**

![](img/7b2f7d224c489d0a58f818abfb2651b4.png)

## 蟒蛇 3

```
# porgam to depict shallow copy
# in pandas dataframe

# import module
import pandas as pd

# assign dataframe
df = pd.DataFrame({'index': [1, 2, 3, 4],
                   'GFG': ['Mandy', 'Ron', 'Jacob', 'Bayek']})

# shallow copy
copydf = df.copy(deep=False)

# comparing shallow copied dataframe
# and original dataframe
print('\nBefore Operation:\n', copydf == df)

# assignment operation
copydf['index'] = [0, 0, 0, 0]

# comparing shallow copied dataframe
# and original dataframe
print('\nAfter Operation:\n', copydf == df)

print('\nOriginal Dataframe after operation:\n', df)
```

**输出:**

![](img/b9fea20b0788a713036856e8a5c2e9f8.png)

从上面程序的输出中我们可以看到，应用于浅拷贝数据帧的更改会自动应用于原始数据帧。

## 深度复制

数据框或系列对象的深层副本有自己的索引和数据副本。这是一个复制过程递归发生的过程。这意味着首先构造一个新的集合对象，然后递归地用在原始集合中找到的子对象的副本填充它。在深度复制的情况下，一个对象的副本被复制到另一个对象中。这意味着对对象副本所做的任何更改都不会反映在原始对象中。

**示例:**

![](img/af715b5797c00a34a41dff0e63b8a095.png)

## 蟒蛇 3

```
# porgam to depict deep copy
# in pandas dataframe

# import module
import pandas as pd

# assign dataframe
df = pd.DataFrame({'index': [1, 2, 3, 4],
                   'GFG': ['Mandy', 'Ron', 'Jacob', 'Bayek']})

# deep copy
copydf = df.copy(deep=True)

# comparing shallow copied dataframe
# and original dataframe
print('\nBefore Operation:\n', copydf == df)

# assignment operation
copydf['index'] = [0, 0, 0, 0]

# comparing shallow copied dataframe
# and original dataframe
print('\nAfter Operation:\n', copydf == df)

print('\nOriginal Dataframe after operation:\n', df)
```

**输出:**

![](img/6f9056a5b4abdbf138df40cd60c60b6f.png)

这里，原始对象内部的数据不会被递归复制。也就是说，原始对象的数据内部的数据仍然指向同一个存储单元。例如，如果 Dataframe 或 Series 对象中的数据包含任何可变数据，则该数据将在其与其深层副本之间共享，对其中一个的任何修改都将反映在另一个中。

## 浅拷贝和深拷贝之间的差异表

<figure class="table">

| 不，先生。 | 浅拷贝 | 深度复制 |
| --- | --- | --- |
| one | 是集合结构的副本，不是元素。 | 是集合的副本，原始集合中的所有元素都被复制。 |
| Two | 影响初始数据帧。 | 不影响初始数据帧。 |
| three | 浅层复制不会复制子对象。 | 深度复制递归复制子对象。 |
| four | 与深度拷贝相比，创建浅拷贝速度更快。 | 与浅拷贝相比，创建深拷贝较慢。 |
| five | 副本依赖于原件 | 副本并不完全依赖于原件。 |

</figure>