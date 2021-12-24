# Python 中的 matplotlib . artist . artist . get _ GID()

> 原文:[https://www . geesforgeks . org/matplotlib-artist-artist-get _ GID-in-python/](https://www.geeksforgeeks.org/matplotlib-artist-artist-get_gid-in-python/)

[**【Matplotlib】**](https://www.geeksforgeeks.org/python-introduction-matplotlib/)是 Python 中的一个库，它是 NumPy 库的数字-数学扩展。 **艺术家类** 包含将渲染到图形画布中的对象的抽象基类。图形中所有可见的元素都是艺术家的子类。

## matplotlib . artist . artist . get _ GID()方法

matplotlib 库的艺术家模块中的 **get_gid()方法**用于获取组 id。

> ***语法:*** 艺术家 g *et_gid(自我)*
> 
> ***参数:**此方法不接受任何参数。*
> 
> ***返回:**该方法返回组 id。*

以下示例说明了 matplotlib 中的 matplotlib . artist . get _ GID()函数:

**例 1:**

```
# Implementation of matplotlib function
from matplotlib.artist import Artist 
import numpy as np 
import matplotlib.pyplot as plt 

y, x = np.mgrid[:5, 1:6] 

poly_coords = [ 
    (0.25, 2.75), (3.25, 2.75), 
    (2.25, 0.75), (0.25, 0.75) 
] 

fig, ax = plt.subplots() 

cells = ax.plot(x, y, x + y, color ='green') 

ax.add_patch( 
    plt.Polygon(poly_coords,  
                color ='forestgreen',  
                alpha = 0.5) 
    ) 

ax.margins(x = 0.1, y = 0.05) 
ax.set_aspect('equal') 

for i, t in enumerate(ax.patches): 
    Artist.set_gid(t, 'patch_% d' % i)
    print("Value Return :", Artist.get_gid(t))

fig.suptitle("""matplotlib.artist.Artist.get_gid()
function Example""", fontweight="bold")

plt.show()
```

**输出:**

![](img/e0f6489b94d0cdcba7a093ef08843f0d.png)

```
Value Return : patch_ 0

```

**例 2:**

```
# Implementation of matplotlib function
from matplotlib.artist import Artist 
import numpy as np 
import matplotlib.pyplot as plt 

fig, ax = plt.subplots() 

circle = plt.Circle((0, 0), 5, fc ='blue') 
rect = plt.Rectangle((-5, 10), 10, 5, fc ='green') 

ax.add_patch(circle) 
ax.add_patch(rect) 

circle_tip = ax.annotate('This is a blue circle.', 
            xy =(0, 0), 
            xytext =(30, -30), 
            textcoords ='offset points', 
            color ='w', 
            ha ='left', 
            bbox = dict(boxstyle ='round, pad =.5',  
                        fc =(.1, .1, .1, .92), 
                        ec =(1., 1., 1.),  
                        lw = 1, 
                        zorder = 1), 
            ) 

rect_tip = ax.annotate('This is a green rectangle.', 
            xy =(-5, 10), 
            xytext =(30, 40), 
            textcoords ='offset points', 
            color ='w', 
            ha ='left', 
            bbox = dict(boxstyle ='round, pad =.5', 
                        fc =(.1, .1, .1, .92),  
                        ec =(1., 1., 1.),  
                        lw = 1, 
                        zorder = 1), 
            ) 

print("Value Return :") 
for i, t in enumerate(ax.patches): 
    Artist.set_gid(t, 'patch_% d'% i)
    print(Artist.get_gid(t)) 

for i, t in enumerate(ax.texts): 
    Artist.set_gid(t, 'tooltip_% d'% i)
    print(Artist.get_gid(t)) 

ax.set_xlim(-30, 30) 
ax.set_ylim(-30, 30) 
ax.set_aspect('equal') 

fig.suptitle("""matplotlib.artist.Artist.get_gid()
function Example""", fontweight="bold")

plt.show()
```

**输出:**

![](img/b81ceb00f1d97a192ffaa5ac414257bb.png)

```
Value Return :
patch_ 0
patch_ 1
tooltip_ 0
tooltip_ 1

```