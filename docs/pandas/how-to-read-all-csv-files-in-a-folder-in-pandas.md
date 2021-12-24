# 如何在 Pandas 中读取一个文件夹中的所有 CSV 文件？

> 原文:[https://www . geesforgeks . org/如何阅读熊猫文件夹中的所有 csv 文件/](https://www.geeksforgeeks.org/how-to-read-all-csv-files-in-a-folder-in-pandas/)

在本文中，我们将看到如何将一个文件夹中的所有 CSV 文件读入一个熊猫数据帧。首先使用 [glob()](https://www.geeksforgeeks.org/how-to-use-glob-function-to-find-files-recursively-in-python/) 方法查找特定文件夹中的所有 CSV 文件，然后使用 [pandas.read_csv()](https://www.geeksforgeeks.org/python-read-csv-using-pandas-read_csv/) 方法读取文件，然后显示内容，即可执行任务。

### 方法:

1.  导入必要的 python 包，如 pandas、glob 和 os。
2.  使用 glob python 包来检索与指定模式匹配的文件/路径名。csv '
3.  循环浏览 csv 文件列表，使用 [pandas.read_csv()](https://www.geeksforgeeks.org/python-read-csv-using-pandas-read_csv/) 读取该文件。
4.  将每个 csv 文件转换为数据帧。
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
csv_files = glob.glob(os.path.join(path, "*.csv"))

# loop over the list of csv files
for f in csv_files:

    # read the csv file
    df = pd.read_csv(f)

    # print the location and filename
    print('Location:', f)
    print('File Name:', f.split("\\")[-1])

    # print the content
    print('Content:')
    display(df)
    print()
```