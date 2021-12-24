# 大熊猫的绝对和相对频率

> 原文:[https://www . geesforgeks . org/绝对和相对频率熊猫/](https://www.geeksforgeeks.org/absolute-and-relative-frequency-in-pandas/)

**频率**是给定样本中结果出现的次数。它可以用两种不同的方式来描述。

**1。绝对频率:**
是某一特定类别的观测次数。它总是有一个整数值，或者我们可以说它有离散值。

**示例:**

> 下列数据是关于学生在一个班级举行的数学考试中的及格或不及格。
> `P, P, F, P, F, P, P, F, F, P, P, P`
> 
> 其中，P =通过，F =失败。
> 
> **解法:**
> 从给定的数据我们可以说，
> 有 8 名学生通过了考试
> 有 4 名学生没有通过考试

**Python 中的实现:**
让我们把 12 个人在两个类别中声明通过(P)和失败(F)的结果分别归类为 1 和 0。

```py
P, P, F, P, F, P, P, F, F, P, P, P
1, 1, 0, 1, 0, 1, 1, 0, 0, 1, 1, 1

```

```py
import pandas as pd

data = [1, 1, 0, 1, 0, 1, 1, 0, 0, 1, 1, 1]

# Create Data Frame using pandas library
# .value_counts() counts the number of 
# occurrences of particular observation

df = pd.Series(data).value_counts()
print(df)
```

**Output:**

```py
1    8
0    4
dtype: int64

```

**2。相对频率:**
它是给定数据集中特定类别的观测值的分数。它有浮动值，也用百分比表示。让我们考虑给定的数学考试及格和不及格学生的例子。然后，

> 及格学生相对频率= 8 / ( 8 + 4 ) = 0.666 = 66.6 %
> 不及格学生相对频率= 4 / ( 8 + 4 ) = 0.333 = 33.3 %

```py
import pandas as pd

data = [1, 1, 0, 1, 0, 1, 1, 0, 0, 1, 1, 1]

# Create Data Frame using pandas library
# .value_counts() counts the number of 
# occurrences of particular observation

df = pd.Series(data).value_counts()      
print(df / len(data))
```

**Output:**

```py
1    0.666667
0    0.333333
dtype: float64

```