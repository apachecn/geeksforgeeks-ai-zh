# 使用字典从列表中创建熊猫数据框

> 原文:[https://www . geesforgeks . org/create-pandas-data frame-from-list-use-dictionary/](https://www.geeksforgeeks.org/create-pandas-dataframe-from-lists-using-dictionary/)

使用字典从列表中创建熊猫数据框可以通过多种方式实现。

**方法#1:** 利用大熊猫。数据帧

通过熊猫中的这个方法，我们可以将一个列表字典转换成一个数据帧。

```py
# importing pandas as pd
import pandas as pd

# dictionary of lists
dict = {'name':["aparna", "pankaj", "sudhir", "Geeku"],
        'degree': ["MBA", "BCA", "M.Tech", "MBA"],
        'score':[90, 40, 80, 98]}

df = pd.DataFrame(dict)

df
```

**输出:**
![](img/2f2e3bba7b7702ba1b448fd853add3b5.png)

**方法#2:** 使用 from_dict()函数。

```py
# importing pandas as pd
import pandas as pd

# dictionary of lists
dict = {'name':["aparna", "pankaj", "sudhir", "Geeku"],
        'degree': ["MBA", "BCA", "M.Tech", "MBA"],
        'score':[90, 40, 80, 98]}

df = pd.DataFrame.from_dict(dict)

df
```

**输出:**
![](img/2f2e3bba7b7702ba1b448fd853add3b5.png)
通过使用这个函数，我们在排列数据时获得了一些灵活性，比如数据的方向、数据类型和列的名称都可以作为参数输入函数中。