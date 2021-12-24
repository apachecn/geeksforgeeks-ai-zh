# 如何使用 Concat 联合熊猫数据帧？

> 原文:[https://www . geesforgeks . org/how-union-pandas-data frames-using-concat/](https://www.geeksforgeeks.org/how-to-union-pandas-dataframes-using-concat/)

**concat()** 函数执行所有重的提升操作，沿着一个轴执行连接操作，同时在其他轴上执行索引(如果有)的可选设置逻辑(并集或交集)。

concat()函数以两种方式之一组合数据帧:

*   **堆叠:轴= 0(这是默认选项)。**

![](img/86502d2bb59d910cb8815059f97b56cb.png)

轴=0

*   **并排:轴= 1**

![](img/08bbe8da0b1d16eb48144afd3ca9b710.png)

轴=1

**使用 Concat 联合熊猫数据帧的步骤:**

*   **创建第一个数据框**

## 蟒蛇 3

```
import pandas as pd

students1 = {'Class': ['10','10','10'],
            'Name': ['Hari','Ravi','Aditi'],
            'Marks': [80,85,93]
           }

df1 = pd.DataFrame(students1, columns= ['Class','Name','Marks'])

df1
```

**输出:**

![](img/4dcdf7b18b9d02981575225792452bdf.png)

*   **创建第二个数据框**

## 蟒蛇 3

```
import pandas as pd

students2 = {'Class': ['10','10','10'],
            'Name': ['Tanmay','Akshita','Rashi'],
            'Marks': [89,91,87]
           }

df2 = pd.DataFrame(students2, 
                   columns= ['Class','Name','Marks'])

df2
```

**输出:**

![](img/e6e696c4bd015a647e42dbf272c88bfc.png)

*   **使用 Concat** 联合熊猫数据帧

## 蟒蛇 3

```
pd.concat([df1,df2])
```

**输出:**

![](img/ffed4db98dc3891e915e8107fe823e75.png)

**注意:**您需要在所有数据帧中保持相同的列名，以避免任何“NaN”值。