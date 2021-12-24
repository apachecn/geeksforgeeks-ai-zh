# python | panda panel . rml()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-pandas-panel-rml/

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

熊猫`**Panel.rmul()**`函数用于获取数列和数据框/面板的乘积。

> **语法:** Panel.rmul(其他，轴=0)
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

print("\nMultiplying panel['b'] with df2['b'] using rmul() method - \n") 
print("\n", panel['b'].rmul(df2['b'], axis = 0)) 
```

**Output:**

```
panel['b'] is - 

    item1  item2
0    111    100
1    123    100
2    425    100
3   1333    100

Multiplying panel['b'] with df2['b'] using rmul() method - 

     item1  item2
0   11100  10000
1   12300  10000
2   42500  10000
3  133300  10000

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

print("\nMultiplying panel['b'] with df2 using rmul() method - \n") 
print(panel['b'].rmul(df2, axis = 0)) 
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
0  0.549490  0.658451
1  0.321557  0.139482
2  0.010817  0.775445
3  0.011675  0.333828
4  0.818014  0.462602

Multiplying panel['b'] with df2 using rmul() method - 

         item1       item2
0     6.044385    7.242957
1     0.329596    0.142969
2     3.602168  258.223060
3     1.336504   38.216583
4  1090.412087  616.648529

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

print("\nMultiplying panel['b']['item1'] with df2['b'] or panel['b']['item2'] using rmul() method - \n") 
print("\n", panel['b']['item1'].rmul(df2['b'], axis = 0)) 
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

Multiplying panel['b']['item1'] with df2['b'] or panel['b']['item2'] using rmul() method - 

 0       110.00
1        10.25
2      3330.00
3     12592.80
4    146630.00
dtype: float64

```