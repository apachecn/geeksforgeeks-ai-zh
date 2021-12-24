# 蟒蛇|熊猫系列. abs()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-abs/](https://www.geeksforgeeks.org/python-pandas-series-abs/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。
熊猫 **Series.abs()** 方法用于获取 Series/DataFrame 中每个元素的绝对数值。

> **语法:** Series.abs()
> **参数:**无参数
> **返回:**返回包含每个元素绝对值的 Series 或 DataFrame。

**代码#1:**

## 蟒蛇 3

```
# importing pandas module
import pandas as pd

# creating lists
lst = [2, -10.87, -3.14, 0.12]
lst2 = [-10.87 + 4j]

ser = pd.Series(lst)
ser1 = pd.Series(lst2)

# printing values explaining abs()
print(ser1.abs(), '\n\n', ser.abs())
```

**输出:**

```
0    11.582612
dtype: float64 

 0     2.00
1    10.87
2     3.14
3     0.12
dtype: float64
```

**代码#2:** 解释 abs()在特定行
上的使用

## 蟒蛇 3

```
# importing pandas module
import pandas as pd

df = pd.DataFrame({'Name': ['John', 'Hari', 'Peter', 'Loani'],
                  'Age': [31, 29, 57, 40],
                  'val': [98, 48, -80, -14]})

df['ope'] = (df.val - 87).abs()

df
```

**输出:**

```
Name    Age    val    ope
0    John    31    98    11
1    Hari    29    48    39
2    Peter    57    -80    167
3    Loani    40    -14    101
```