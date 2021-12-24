# python | panda panel . mul()

> 原文:[https://www.geeksforgeeks.org/python-pandas-panel-mul/](https://www.geeksforgeeks.org/python-pandas-panel-mul/)

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

熊猫`**Panel.mul()**`函数用于获取数列和数据框/面板的乘积。

> **语法:** Panel.mul(其他，轴=0)
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

print("\nMultiplying panel['b'] with df2['b'] using mul() method - \n") 
print("\n", panel['b'].mul(df2['b'], axis = 0)) 
```

**输出:**
![](img/96631a871a8c3f3a764537c40fd53552.png)

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

print("\nMultiplying panel['b'] with df2 using mul() method - \n") 
print(panel['b'].mul(df2, axis = 0)) 
```

**输出:**
![](img/aac4df2a8515b2dd1c9ef50b0d92e8ef.png)

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

print("\nMultiplying panel['b']['item1'] with df2['b'] or panel['b']['item2'] using mul() method - \n") 
print("\n", panel['b']['item1'].mul(df2['b'], axis = 0)) 
```

**输出:**
![](img/aeb9c6c5f05d8ec004f2c0f9ae59b984.png)