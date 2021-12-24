# Python | Pandas Series.str .大写()

> 原文:[https://www . geesforgeks . org/python-pandas-series-str-大写/](https://www.geeksforgeeks.org/python-pandas-series-str-capitalize/)

**series . str . capital()**用于将熊猫系列中的字符串元素大写。Series 是一种数据结构，在 python 中与 list 一样使用。系列可以包含不同类型的数据，就像我们想在系列列表中输入的那样。

> **语法:** Series.str .大写()
> 
> **参数:**无
> 
> **返回:**系列/对象索引

要获得 csv 文件的链接，点击 [nba.csv](https://media.geeksforgeeks.org/wp-content/uploads/nba.csv)

**代码#1 :**
我们正在使用熊猫`**Series.str.capitalize()**`方法，该方法有助于将给定系列的第一个字母*转换为大写字母*，其余所有字符在特定字符串中保持不变。

```
import pandas as pd

data = pd.read_csv("nba.csv")

g = pd.Series(data['Name'].head())
print(g.str.lower(), end ='\n\n')
print(g.str.capitalize())
```

**Output:**As we have explained that only first letter should be capitalize rest of all should be same. As you can see the output given below.

```
     Before

0    avery bradley
1      jae crowder
2     john holland
3      r.j. hunter
4    jonas jerebko
Name: Name, dtype: object

     After

0    Avery bradley
1      Jae crowder
2     John holland
3      R.j. hunter
4    Jonas jerebko
Name: Name, dtype: object

```

**代码#2 :**

```
import pandas as pd

data = pd.read_csv("nba.csv")

g = pd.Series(data['Team'].head())
print(g.str.lower(), end ='\n\n')
print(g.str.capitalize())
```

**Output:**

```
     Before

0    boston celtics
1    boston celtics
2    boston celtics
3    boston celtics
4    boston celtics
Name: Team, dtype: object

     After

0    Boston celtics
1    Boston celtics
2    Boston celtics
3    Boston celtics
4    Boston celtics
Name: Team, dtype: object

```