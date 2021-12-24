# Python Bokeh–在图形上绘制三角形引脚

> 原文:[https://www . geesforgeks . org/python-bokeh-绘图-三角形-图钉/](https://www.geeksforgeeks.org/python-bokeh-plotting-triangle-pins-on-a-graph/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用 HTML 和 JavaScript 来渲染它的图。它以现代网络浏览器为呈现目标，提供优雅、简洁的新颖图形结构和高性能交互性。

Bokeh 可用于在图形上绘制三角形引脚。可以使用`plotting`模块的`triangle_pin()`方法在图形上绘制三角形引脚。

## ploting . figure . triangle _ pin()

> **语法:**三角形 _pin(参数)
> 
> **参数:**
> 
> *   **x :** 三角形标记中心的 x 坐标
> *   **y :** 三角形标记中心的 y 坐标
> 
> **返回:**类的一个对象`GlyphRenderer`

**示例 1 :** 在本例中，我们将使用默认值绘制图表。

```
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Triangle Pin Graph")

# the points to be plotted
x = 0
y = 0

# plotting the graph
graph.triangle_pin(x, y, size = 30)

# displaying the model
show(graph)
```

**输出:**
![](img/2c5dd660e804c6465bb983610a0095a0.png)

**示例 2 :** 在本例中，我们将绘制多个具有各种其他参数的三角形引脚。

```
# importing the modules 
from bokeh.plotting import figure, output_file, show 

# file to save the model 
output_file("gfg.html") 

# instantiating the figure object 
graph = figure(title = "Bokeh Triangle Pin Graph") 

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
graph.triangle_pin(x, y,
                   size = size,
                   color = color,
                   fill_alpha = fill_alpha) 

# displaying the model 
show(graph) 
```

**输出:**
![](img/357643d2e431c0fb9594793929345303.png)