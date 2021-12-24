# 如何获取熊猫数据框中的行/索引名

> 原文:[https://www . geesforgeks . org/how-to-rows-index-in-names-pandas-data frame/](https://www.geeksforgeeks.org/how-to-get-rows-index-names-in-pandas-dataframe/)

在分析实际数据集时，这些数据集的大小通常非常大，我们可能需要获取行或索引名称，以便执行某些特定的操作。

我们来讨论一下如何在熊猫[数据框](https://www.geeksforgeeks.org/python-pandas-dataframe/)中获取行名。

首先，让我们用`nba.csv`创建一个简单的数据框

## 蟒蛇 3

```
# Import pandas package 
import pandas as pd 

# making data frame 
data = pd.read_csv("https://media.geeksforgeeks.org/wp-content/uploads/nba.csv") 

# calling head() method  
# storing in new variable 
data_top = data.head(10) 

# display 
data_top 
```

![](img/06914b348805281845da4373b7453834.png)

现在让我们尝试从上面的数据集获取行名。

**方法#1:** 简单地迭代索引

## 蟒蛇 3

```
# Import pandas package 
import pandas as pd 

# making data frame 
data = pd.read_csv("nba.csv") 

# calling head() method  
# storing in new variable 
data_top = data.head() 

# iterating the columns
for row in data_top.index:
    print(row, end = " ")
```

**输出:**

```
0 1 2 3 4 5 6 7 8 9 
```

**方法#2:** 使用带有数据框对象的行

## 蟒蛇 3

```
# Import pandas package 
import pandas as pd 

# making data frame 
data = pd.read_csv("nba.csv") 

# calling head() method  
# storing in new variable 
data_top = data.head() 

# list(data_top) or
list(data_top.index)
```