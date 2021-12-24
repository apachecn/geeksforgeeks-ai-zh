# python | panda panel . rfloordiv()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-pandas-panel-rfloordiv/

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

熊猫中`**Panel.rfloordiv()**`函数用于获取数列和数据框/面板的整数除法。

> **语法:** Panel.rfloordiv(其他，轴=0)
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

df1 = pd.DataFrame({'a': ['Geeks', 'For', 'geeks', 'real'], 
                    'b': [111, 123, 425, 1333]}) 

df2 = pd.DataFrame({'a': ['I', 'am', 'dataframe', 'two'], 
                    'b': [5, 5, 2, 10]}) 

data = {'item1':df1, 'item2':df2}

# creating Panel 
panel = pd.Panel.from_dict(data, orient ='minor') 
print("panel['b'] is - \n\n", panel['b']) 

print("\nInteger Dividing panel['b'] with df2['b'] using rfloordiv() method - \n") 
print("\n", panel['b'].rfloordiv(df2['b'], axis = 0)) 
```

**Output:**

```py
panel['b'] is - 

    item1  item2
0    111      5
1    123      5
2    425      2
3   1333     10

Integer Dividing panel['b'] with df2['b'] using rfloordiv() method - 

    item1  item2
0      0      1
1      0      1
2      0      1
3      0      1

```

**代码#2:**

```py
# importing pandas module 
import pandas as pd 
import numpy as np 

df1 = pd.DataFrame({'a': ['Geeks', 'For', 'geeks', 'for', 'real'], 
                    'b': [11, 1.025, 333, 114.48, 1333]}) 

df2 = pd.DataFrame({'a': ['I', 'am', 'DataFrame', 'number', 'two'], 
                    'b': [3, 3, 3, 13, 27]})                     

data = {'item1':df1, 'item2':df2} 

# creating Panel 
panel = pd.Panel.from_dict(data, orient ='minor') 

print("panel['b'] is - \n\n", panel['b'], '\n') 

print("\nInteger Dividing panel['b']['item1'] with df2['b'] or panel['b']['item2'] using rfloordiv() method - \n") 
print("\n", panel['b']['item1'].rfloordiv(df2['b'], axis = 0)) 
```

**Output:**

```py
panel['b'] is - 

       item1  item2
0    11.000      3
1     1.025      3
2   333.000      3
3   114.480     13
4  1333.000     27 

Integer Dividing panel['b']['item1'] with df2['b'] or panel['b']['item2'] using rfloordiv() method - 

 0    0
1    2
2    0
3    0
4    0
dtype: float64

```