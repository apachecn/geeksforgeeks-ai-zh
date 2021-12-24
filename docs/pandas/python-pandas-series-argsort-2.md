# Python |熊猫系列. argsort()

> 原文:[https://www . geesforgeks . org/python-pandas-series-arg sort-2/](https://www.geeksforgeeks.org/python-pandas-series-argsort-2/)

借助**熊猫系列. argsort()** ，可以对熊猫中的系列元素进行排序。但是熊猫系列的主要内容是我们得到的输出是系列中排序元素的**索引值**。在后面的代码演示中，我们将解释如何将输出作为**排序索引值**。

> **语法:**熊猫。Series.argsort(轴=0，种类='quicksort '，顺序=无)
> 
> **参数:**
> **轴:**对 numpy 有用。
> **种类:** {'mergesort '，' quicksort '，' heapsort'}，默认' quicksort'
> **顺序:**对 numpy 有用。
> 
> **返回:** argsorted Series，其中-1 表示存在 nan 值的位置

要获得 csv 文件的链接，点击 [nba.csv](https://media.geeksforgeeks.org/wp-content/uploads/nba.csv)

**代码#1 :**
在这段代码中，您会看到我们正在取一些整数值的简单序列，并尝试基于不同的排序算法方法进行排序，如**快速排序**、**合并排序**和**堆排序**，但默认情况下，它将假设为快速排序。让我们看看下面的代码和下面的输出。

```
# importing pandas 
import pandas as pd  

# reading the csv   
data = pd.read_csv("nba.csv")

data.dropna(inplace = True)

# creating series form weight column 
g = pd.Series(data['Weight'].head())
print(g)

gfg = g.argsort(axis = 0, kind ='quicksort', order = None)

print(gfg)
```

**Output:**

```
0    180.0
1    235.0
3    185.0
6    235.0
7    238.0
Name: Weight, dtype: float64
0    0
1    2
3    1
6    3
7    4
Name: Weight, dtype: int64

```

正如你在输出中看到的，看起来很奇怪，为什么我们没有得到序列的排序值，而是得到了这些数字。这是`Series.argsort()`方法的主要概念，它首先返回一个最小数的索引值，最后返回最大值的索引值。因为我们有 1 是最小的数字，它的索引值是 4，那么 4 将首先出现，这个概念就像下面的输出一样流动。

**代码#2 :**

```
# importing pandas 
import pandas as pd  

# reading the csv   
data = pd.read_csv("nba.csv")

data.dropna(inplace = True)

# creating series form weight column 
g = pd.Series(data['Weight'].head())
print(g)

gfg = g.argsort(axis = 0, kind ='mergesort', order = None)

print(gfg)
```

**Output:**

```
0    180.0
1    235.0
3    185.0
6    235.0
7    238.0
Name: Weight, dtype: float64
0    0
1    2
3    1
6    3
7    4
Name: Weight, dtype: int64

```

**代码#3 :**

```
# importing pandas 
import pandas as pd  

# reading the csv   
data = pd.read_csv("nba.csv")

data.dropna(inplace = True)

# creating series form weight column 
g = pd.Series(data['Weight'].head())
print(g)

gfg = g.argsort(axis = 0, kind ='heapsort', order = None)

print(gfg)
```

**Output:**

```
0    180.0
1    235.0
3    185.0
6    235.0
7    238.0
Name: Weight, dtype: float64
0    0
1    2
3    1
6    3
7    4
Name: Weight, dtype: int64

```

**当我们有缺失值时，输出是什么？**

如上所述，如果我们想要处理丢失的值，那么在**无**的地方，它将给出-1 的输出。

```
import pandas as pd

# importing pandas 
import pandas as pd  

# reading the csv   
data = pd.read_csv("nba.csv")

# creating series form weight column 
g = pd.Series(data['Weight'])
print(g)

gfg = g.argsort(axis = 0, kind ='mergesort', order = None)

print(gfg)
```

**Output:**

```
450    226.0
451    206.0
452    234.0
453    203.0
454    179.0
455    256.0
456    231.0
457      NaN
Name: Weight, Length: 458, dtype: float64
450    237
451     41
452    188
453    395
454    330
455    302
456    405
457     -1
Name: Weight, Length: 458, dtype: int64

```