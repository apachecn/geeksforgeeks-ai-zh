# 如何将熊猫转换为 PySpark 数据帧？

> 原文:[https://www . geesforgeks . org/如何将熊猫转换为 pyspark-dataframe/](https://www.geeksforgeeks.org/how-to-convert-pandas-to-pyspark-dataframe/)

在本文中，我们将学习如何将熊猫转换为 PySpark 数据帧。有时我们会得到 csv、xlsx 等。格式化数据，我们必须将其存储在 PySpark 数据帧中，这可以通过将数据加载到 Pandas 中，然后转换为 PySpark 数据帧来完成。为了进行转换，我们将熊猫数据帧传递给 CreateDataFrame()方法。

> ***语法:** spark.createDataframe(数据，架构)*
> 
> ***参数:***
> 
> *   *Data–Create a list of values for the data frame.*
> *   *Schema-a list of data set structures or column names.*
> 
> *这里的火花就是 SparkSession 对象。*

**示例 1:创建一个数据帧，然后使用 spark.createDataFrame()方法进行转换**

## python 3

```py
# import the pandas
import pandas as pd

# from  pyspark library import 
# SparkSession
from pyspark.sql import SparkSession

# Building the SparkSession and name
# it :'pandas to spark'
spark = SparkSession.builder.appName(
  "pandas to spark").getOrCreate()

# Create the DataFrame with the help 
# of pd.DataFrame()
data = pd.DataFrame({'State': ['Alaska', 'California',
                               'Florida', 'Washington'],

                     'city': ["Anchorage", "Los Angeles", 
                              "Miami", "Bellevue"]})

# create DataFrame
df_spark = spark.createDataFrame(data)

df_spark.show()
```