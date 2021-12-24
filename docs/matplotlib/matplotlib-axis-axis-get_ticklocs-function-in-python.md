# Python 中的 matplotlib . axis . axis . get _ tick locs()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ tick locs-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_ticklocs-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ ticlocs()函数

matplotlib 库的 Axis 模块中的 **Axis.get_ticklocs()函数**用于获取数据坐标中的刻度位置数组。

> **语法:** Axis.get_ticklocs(self，minor=False)
> 
> **参数:**该方法接受以下参数。
> 
> *   **次要:**该参数包含布尔值。如果为真，返回次要 tick loc，否则返回主要 tick loc。
> 
> **返回值:**此方法返回数据坐标中的刻度位置数组。

以下示例说明 matplotlib . axis . axis . get _ tick locs()函数在 matplotlib.axis:
**示例 1:**

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

fig.suptitle('Matplotlib.axis.Axis.get_ticklocs()\n\
Function Example', fontweight ="bold")  
ax.grid()

print("Value of get_ticklocs() :")
for i in ax.xaxis.get_ticklocs():
    print(i)

plt.show()
```

**输出:**

![](img/827d5ae8c5b7c0d224e6bd86093bd9f9.png)

```py
Value of get_ticklocs() :
2
7
9

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

ax.spines['left'].set_bounds(-1, 1) 
ax.spines['right'].set_visible(False) 
ax.spines['top'].set_visible(False)

print("Value of get_ticklocs() :")
for i in ax.xaxis.get_ticklocs():
    print(i)

fig.suptitle('Matplotlib.axis.Axis.get_ticklocs()\n\
Function Example', fontweight ="bold")  
ax.grid()

plt.show()
```

**输出:**

![](img/c3db4557373a1c58d74f3a3781f02a3e.png)

```py
Value of get_ticklocs() :
0.0
3.141592653589793
6.283185307179586

```