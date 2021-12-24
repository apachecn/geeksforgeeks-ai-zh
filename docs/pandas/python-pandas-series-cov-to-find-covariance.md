# Python | Pandas Series.cov()查找协方差

> 原文:[https://www . geesforgeks . org/python-pandas-series-cov-to-find-协方差/](https://www.geeksforgeeks.org/python-pandas-series-cov-to-find-covariance/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫**级数. cov()** 用于求两个级数的协方差。在下面的例子中，使用熊猫方法和手动方法找到协方差，然后比较答案。

要了解更多关于协方差的信息，请点击这里的[。](https://www.geeksforgeeks.org/program-find-covariance/)

> **语法:** Series.cov(other，min_periods=None)
> **参数:**
> **other:** 用于寻找协方差的其他系列
> **min_periods:** 获得有效结果的最小观察数
> **返回类型:**浮点值，返回调用方系列和传递系列的协方差

**示例:**
在本例中，使用 Pandas 制作了两个列表并将其转换为系列。Series()方法。如果找到了两个系列的平均值，并创建了一个函数来手动查找协方差。熊猫。cov()也被应用，两种方式的结果都存储在变量中，并打印出来以比较输出。

## 蟒蛇 3

```py
import pandas as pd

# list  1
a = [2, 3, 2.7, 3.2, 4.1]

# list 2
b = [10, 14, 12, 15, 20]

# storing average of a
av_a = sum(a)/len(a)

# storing average of b
av_b = sum(b)/len(b)

# making series from list a
a = pd.Series(a)

# making series from list b
b = pd.Series(b)

# covariance through pandas method
covar = a.cov(b)

# finding covariance manually
def covarfn(a, b, av_a, av_b):
    cov = 0

    for i in range(0, len(a)):
        cov += (a[i] - av_a) * (b[i] - av_b)
    return (cov / (len(a)-1))

# calling function
cov = covarfn(a, b, av_a, av_b)

# printing results
print("Results from Pandas method: ", covar)
print("Results from manual function method: ", cov)
```

**输出:**

从输出中可以看出，两种方式的输出是相同的。因此，这种方法在寻找大序列的协方差时是有用的。

```py
Results from Pandas method:  2.8499999999999996
Results from manual function method:  2.8499999999999996
```