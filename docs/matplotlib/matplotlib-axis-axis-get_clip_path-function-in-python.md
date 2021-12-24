# Python 中的 matplotlib . axis . axis . get _ clip _ path()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ clip _ path-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_clip_path-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ clip _ path()函数

matplotlib 库的 Axis 模块中的 **Axis.get_clip_path()函数**用于获取剪辑路径。

> **语法:** Axis.get_clip_path(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**此方法返回剪辑路径。

下面的例子说明了 matplotlib . axis . get _ clip _ path()函数在 matplotlib.axis:
中的作用

**例 1:**

**使用的图像**

![](img/01b4c4a487799db375e5275e0d4480a1.png)

## 蟒蛇 3

```
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt  
import matplotlib.patches as patches  
import matplotlib.cbook as cbook  

with cbook.get_sample_data('loggf.PNG') as image_file:  
    image = plt.imread(image_file)  

fig, ax = plt.subplots()  
im = ax.imshow(image)  
patch = patches.Rectangle((10, 10),  
                          560,  
                          500,   
                          transform = ax.transData)   

if Axis.get_clip_path(im) is None:  
    im.set_clip_path(patch)

fig.suptitle("""matplotlib.axis.Axis.get_clip_path()
function Example\n""", fontweight ="bold")  

plt.show()
```