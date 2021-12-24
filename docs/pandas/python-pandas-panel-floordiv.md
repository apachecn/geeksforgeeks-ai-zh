# Python | Pandas panel . floor div()

> 原文:[https://www.geeksforgeeks.org/python-pandas-panel-floordiv/](https://www.geeksforgeeks.org/python-pandas-panel-floordiv/)

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

熊猫中`**Panel.floordiv()**`函数用于获取数列和数据框/面板的整数除法。

> **语法:** Panel.floordiv(其他，轴=0)
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

print("\nInteger Dividing panel['b'] with df2['b'] using floordiv() method - \n") 
print("\n", panel['b'].floordiv(df2['b'], axis = 0)) 
```

**Output:**

```
panel['b'] is - 

    item1  item2
0    111    100
1    123    100
2    425    100
3   1333    100

Integer Dividing panel['b'] with df2['b'] using floordiv() method - 

    item1  item2
0      1      1
1      1      1
2      4      1
3     13      1

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

print("\nInteger Dividing panel['b'] with df2 using floordiv() method - \n") 
print(panel['b'].floordiv(df2, axis = 0)) 
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
0  0.346012  0.135318
1  0.850487  0.589151
2  0.074627  0.742770
3  0.296359  0.417620
4  0.216676  0.682704

Integer Dividing panel['b'] with df2 using floordiv() method - 

   item1  item2
0     31     81
1      1      1
2   4462    448
3    386    274
4   6152   1952

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

print("\nInteger Dividing panel['b']['item1'] with df2['b'] or panel['b']['item2'] using floordiv() method - \n") 
print("\n", panel['b']['item1'].floordiv(df2['b'], axis = 0)) 
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

Integer Dividing panel['b']['item1'] with df2['b'] or panel['b']['item2'] using floordiv() method - 

 0     1
1     0
2    33
3     1
4    12
dtype: float64

```