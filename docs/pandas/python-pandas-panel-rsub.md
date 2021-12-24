# python | panda panel . rsub()

> 原文:[https://www.geeksforgeeks.org/python-pandas-panel-rsub/](https://www.geeksforgeeks.org/python-pandas-panel-rsub/)

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

熊猫 `**Panel.rsub()**`功能用于获取数列和数据框/面板的减法。

> **语法:** Panel.rsub(其他，轴=0)
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

print("\nSubtracting panel['b'] with df2['b'] using rsub() method - \n") 
print("\n", panel['b'].rsub(df2['b'], axis = 0)) 
```

**Output:**

```
panel['b'] is - 

    item1  item2
0    111    100
1    123    100
2    425    100
3   1333    100

Subtracting panel['b'] with df2['b'] using rsub() method - 

    item1  item2
0    -11      0
1    -23      0
2   -325      0
3  -1233      0

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

print("\nSubtracting panel['b'] with df2 using rsub() method - \n") 
print(panel['b'].rsub(df2, axis = 0)) 
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
0  0.159943  0.383040
1  0.769608  0.776670
2  0.038762  0.889516
3  0.672955  0.094725
4  0.127130  0.729699

Subtracting panel['b'] with df2 using rsub() method - 

         item1        item2
0   -10.840057   -10.616960
1    -0.255392    -0.248330
2  -332.961238  -332.110484
3  -113.807045  -114.385275
4 -1332.872870 -1332.270301

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

print("\nSubtracting panel['b']['item1'] with df2['b'] or panel['b']['item2'] using rsub() method - \n") 
print("\n", panel['b']['item1'].rsub(df2['b'], axis = 0)) 
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

Subtracting panel['b']['item1'] with df2['b'] or panel['b']['item2'] using rsub() method - 

 0      -1.000
1       8.975
2    -323.000
3      -4.480
4   -1223.000
dtype: float64

```