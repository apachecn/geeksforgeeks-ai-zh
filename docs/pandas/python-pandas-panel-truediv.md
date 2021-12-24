# Python | Pandas panels . truediv()

> 原文:[https://www.geeksforgeeks.org/python-pandas-panel-truediv/](https://www.geeksforgeeks.org/python-pandas-panel-truediv/)

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

熊猫`**Panel.truediv()**`功能用于获取系列和数据框/面板的浮动划分。

> **语法:** Panel.truediv(其他，轴=0)
> 
> **参数:**
> **其他:**数据框或面板
> **轴:**轴广播结束
> 
> **返回:**面板

**代码#1:**

```
# importing pandas module 
import pandas as pd 
import numpy as np 

df1 = pd.DataFrame({'a': ['Geeks', 'For', 'geeks', 'real'], 
                    'b': [111, 123, 425, 1333]}) 

df2 = pd.DataFrame({'a': ['I', 'am', 'dataframe', 'two'], 
                    'b': [100, 100, 100, 100]}) 

data = {'item1':df1, 'item2':df2}

# creating Panel 
panel = pd.Panel.from_dict(data, orient ='minor') 
print("panel['b'] is - \n\n", panel['b']) 

print("\nFloating Dividing panel['b'] with df2['b'] using truediv() method - \n") 
print("\n", panel['b'].truediv(df2['b'], axis = 0)) 
```

**Output:**

```
panel['b'] is - 

    item1  item2
0    111    100
1    123    100
2    425    100
3   1333    100

Floating Dividing panel['b'] with df2['b'] using truediv() method - 

    item1  item2
0   1.11      1
1   1.23      1
2   4.25      1
3  13.33      1

```

**代码#2:**

```
# importing pandas module 
import pandas as pd 
import numpy as np 

df1 = pd.DataFrame({'a': ['Geeks', 'For', 'geeks', 'for', 'real'], 
                    'b': [11, 1.025, 333, 114.48, 1333]}) 

data = {'item1':df1, 'item2':df1} 

# creating Panel 
panel = pd.Panel.from_dict(data, orient ='minor') 
print("panel['b'] is - \n\n", panel['b'], '\n') 

# Create a 5 * 5 dataframe 
df2 = pd.DataFrame(np.random.rand(5, 2), columns =['item1', 'item2']) 
print("Newly create dataframe with random values is - \n\n", df2)

print("\nFloating Dividing panel['b'] with df2 using truediv() method - \n") 
print(panel['b'].truediv(df2, axis = 0)) 
```

**Output:**

```
panel['b'] is - 

       item1     item2
0    11.000    11.000
1     1.025     1.025
2   333.000   333.000
3   114.480   114.480
4  1333.000  1333.000 

Newly create dataframe with random values is - 

       item1     item2
0  0.154734  0.270466
1  0.793149  0.594710
2  0.203894  0.133580
3  0.986028  0.826181
4  0.814395  0.072388

Floating Dividing panel['b'] with df2 using truediv() method - 

         item1         item2
0    71.089512     40.670489
1     1.292318      1.723528
2  1633.203306   2492.883184
3   116.102223    138.565208
4  1636.798165  18414.531628

```

**代码#3:**

```
# importing pandas module 
import pandas as pd 
import numpy as np 

df1 = pd.DataFrame({'a': ['Geeks', 'For', 'geeks', 'for', 'real'], 
                    'b': [11, 1.025, 333, 114.48, 1333]}) 

df2 = pd.DataFrame({'a': ['I', 'am', 'DataFrame', 'number', 'two'], 
                    'b': [10, 10, 10, 110, 110]})                     

data = {'item1':df1, 'item2':df2} 

# creating Panel 
panel = pd.Panel.from_dict(data, orient ='minor') 

print("panel['b'] is - \n\n", panel['b'], '\n') 

print("\nFloating Dividing panel['b']['item1'] with df2['b'] or panel['b']['item2'] using truediv() method - \n") 
print("\n", panel['b']['item1'].truediv(df2['b'], axis = 0)) 
```

**Output:**

```
panel['b'] is - 

       item1  item2
0    11.000     10
1     1.025     10
2   333.000     10
3   114.480    110
4  1333.000    110 

Floating Dividing panel['b']['item1'] with df2['b'] or panel['b']['item2'] using truediv() method - 

 0     1.100000
1     0.102500
2    33.300000
3     1.040727
4    12.118182
dtype: float64

```