# Python Bokeh–在图形上绘制 Ys

> 原文:[https://www . geesforgeks . org/python-bokeh-ploging-ys-on-a-graph/](https://www.geeksforgeeks.org/python-bokeh-plotting-ys-on-a-graph/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用 HTML 和 JavaScript 来渲染它的图。它以现代网络浏览器为呈现目标，提供优雅、简洁的新颖图形结构和高性能交互性。

Bokeh 可用于在图表上绘制 Ys。可以使用`plotting`模块的`y()`方法在图形上绘制 Ys。

## 标绘. figure.y()

> **语法:** y(参数)
> 
> **参数:**
> 
> *   **x:**y 标记中心的 x 坐标
> *   **y :** y 标记中心的 y 坐标
> 
> **返回:**类的一个对象`GlyphRenderer`

**示例 1 :** 在本例中，我们将使用默认值绘制图表。

```
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Y Graph")

# the points to be plotted
x = 0
y = 0

# plotting the graph
graph.y(x, y, size = 30)

# displaying the model
show(graph)
```

**输出:**
![](img/f0563ba4967946bdc1d5de4f0273bb32.png)

**示例 2 :** 在本例中，我们将使用各种其他参数绘制多个 Ys。

```
# importing the modules 
from bokeh.plotting import figure, output_file, show 

# file to save the model 
output_file("gfg.html") 

# instantiating the figure object 
graph = figure(title = "Bokeh Y Graph") 

# name of the x-axis 
graph.xaxis.axis_label = "x-axis"

# name of the y-axis 
graph.yaxis.axis_label = "y-axis"

# points to be plotted
x = [3, 3, 5]
y = [3, 1, 3]
size = [130, 100, 60]

# color value of the Ys
color = ["yellow", "red", "purple"]

# fill alpha value of the Ys
fill_alpha = [0.9, 0.7, 0.5]

# line width of the Ys
line_width = [10, 15, 5]

# plotting the graph 
graph.y(x, y,
        size = size,
        color = color,
        fill_alpha = fill_alpha,
        line_width = line_width) 

# displaying the model 
show(graph)
```

**输出:**
![](img/8a9f15cbf14d3c15636e1e1fda186664.png)