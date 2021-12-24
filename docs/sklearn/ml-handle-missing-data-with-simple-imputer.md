# ML |用简单估算器处理缺失数据

> 原文:[https://www . geeksforgeeks . org/ml-handle-missing-data-with-simple-import/](https://www.geeksforgeeks.org/ml-handle-missing-data-with-simple-imputer/)

**简单估算器**是一个 scikit-learn 类，有助于处理预测模型数据集中缺失的数据。它用指定的占位符替换 NaN 值。
通过使用**简单估算器()**方法实现，该方法采用以下参数:

> **缺失值**:需要输入的缺失值占位符。默认为*NaN*
> T5 策略:从数据集中替换 NaN 值的数据。策略参数可以取值——“平均值”(默认值)、“中位数”、“最频繁”和“常数”。
> **fill_value** :使用常量策略赋予 NaN 数据的常量值。

**代码:说明 SimpleImputer 类使用的 Python 代码。**

## 蟒蛇 3

```py
import numpy as np

# Importing the SimpleImputer class
from sklearn.impute import SimpleImputer

# Imputer object using the mean strategy and
# missing_values type for imputation
imputer = SimpleImputer(missing_values = np.nan,
                        strategy ='mean')

data = [[12, np.nan, 34], [10, 32, np.nan],
        [np.nan, 11, 20]]

print("Original Data : \n", data)
# Fitting the data to the imputer object
imputer = imputer.fit(data)

# Imputing the data    
data = imputer.transform(data)

print("Imputed Data : \n", data)
```

**输出**T2】

```py
Original Data : 

[[12, nan, 34]
[10, 32, nan]
[nan, 11, 20]]

Imputed Data : 

[[12, 21.5, 34]
[10, 32, 27]
[11, 11, 20]]
```

**记住:沿着矩阵的列**取平均值或中值