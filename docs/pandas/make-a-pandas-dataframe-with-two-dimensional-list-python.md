# 用二维列表制作熊猫数据框| Python

> 原文:[https://www . geeksforgeeks . org/make-a-pandas-data frame-with-二维列表-python/](https://www.geeksforgeeks.org/make-a-pandas-dataframe-with-two-dimensional-list-python/)

众所周知，Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

熊猫数据框可以通过多种方式实现。在本文中，我们将学习如何使用二维列表创建数据框架。

**示例#1:**

```py
# import pandas as pd 
import pandas as pd  

# List1  
lst = [['Geek', 25], ['is', 30], 
       ['for', 26], ['Geeksforgeeks', 22]] 

# creating df object with columns specified    
df = pd.DataFrame(lst, columns =['Tag', 'number']) 
print(df )
```

**输出:**

```py
             Tag  number
0           Geek      25
1             is      30
2            for      26
3  Geeksforgeeks      22
```

**例 2:**

```py
import pandas as pd  

# List1  
lst = [['tom', 'reacher', 25], ['krish', 'pete', 30], 
       ['nick', 'wilson', 26], ['juli', 'williams', 22]] 

df = pd.DataFrame(lst, columns =['FName', 'LName', 'Age'],
                                           dtype = float) 
print(df)
```

**输出:**

```py
   FName     LName  Age
0    tom   reacher   25
1  krish      pete   30
2   nick    wilson   26
3   juli  williams   22

```