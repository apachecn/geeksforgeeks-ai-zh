# 如何检查熊猫数据框中的数据类型？

> 原文:[https://www . geesforgeks . org/如何检查熊猫数据类型-数据框/](https://www.geeksforgeeks.org/how-to-check-the-data-type-in-pandas-dataframe/)

熊猫数据框架是一个可变大小和异构表格数据的二维数据结构。Python 中有不同的内置数据类型。用于检查数据类型的两种方法是 [**熊猫。**T3 和](https://www.geeksforgeeks.org/python-pandas-dataframe-dtypes/)[T5 熊猫。DataFrame.select _ dtypes。](https://www.geeksforgeeks.org/python-pandas-dataframe-select_dtypes/)

考虑一个购物商店的数据集，其中包含关于客户序列号、客户名称、所购商品的产品标识、产品成本和购买日期的数据。

## 蟒 3

```
#importing pandas as pd
import pandas as pd

# Create the dataframe 
df = pd.DataFrame({
'Cust_No': [1,2,3],
'Cust_Name': ['Alex', 'Bob', 'Sophie'],
'Product_id': [12458,48484,11311],
'Product_cost': [65.25, 25.95, 100.99],
'Purchase_Date': [pd.Timestamp('20180917'),
                  pd.Timestamp('20190910'),
                  pd.Timestamp('20200610')]
})

# Print the dataframe 
df
```