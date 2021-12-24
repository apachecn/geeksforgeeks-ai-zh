# Python 中的 Matplotlib.axis.Axis.set_alpha()函数

> 原文:[https://www . geesforgeks . org/matplotlib-axis-axis-set _ alpha-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-set_alpha-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## Matplotlib.axis.Axis.set_alpha()函数

matplotlib 库的 Axis 模块中的 **Axis.set_alpha()函数**用于设置用于混合的 alpha 值。

> **语法:** Axis.set_alpha(self，alpha)
> 
> **参数:**该方法接受以下参数。
> 
> *   **alpha:** 此参数为包含浮点值或无。
> 
> **返回值:**此方法不返回值。

以下示例说明 matplotlib.axis.Axis.set_alpha()函数在 matplotlib.axis:
**示例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt  
import numpy as np  

# create test data  
np.random.seed(10**7)  
data = [sorted(np.random.normal(0, std, 100))   
       for std in range(1, 5)]  

fig, ax1 = plt.subplots()  
val = ax1.violinplot(data)  
ax1.set_ylabel('Result')  
ax1.set_xlabel('Domain Name')  

for i in val['bodies']:  
    i.set_facecolor('yellow')  
    Axis.set_alpha(i, 0.3)

fig.suptitle('matplotlib.axis.Axis.set_alpha() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/344ffa175bdb95197eaa15af961d9bcc.png)

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt  
import numpy as np  
from matplotlib.patches import Ellipse  

NUM = 100

ells = [Ellipse(xy = np.random.rand(2) * 10,  
                width = np.random.rand(),   
                height = np.random.rand(),  
                angle = np.random.rand() * 360)  
        for i in range(NUM)]  

fig, ax = plt.subplots(subplot_kw ={'aspect': 'equal'})  

for e in ells:  
    ax.add_artist(e)  
    e.set_clip_box(ax.bbox)  
    Axis.set_alpha(e, np.random.rand())  
    e.set_facecolor(np.random.rand(4))  

ax.set_xlim(2, 8)  
ax.set_ylim(2, 8) 

fig.suptitle('matplotlib.axis.Axis.set_alpha() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/efd32419e3904ed356491f5375a3b44b.png)