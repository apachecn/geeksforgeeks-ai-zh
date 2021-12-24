# 将大型熊猫数据帧分割成较小数据帧的列表

> 原文:[https://www . geeksforgeeks . org/split-大熊猫-data frame-to-list-of-small-data frame/](https://www.geeksforgeeks.org/split-large-pandas-dataframe-into-list-of-smaller-dataframes/)

在本文中，我们将了解如何将大型数据帧拆分成较小数据帧的列表。这主要可以通过两种不同的方式完成:

1.  By using

的 groupby 概念拆分每一行*   在这里，我们使用一个小的数据框架来轻松理解这个概念，这也可以用一种简单的方式来实现。数据框由学生证、姓名、分数和成绩组成。让我们创建数据帧。

    ## 蟒 3

    ```py
    # importing packages
    import pandas as pd

    # dictionary of data
    dct = {'ID': {0: 23, 1: 43, 2: 12,
                  3: 13, 4: 67, 5: 89,
                  6: 90, 7: 56, 8: 34},

           'Name': {0: 'Ram', 1: 'Deep',
                    2: 'Yash', 3: 'Aman',
                    4: 'Arjun', 5: 'Aditya',
                    6: 'Divya', 7: 'Chalsea',
                    8: 'Akash'},

           'Marks': {0: 89, 1: 97, 2: 45, 3: 78,
                     4: 56, 5: 76, 6: 100, 7: 87,
                     8: 81},

           'Grade': {0: 'B', 1: 'A', 2: 'F', 3: 'C',
                     4: 'E', 5: 'C', 6: 'A', 7: 'B',
                     8: 'B'}
           }

    # create dataframe
    df = pd.DataFrame(dct)

    # view dataframe
    df
    ```