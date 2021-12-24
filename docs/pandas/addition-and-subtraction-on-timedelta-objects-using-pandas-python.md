# 使用熊猫 Python 对时间增量对象进行加减运算

> 原文:[https://www . geeksforgeeks . org/time delta 加减运算-对象-使用-pandas-python/](https://www.geeksforgeeks.org/addition-and-subtraction-on-timedelta-objects-using-pandas-python/)

**TimeDelta** 模块用于表示熊猫模块中的时间，可以有多种使用方式。执行像**加法**和**减法**这样的操作对于每种语言都非常重要，但是在日期和时间上执行这些任务可能非常有价值。

**对时间增量数据帧或系列的操作–**

**1)添加–**

```
df['Result'] = df['TimeDelta1'] + df['TimeDelta2']
```

**2)减法–**

```
df['Result'] = df['TimeDelta1'] - df['TimeDelta2']
```

**返回:**执行操作后返回数据帧。

**示例#1 :**

在这个例子中，我们可以看到，通过对日期和时间使用各种**操作，我们能够对具有时间增量对象值的数据帧进行加减运算。**

## 蟒蛇 3

```
# import pandas and numpy
import pandas as pd
import numpy as np

# Perform addition operation
a = pd.Series(pd.date_range('2020-8-10', periods=5, freq='D'))
b = pd.Series([pd.Timedelta(days=i) for i in range(5)])

gfg = pd.DataFrame({'A': a, 'B': b})
gfg['Result'] = gfg['A'] + gfg['B']

print(gfg)
```

**输出:**

> 最佳结果
> 
> 0 2020-08-10 0 天 2020-08-10
> 
> 1 2020-08-11 1 天 2020-08-12
> 
> 2 2020-08-12 2 天 2020-08-14
> 
> 3 2020-08-13 3 天 2020-08-16
> 
> 2020-08-14 4 天 2020-08-18

**例 2 :**

## 蟒蛇 3

```
# import pandas and numpy
import pandas as pd
import numpy as np

# Perform addition operation
a = pd.Series(pd.date_range('2020-8-10', periods=4, freq='D'))
b = pd.Series([pd.Timedelta(days=i) for i in range(4)])

gfg = pd.DataFrame({'A': a, 'B': b})
gfg['Result'] = gfg['A'] - gfg['B']

print(gfg)
```

**输出:**

> 最佳结果
> 
> 0 2020-08-10 0 天 2020-08-10
> 
> 1 2020-08-11 1 天 2020-08-10
> 
> 2 2020-08-12 2 天 2020-08-10
> 
> 3 2020-08-13 3 天 2020-08-10