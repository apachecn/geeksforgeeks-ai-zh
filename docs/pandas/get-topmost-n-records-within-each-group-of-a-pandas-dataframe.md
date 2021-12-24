# 在熊猫数据框的每一组中获取最高的 N 条记录

> 原文:[https://www . geesforgeks . org/get-top-n-records-in-每组熊猫-dataframe/](https://www.geeksforgeeks.org/get-topmost-n-records-within-each-group-of-a-pandas-dataframe/)

首先，熊猫数据框以表格的形式存储数据。在某些情况下，我们需要根据某些条件从数据帧中检索数据。例如，如果我们想要获得每组数据帧的前 N 条记录。这里我们将使用熊猫的 **Groupby()** 功能对列进行分组。所以我们可以这样做:

首先，我们创建了一个熊猫数据框:

```
#importing pandas as pd
import pandas as pd

#creating dataframe
df=pd.DataFrame({ 'Variables': ['A','A','A','A','B','B',
                                'B','C','C','C','C'],
                 'Value': [2,5,0,3,1,0,9,0,7,5,4]})
df
```