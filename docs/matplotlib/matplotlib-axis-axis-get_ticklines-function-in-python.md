# Python 中的 matplotlib . axis . axis . get _ 怕痒()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ 挠痒痒-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_ticklines-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ 怕痒()函数

matplotlib 库的 Axis 模块中的**axis . get _ 怕痒()函数**用于获取作为 Line2D 实例列表的刻度线。

> **语法:**axis . get _ 怕痒(自身，次要=False)
> 
> **参数:**该方法接受以下参数。
> 
> *   **次要:**该参数包含布尔值。如果为真，返回次要的怕痒，否则返回主要的怕痒。
> 
> **返回值:**该方法将刻度线作为线 2D 实例列表返回。

下面的例子说明了 matplotlib.axis . axis . get _ cleanines()函数在 matplotlib . axis 中的作用:

**例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
from matplotlib.axis import Axis  
import numpy as np 
import matplotlib.pyplot as plt 
from matplotlib.patches import Polygon 

def func(x): 
    return (x - 4) * (x - 6) * (x - 5) + 100

a, b = 2, 9  # integral limits 
x = np.linspace(0, 10) 
y = func(x) 

fig, ax = plt.subplots() 
ax.plot(x, y, "k", linewidth = 2) 
ax.set_ylim(bottom = 0) 

# Make the shaded region 
ix = np.linspace(a, b) 
iy = func(ix) 
verts = [(a, 0), *zip(ix, iy), (b, 0)] 

poly = Polygon(verts, facecolor ='green', 
               edgecolor ='0.5', alpha = 0.4) 
ax.add_patch(poly) 

ax.text(0.5 * (a + b), 30,  
        r"$\int_a ^ b f(x)\mathrm{d}x{content}quot;, 
        horizontalalignment ='center',  
        fontsize = 20) 

fig.text(0.9, 0.05, '$x{content}apos;) 
fig.text(0.1, 0.9, '$y{content}apos;) 

ax.spines['right'].set_visible(False) 
ax.spines['top'].set_visible(False) 

ax.set_xticks((a, b-a, b)) 
ax.set_xticklabels(('$a{content}apos;, '$valx{content}apos;, '$b{content}apos;))

fig.suptitle('Matplotlib.axis.Axis.get_ticklines()\n\
Function Example', fontweight ="bold")  
ax.grid()

print("Value of get_ticklines() :")
for i in ax.xaxis.get_ticklines():
    print(i)

plt.show()
```

**输出:**

![](img/a41eb7dfd346c63a32f6a912067efb54.png)

```py
Value of get_ticklines() :
Line2D()
Line2D()
Line2D()
Line2D()
Line2D()
Line2D()

```

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
from matplotlib.axis import Axis  
import numpy as np 
import matplotlib.pyplot as plt 

# Fixing random state for reproducibility 
np.random.seed(19680801) 

x = np.linspace(0, 2 * np.pi, 100) 
y = np.sin(x) 
y2 = y + 0.2 * np.random.normal(size = x.shape) 

fig, ax = plt.subplots() 
ax.plot(x, y) 
ax.plot(x, y2) 

ax.set_xticks([0, np.pi, 2 * np.pi]) 
ax.set_xticklabels(['0', r'$\pi{content}apos;, r'2$\pi{content}apos;])

for line in ax.yaxis.get_ticklines():
    # line is a Line2D instance
    line.set_color('tab:green')
    line.set_markersize(25)
    line.set_markeredgewidth(3)

ax.spines['left'].set_bounds(-1, 1) 
ax.spines['right'].set_visible(False) 
ax.spines['top'].set_visible(False) 

fig.suptitle('Matplotlib.axis.Axis.get_ticklines()\n\
Function Example', fontweight ="bold")  
ax.grid()

plt.show()
```

**输出:**

![](img/f9c1807df2b876b7c28e97b45d0a68ed.png)