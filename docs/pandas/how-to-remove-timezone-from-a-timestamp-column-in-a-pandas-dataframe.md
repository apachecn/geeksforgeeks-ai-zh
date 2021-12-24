# 如何从熊猫数据框的时间戳列中删除时区

> 原文:[https://www . geesforgeks . org/如何从时间戳中删除时区-熊猫中的列-数据框/](https://www.geeksforgeeks.org/how-to-remove-timezone-from-a-timestamp-column-in-a-pandas-dataframe/)

世界分为 24 个时区。我们都知道不同的时区是必需的，因为整个地球不是同时被照亮的。虽然在许多情况下，我们可能不需要时区，尤其是当数据驻留在某个位置甚至本地系统的公共服务器上时。在本文中，我们将看到如何从熊猫数据帧的时间戳列中删除时区。

**为**演示创建数据框**:**

## Python

```py
import pandas as pd
from datetime import datetime, timezone

# CREATE THE PANDAS DATAFRAME
# WITH TIMESTAMP COLUMN
df = pd.DataFrame({
    "orderNo": [
        "4278954",
        "3473895",
        "8763762",
        "4738289",
        "1294394"
    ],
    "timestamp": [
        datetime.strptime("2021-06-01",
                          "%Y-%m-%d").replace(tzinfo=timezone.utc),
        datetime.strptime("2021-06-02",
                          "%Y-%m-%d").replace(tzinfo=timezone.utc),
        datetime.strptime("2021-06-03",
                          "%Y-%m-%d").replace(tzinfo=timezone.utc),
        datetime.strptime("2021-06-04",
                          "%Y-%m-%d").replace(tzinfo=timezone.utc),
        datetime.strptime("2021-06-05",
                          "%Y-%m-%d").replace(tzinfo=timezone.utc)
    ]
})

# PRINT THE DATATYPES OF
# EACH COLUMN OF DATAFRAME
print(df.dtypes)

# VIEW THE DATAFRAME
print(df)
```