# 熊猫——两列的所有组合

> 原文:[https://www . geeksforgeeks . org/pandas-两列全组合/](https://www.geeksforgeeks.org/pandas-all-combinations-of-two-columns/)

在本文中，我们将看到如何获得数据框的两列的组合。首先，让我们创建一个示例数据帧。

**代码:**使用字典创建数据框的示例代码。

## 蟒 3

```
# importing pandas module for the  
# data frame
import pandas as pd

# creating data frame for student details 
# using dictionary
data = pd.DataFrame({'id': [7058, 7059, ], 
                     'name': ['sravan', 'jyothika']})

print(data)
```