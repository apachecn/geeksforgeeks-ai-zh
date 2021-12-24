# 使用熊猫数据框中的 for 循环创建一个列

> 原文:[https://www . geesforgeks . org/create-a-column-for-loop-in-pandas-data frame/](https://www.geeksforgeeks.org/create-a-column-using-for-loop-in-pandas-dataframe/)

让我们看看如何使用 for 循环在 pandas dataframe 中创建一个列。当我们需要处理之前为此目的创建的数据帧的数据时，有时需要这样的操作，我们需要这种类型的计算，这样我们就可以处理现有的数据，并创建一个单独的列来存储数据。

在这种类型的计算中，我们需要注意现有数据帧中的值。我们只使用这些值在 dataframe 中添加新列。

```py
# importing pandas
import pandas as pd

# Creating new dataframe
initial_data = {'First_name': ['Ram', 'Mohan', 'Tina', 'Jeetu', 'Meera'], 
                'Last_name': ['Kumar', 'Sharma', 'Ali', 'Gandhi', 'Kumari'], 
                'Marks': [12, 52, 36, 85, 23] }

df = pd.DataFrame(initial_data, columns = ['First_name', 'Last_name', 'Marks'])

# Generate result using pandas
result = []
for value in df["Marks"]:
    if value >= 33:
        result.append("Pass")
    elif value < 0 and value > 100:
        result.append("Invalid")
    else:
        result.append("Fail")

df["Result"] = result   
print(df)
```

**输出:**

```py
  First_name Last_name  Marks Result
0        Ram     Kumar     12   Fail
1      Mohan    Sharma     52   Pass
2       Tina       Ali     36   Pass
3      Jeetu    Gandhi     85   Pass
4      Meera    Kumari     23   Fail

```