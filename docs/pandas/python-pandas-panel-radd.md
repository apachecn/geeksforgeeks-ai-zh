# 蟒蛇|熊猫面板. radd()

> 原文:[https://www.geeksforgeeks.org/python-pandas-panel-radd/](https://www.geeksforgeeks.org/python-pandas-panel-radd/)

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

在熊猫中`**Panel.radd()**`功能用于序列和序列/数据帧的元素相加。相当于其他+面板。

> **语法:** Panel.radd(其他，轴=0)
> 
> **参数:**
> **其他:**数据框或面板
> **轴:**轴广播结束
> 
> **返回:**面板

**代码#1:**

```py
# importing pandas module  
import pandas as pd  
import numpy as np 

df1 = pd.DataFrame({'a': ['Geeks', 'For', 'geeks', 'for', 'real'],  
                    'b': [11, 1.025, 333, 114.48, 1333]}) 

data = {'item1':df1, 'item2':df1} 

# creating Panel  
panel = pd.Panel.from_dict(data, orient ='minor') 

print("panel['b'] is - \n\n", panel['b'], '\n') 

print("\nAdding panel['b'] with df1['b'] using radd() method - \n")   
print("\n", panel['b'].radd(df1['b'], axis = 0)) 
```

**Output:**

```py
panel['b'] is - 

       item1     item2
0    11.000    11.000
1     1.025     1.025
2   333.000   333.000
3   114.480   114.480
4  1333.000  1333.000 

Adding panel['b'] with df1['b'] using radd() method - 

      item1    item2
0    22.00    22.00
1     2.05     2.05
2   666.00   666.00
3   228.96   228.96
4  2666.00  2666.00

```

**代码#2:**

```py
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

print("\nAdding panel['b'] with df2  using radd() method - \n")  
print(panel['b'].radd(df2, axis = 0)) 
```

**Output:**

```py
panel['b'] is - 

       item1     item2
0    11.000    11.000
1     1.025     1.025
2   333.000   333.000
3   114.480   114.480
4  1333.000  1333.000 

Newly create dataframe with random values is - 

       item1     item2
0  0.584980  0.504366
1  0.730408  0.259226
2  0.255814  0.825562
3  0.459585  0.052188
4  0.197732  0.551450

Adding panel['b'] with df2  using radd() method - 

         item1        item2
0    11.584980    11.504366
1     1.755408     1.284226
2   333.255814   333.825562
3   114.939585   114.532188
4  1333.197732  1333.551450

```

**代码#3:**

```py
# importing pandas module 
import pandas as pd 
import numpy as np 

df1 = pd.DataFrame({'a': ['Geeks', 'For', 'geeks', 'real'], 
                    'b': [-11, +1.025, -114.48, 1333]}) 

df2 = pd.DataFrame({'a': ['I', 'am', 'dataframe', 'two'], 
                    'b': [100, 100, 100, 100]}) 

data = {'item1':df1, 'item2':df2}

# creating Panel 
panel = pd.Panel.from_dict(data, orient ='minor') 
print("panel['b'] is - \n\n", panel['b']) 

print("\nAdding panel['b'] with df2['b'] using radd() method - \n")   
print("\n", panel['b'].radd(df2['b'], axis = 0)) 
```

**Output:**

```py
panel['b'] is - 

       item1  item2
0   -11.000    100
1     1.025    100
2  -114.480    100
3  1333.000    100

Adding panel['b'] with df2['b'] using radd() method - 

       item1  item2
0    89.000    200
1   101.025    200
2   -14.480    200
3  1433.000    200

```