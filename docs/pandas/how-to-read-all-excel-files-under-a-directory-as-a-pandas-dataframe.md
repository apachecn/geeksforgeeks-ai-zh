# 如何将一个目录下的所有 excel 文件作为 Pandas DataFrame 读取？

> 原文:[https://www . geeksforgeeks . org/如何阅读所有 excel 文件-目录下作为熊猫-数据框架/](https://www.geeksforgeeks.org/how-to-read-all-excel-files-under-a-directory-as-a-pandas-dataframe/)

在本文中，我们将看到如何将一个文件夹中的所有 Excel 文件读入一个熊猫数据框。首先使用 [glob()](https://www.geeksforgeeks.org/how-to-use-glob-function-to-find-files-recursively-in-python/) 方法查找特定文件夹中的所有 excel 文件，然后使用 [pandas.read_excel()](https://www.geeksforgeeks.org/creating-a-dataframe-using-excel-files/) 方法读取文件，然后显示内容，即可完成任务。

### 方法:

1.  导入必要的 python 包，如 pandas、glob 和 os。
2.  使用 glob python 包来检索与指定模式匹配的文件/路径名。xlsx '
3.  遍历 excel 文件列表，使用 pandas.read_excel()读取该文件。
4.  将每个 excel 文件转换为数据帧。
5.  显示其位置、名称和内容。

下面是实现。

## 蟒 3

```py
# import necessary libraries
import pandas as pd
import os
import glob

# use glob to get all the csv files
# in the folder
path = os.getcwd()
csv_files = glob.glob(os.path.join(path, "*.xlsx"))

# loop over the list of csv files
for f in csv_files:

    # read the csv file
    df = pd.read_excel(f)

    # print the location and filename
    print('Location:', f)
    print('File Name:', f.split("\\")[-1])

    # print the content
    print('Content:')
    display(df)
    print()
```