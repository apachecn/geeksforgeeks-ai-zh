# 蟒蛇|熊猫面板. count()

> 原文:[https://www.geeksforgeeks.org/python-pandas-panel-count/](https://www.geeksforgeeks.org/python-pandas-panel-count/)

在熊猫中，面板是一个非常重要的三维数据容器。三个轴的名称旨在为描述涉及面板数据的操作，特别是面板数据的计量经济学分析提供一些语义含义。

`**Panel.count()**`功能用于返回请求轴上的观察次数。

> **语法:** Panel.count(轴= ' major ')
> 
> **参数:**轴:{'items '，' major '，' minor'}或{0，1，2}
> 
> **返回:**数据帧的计数

**代码#1:**

```py
# importing pandas module 
import pandas as pd 
import numpy as np

df1 = pd.DataFrame({'a': ['Geeks', 'For', 'geeks', 'real'], 
                    'b': [-11, +1.025, -114.48, 1333]})

data = {'item1':df1, 'item2':df1}

# creating Panel 
panel = pd.Panel.from_dict(data, orient ='minor')
print(panel, "\n")
print(panel['b'])

print("\n", panel['b'].count())
```

**输出:**
![](img/cdfea5fd06220644c341a5227f0ceb84.png)

**代码#2:**

```py
# importing pandas module 
import pandas as pd 
import numpy as np

df1 = pd.DataFrame({'a': ['Geeks', 'For', 'geeks'], 
                    'b': np.random.randn(3)})

data = {'item1':df1, 'item2':df1}

# creating Panel 
panel = pd.Panel.from_dict(data, orient ='minor')
print(panel, "\n")
print(panel['b'])

df2 = pd.DataFrame({'b': [11, 12, 13]})
print("\n", panel['b'].count())
```

**输出:**
![](img/c8ebfe673bbcbdde2d561818e753d5a8.png)