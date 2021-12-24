# Python 中的 Matplotlib.axis.Axis.pickable()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-可拾取-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-pickable-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . pickle()函数

matplotlib 库的 Axis 模块中的 **Axis.pickable()函数**用于返回艺术家是否可 pick。

> **语法:**轴.可拾取(自)
> 
> **参数:**此方法不接受任何参数。
> 
> **返回值:**此方法返回艺人是否可挑。

以下示例说明 matplotlib.axis.Axis.pickable()函数在 matplotlib.axis:
**示例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import numpy as np  
np.random.seed(19680801)  
import matplotlib.pyplot as plt  

volume = np.random.rayleigh(27, size = 40)  
amount = np.random.poisson(10, size = 40)  
ranking = np.random.normal(size = 40)  
price = np.random.uniform(1, 10, size = 40)  

fig, ax = plt.subplots()  

scatter = ax.scatter(volume * 2, amount * 3,  
                     c = ranking * 3,   
                     s = 0.3*(price * 3)**2,  
                     vmin = -4, vmax = 4,   
                     cmap = "Spectral")  

legend1 = ax.legend(*scatter.legend_elements(num = 5),  
                    loc ="upper left",  
                    title ="Ranking")  

ax.add_artist(legend1)  

ax.text(60, 30, "Value return : "
        + str(Axis.pickable(ax)),   
        fontweight ="bold",   
        fontsize = 18)

fig.suptitle('matplotlib.axis.Axis.pickable() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/6cebe72cb7aef3c57fe06b1de25ea3c3.png)

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import numpy as np  
import matplotlib.pyplot as plt  
import matplotlib.cbook as cbook  

np.random.seed(10**7)  
data = np.random.lognormal(size =(10, 4),  
                           mean = 4.5,  
                           sigma = 4.75)  

labels = ['G1', 'G2', 'G3', 'G4']  

result = cbook.boxplot_stats(data,   
                             labels = labels,   
                             bootstrap = 1000)  

for n in range(len(result)):  
    result[n]['med'] = np.median(data)  
    result[n]['mean'] *= 0.1

fig, axes1 = plt.subplots()  
axes1.bxp(result)  

axes1.text(2, 30000,  
           "Value return : " 
           + str(Axis.pickable(axes1)),   
           fontweight ="bold")  

fig.suptitle('matplotlib.axis.Axis.pickable() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/def3f908c729ec3920dca75ca9de96c0.png)