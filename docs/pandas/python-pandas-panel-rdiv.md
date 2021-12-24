# python | panda panel . rdiv()

> 原文:[https://www.geeksforgeeks.org/python-pandas-panel-rdiv/](https://www.geeksforgeeks.org/python-pandas-panel-rdiv/)

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

熊猫`**Panel.rdiv()**`功能用于获取系列和数据框/面板的划分。

> **语法:** Panel.rdiv(其他，轴=0)
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

print("\nDividing panel['b'] with df2['b'] using rdiv() method - \n") 
print("\n", panel['b'].rdiv(df2['b'], axis = 0)) 
```

**Output:**

```
panel['b'] is - 

    item1  item2
0    111    100
1    123    100
2    425    100
3   1333    100

Dividing panel['b'] with df2['b'] using rdiv() method - 

       item1  item2
0  0.900901      1
1  0.813008      1
2  0.235294      1
3  0.075019      1

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

print("\nDividing panel['b'] with df2 using rdiv() method - \n") 
print(panel['b'].rdiv(df2, axis = 0)) 
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
0  0.364764  0.680203
1  0.804920  0.858278
2  0.519905  0.701869
3  0.429503  0.033674
4  0.151454  0.658271

Dividing panel['b'] with df2 using rdiv() method - 

      item1     item2
0  0.033160  0.061837
1  0.785288  0.837344
2  0.001561  0.002108
3  0.003752  0.000294
4  0.000114  0.000494

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

print("\nDividing panel['b']['item1'] with df2['b'] or panel['b']['item2'] using rdiv() method - \n") 
print("\n", panel['b']['item1'].rdiv(df2['b'], axis = 0)) 
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

Dividing panel['b']['item1'] with df2['b'] or panel['b']['item2'] using rdiv() method - 

 0    0.909091
1    9.756098
2    0.030030
3    0.960867
4    0.082521
dtype: float64

```