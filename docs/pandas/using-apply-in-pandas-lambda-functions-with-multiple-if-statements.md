# 在带有多个 if 语句的 Pandas Lambda 函数中使用 Apply

> 原文:[https://www . geesforgeks . org/using-apply-in-pandas-lambda-functions-with-multi-if-statements/](https://www.geeksforgeeks.org/using-apply-in-pandas-lambda-functions-with-multiple-if-statements/)

在本文中，我们将看到如何在[熊猫数据框](https://www.geeksforgeeks.org/python-pandas-dataframe/)中应用带有[λ函数](https://www.geeksforgeeks.org/python-lambda-anonymous-functions-filter-map-reduce/)的多个 if 语句。有时在现实世界中，我们需要对一个数据帧应用多个条件语句，以便为更好的分析准备数据。

我们通常使用 lambda 函数对数据帧应用任何条件，

> **语法:**λ参数:表达式
> 
> 一个匿名函数，我们可以立即传入，而不需要定义名字或者任何类似于传统函数的东西。

当我们使用这个 lambda 函数时，我们只受到一个条件和一个 else 条件的限制。我们不能像真实的 python 代码那样添加多个 if 语句。现在我们可以打破这些限制，看看如何在 lambda 函数中添加多个 if 语句。

### 创建用于演示的数据框架:

## 蟒蛇 3

```py
# Importing the library
import pandas as pd

# dataframe
df = pd.DataFrame({'Name': ['John', 'Jack', 'Shri',
                            'Krishna', 'Smith', 'Tessa'],
                   'Maths': [5, 3, 9, 10, 6, 3]})
print(df)
```

**输出:**

```py
      Name  Maths
0     John      5
1     Jack      3
2     Shri      9
3  Krishna     10
4    Smith      6
5    Tessa      3
```

如果您需要根据学生的分数将他们分为及格或不及格，那么使用 lambda 函数非常简单。

例如，

> **语法:** df['结果'] = df['数学']。应用(λx:“通过”如果 x > =5 否则“失败”)

## 蟒蛇 3

```py
# Import the library
import pandas as pd

# dataframe
df = pd.DataFrame({'Name': ['John', 'Jack', 'Shri',
                            'Krishna', 'Smith', 'Tessa'],
                   'Maths': [5, 3, 9, 10, 6, 3]})

# Adding the result column
df['Result'] = df['Maths'].apply(lambda x: 'Pass' if x>=5 else 'Fail')

print(df)
```