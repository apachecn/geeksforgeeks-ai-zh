# 计算熊猫系列每个唯一值的频率计数

> 原文:[https://www . geeksforgeeks . org/计算熊猫每个独特价值的频率计数系列/](https://www.geeksforgeeks.org/calculate-the-frequency-counts-of-each-unique-value-of-a-pandas-series/)

让我们看看如何找到熊猫系列的每个唯一值的频率计数。我们将使用 [value_counts()](https://www.geeksforgeeks.org/python-pandas-series-value_counts/) 函数来执行此任务。

**例 1 :**

```py
# importing the module
import pandas as pd

# creating the series
s = pd.Series(data = [2, 3, 4, 5, 5, 6, 
                      7, 8, 9, 5, 3])

# displaying the series
print(s)

# finding the unique count
print(s.value_counts())
```

**输出:**
![](img/1313642f26a917b2d3314a73d9a8bea8.png)

**输出:**
![](img/1cd18dc5ea3e563168dcbc4092841ce8.png)

**例 2 :**

```py
# importing the module
import pandas as pd

# creating the series
s = pd.Series(np.take(list('0123456789'), 
              np.random.randint(10, size = 40)))

# displaying the series
print(s)

# finding the unique count
s.value_counts()
```

**输出:**
![](img/90d860ee0d745d04069283583ed39c48.png)

**输出:**
![](img/cfc3d2b47981264423efff9c232bc789.png)

**例 3 :**

```py
# importing pandas as pd 
import pandas as pd 

# creating the Series 
sr = pd.Series(['Mumbai', 'Pune', 'Agra', 'Pune', 
                'Goa', 'Shimla', 'Goa', 'Pune']) 

# displaying the series 
print(sr) 

# finding the unique count
sr.value_counts()
```

**输出:**
![](img/13f1af622945c481af7ac38f7a2f0c14.png)

![](img/5a1fce09e91b4d8f1b77a1cce01e9b42.png)