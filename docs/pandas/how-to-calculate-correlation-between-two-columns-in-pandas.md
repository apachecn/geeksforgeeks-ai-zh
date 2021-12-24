# 如何计算熊猫两栏的相关性？

> 原文:[https://www . geeksforgeeks . org/如何计算两栏熊猫之间的相关性/](https://www.geeksforgeeks.org/how-to-calculate-correlation-between-two-columns-in-pandas/)

在这篇文章中，我们将讨论如何计算大熊猫两栏之间的相关性

**相关性**用于总结两个定量变量之间线性关联的强弱和方向。它由 r 和介于-1 和+1 之间的值表示。r 的正值表示正关联，r 的负值表示负关联。

通过使用 [corr()](https://www.geeksforgeeks.org/python-pandas-dataframe-corr/) 函数，我们可以得到数据框中两列之间的相关性。

**语法**:

> dataframe['first_column']。corr(data frame[' second _ column '])

哪里，

*   数据帧是输入数据帧
*   first_column 与数据帧的 second_column 相关

### **例 1** : Python 程序获取两列之间的相关性

## 蟒蛇 3

```py
# import pandas module
import pandas as pd

# create dataframe with 3 columns
data = pd.DataFrame({
    "column1": [12, 23, 45, 67],
    "column2": [67, 54, 32, 1],
    "column3": [34, 23, 56, 23]
}
)
# display dataframe
print(data)

# correlation between column 1 and column2
print(data['column1'].corr(data['column2']))

# correlation between column 2 and column3
print(data['column2'].corr(data['column3']))

# correlation between column 1 and column3
print(data['column1'].corr(data['column3']))
```

**输出:**

```py
 column1  column2  column3
0       12       67       34
1       23       54       23
2       45       32       56
3       67        1       23
-0.9970476685163736
0.07346999975265099
0.0
```

仅使用 corr()函数也可以获得数值列的元素相关性。

**语法:**

```py
dataset.corr()
```

### **例 2** :获取元素相关性

## 蟒蛇 3

```py
# import pandas module
import pandas as pd

# create dataframe with 3 columns
data = pd.DataFrame({
    "column1": [12, 23, 45, 67],
    "column2": [67, 54, 32, 1],
    "column3": [34, 23, 56, 23]
}
)
# get correlation between element wise
print(data.corr())
```

**输出**:

```py
          column1   column2  column3
column1  1.000000 -0.997048  0.00000
column2 -0.997048  1.000000  0.07347
column3  0.000000  0.073470  1.00000
```