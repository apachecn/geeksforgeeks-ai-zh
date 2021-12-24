# Python | Pandas panels . mod()

> 原文:[https://www.geeksforgeeks.org/python-pandas-panel-mod/](https://www.geeksforgeeks.org/python-pandas-panel-mod/)

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

熊猫`**Panel.mod()**`功能用于获取系列模块和数据框/面板。

> **语法:** Panel.mod(其他，轴=0)
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
                    'b': [100, 100, 100, 100]}) 

data = {'item1':df1, 'item2':df2}

# creating Panel 
panel = pd.Panel.from_dict(data, orient ='minor') 
print("panel['b'] is - \n\n", panel['b']) 

print("\nModulo of panel['b'] with df2['b'] using mod() method - \n") 
print("\n", panel['b'].mod(df2['b'], axis = 0)) 
```

**Output:**

```py
panel['b'] is - 

    item1  item2
0    111    100
1    123    100
2    425    100
3   1333    100

Modulo of panel['b'] with df2['b'] using mod() method - 

    item1  item2
0     11      0
1     23      0
2     25      0
3     33      0

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

print("\nModulo of panel['b'] with df2 using mod() method - \n") 
print(panel['b'].mod(df2, axis = 0)) 
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
0  0.003619  0.293626
1  0.624030  0.360525
2  0.335041  0.450568
3  0.414065  0.120144
4  0.842085  0.222036

Modulo of panel['b'] with df2 using mod() method - 

      item1     item2
0  0.001529  0.135848
1  0.400970  0.303949
2  0.303965  0.030172
3  0.197954  0.103345
4  0.820835  0.118100

```

**代码#3:**

```py
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

print("\nModulo of panel['b']['item1'] with df2['b'] or panel['b']['item2'] using mod() method - \n") 
print("\n", panel['b']['item1'].mod(df2['b'], axis = 0)) 
```

**Output:**

```py
panel['b'] is - 

       item1  item2
0    11.000     10
1     1.025     10
2   333.000     10
3   114.480    110
4  1333.000    110 

Modulo of panel['b']['item1'] with df2['b'] or panel['b']['item2'] using mod() method - 

 0     1.000
1     1.025
2     3.000
3     4.480
4    13.000
dtype: float64

```