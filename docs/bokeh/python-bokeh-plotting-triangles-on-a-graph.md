# Python Bokeh–在图形上绘制三角形

> 原文:[https://www . geesforgeks . org/python-bokeh-绘图-图形上的三角形/](https://www.geeksforgeeks.org/python-bokeh-plotting-triangles-on-a-graph/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用超文本标记语言和 JavaScript 渲染它的绘图。它以现代网络浏览器为目标，提供优雅、简洁的新颖图形结构和高性能交互性。

Bokeh 可用于在图形上绘制三角形。可以使用`plotting`模块的`triangle()`方法在图形上绘制三角形。

## 绘图.图形.三角形()

> **语法:**三角形(参数)
> 
> **参数:**
> 
> *   **x :** 三角形标记中心的 x 坐标
> *   **y :** 三角形标记中心的 y 坐标
> 
> **返回:**类的一个对象`GlyphRenderer`

**示例 1 :** 在本例中，我们将使用默认值绘制图表。

```py
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Triangle Graph")

# the points to be plotted
x = 0
y = 0

# plotting the graph
graph.triangle(x, y, size = 30)

# displaying the model
show(graph) 
```

**输出:**
![](img/968e6dde0b578b517fedb500d5f0b1dd.png)

**示例 2 :** 在本例中，我们将使用各种其他参数绘制多个三角形。

```py
# importing the modules 
from bokeh.plotting import figure, output_file, show 

# file to save the model 
output_file("gfg.html") 

# instantiating the figure object 
graph = figure(title = "Bokeh Triangle Graph") 

# name of the x-axis 
graph.xaxis.axis_label = "x-axis"

# name of the y-axis 
graph.yaxis.axis_label = "y-axis"

# points to be plotted
x = [3, 3, 5]
y = [3, 1, 3]
size = [130, 100, 60]

# color value of the triangles
color = ["yellow", "red", "purple"]

# fill alpha value of the triangles
fill_alpha = [0.9, 0.7, 0.5]

# plotting the graph 
graph.triangle(x, y,
               size = size,
               color = color,
               fill_alpha = fill_alpha) 

# displaying the model 
show(graph)
```

**输出:**
![](img/56103cc112a706686092143ec34571c3.png)