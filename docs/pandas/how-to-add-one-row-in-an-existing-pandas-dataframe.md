# 如何在现有熊猫数据框中添加一行？

> 原文:[https://www . geesforgeks . org/如何在现有熊猫中添加一行-数据框/](https://www.geeksforgeeks.org/how-to-add-one-row-in-an-existing-pandas-dataframe/)

在本文中，我们将看到如何向现有的数据框中添加新的值行。当我们想要在数据中插入一个我们之前可能没有添加的新条目时，可以使用它。实现这一点有不同的方法。现在让我们借助例子来看看如何做到这一点

**例 1:**

我们可以使用 **[DataFrame.loc](https://www.geeksforgeeks.org/python-pandas-dataframe-loc/)** 添加一行。我们可以在数据框的最后添加一行。我们可以使用 **len(DataFrame.index)** 获取行数，以确定需要添加新行的位置。

```
from IPython.display import display, HTML

import pandas as pd
from numpy.random import randint

dict = {'Name':['Martha', 'Tim', 'Rob', 'Georgia'],
        'Maths':[87, 91, 97, 95],
        'Science':[83, 99, 84, 76]
       }

df = pd.DataFrame(dict)

display(df)

df.loc[len(df.index)] = ['Amy', 89, 93] 

display(df)
```

**输出:**

![add-row-to-existing-pandas-dataframe](img/b2c6980abd4446387b5a25eb5d3d4272.png)

**例 2:**

我们也可以使用**[data frame . append()](https://www.geeksforgeeks.org/python-pandas-dataframe-append/)**函数添加新行

```
from IPython.display import display, HTML

import pandas as pd
import numpy as np

dict = {'Name':['Martha', 'Tim', 'Rob', 'Georgia'],
        'Maths':[87, 91, 97, 95],
        'Science':[83, 99, 84, 76]
       }

df = pd.DataFrame(dict)

display(df)

df2 = {'Name': 'Amy', 'Maths': 89, 'Science': 93}
df = df.append(df2, ignore_index = True)

display(df)
```

**输出:**

![add-row-to-existing-pandas-dataframe](img/b2c6980abd4446387b5a25eb5d3d4272.png)

**例 3:**

我们还可以使用 **[pandas.concat()](https://www.geeksforgeeks.org/python-merge-join-and-concatenate-dataframes-using-panda/)** 来添加多行，方法是为我们需要添加的所有行创建一个新的数据框，然后将该数据框追加到原始数据框中。

```
from IPython.display import display, HTML

import pandas as pd
import numpy as np

dict = {'Name':['Martha', 'Tim', 'Rob', 'Georgia'],
        'Maths':[87, 91, 97, 95],
        'Science':[83, 99, 84, 76]
       }

df1 = pd.DataFrame(dict)
display(df1)

dict = {'Name':['Amy', 'Maddy'],
        'Maths':[89, 90],
        'Science':[93, 81]
       }

df2 = pd.DataFrame(dict)
display(df2)

df3 = pd.concat([df1, df2], ignore_index = True)
df3.reset_index()

display(df3)
```

**输出:**

![add-row-to-existing-pandas-dataframe](img/b3811f6d73ba6c4168ec18c13b33a684.png)