# Python Bokeh–在图形上用 Xs 绘制正方形

> 原文:[https://www . geesforgeks . org/python-bokeh-ploging-squares-with-xs-on-graph/](https://www.geeksforgeeks.org/python-bokeh-plotting-squares-with-xs-on-a-graph/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用 HTML 和 JavaScript 来渲染它的图。它以现代网络浏览器为呈现目标，提供优雅、简洁的新颖图形结构和高性能交互性。

Bokeh 可以用来在图上用 Xs 绘制正方形。使用`plotting`模块的`square_x()`方法可以在图形上用 Xs 绘制正方形。

## 绘图. figure.square_x()

> **语法:** square_x(参数)
> 
> **参数:**
> 
> *   **x :** 正方形中心的 x 坐标
> *   **y :** 正方形中心的 y 坐标
> 
> **返回:**类的一个对象`GlyphRenderer`

**示例 1 :** 在本例中，我们将使用默认值绘制图表。

```
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Square X Graph")

# the points to be plotted
x = 0
y = 0

# plotting the graph
graph.square_x(x, y, size = 30, fill_color = None)

# displaying the model
show(graph)
```

**输出:**
![](img/1bc207423e8f8e3d1aec53979a1759e0.png)

**示例 2 :** 在本例中，我们将使用各种其他参数绘制多个正方形

```
# importing the modules 
from bokeh.plotting import figure, output_file, show 

# file to save the model 
output_file("gfg.html") 

# instantiating the figure object 
graph = figure(title = "Bokeh Square X Graph") 

# name of the x-axis 
graph.xaxis.axis_label = "x-axis"

# name of the y-axis 
graph.yaxis.axis_label = "y-axis"

# points to be plotted
x = [3, 3, 5]
y = [3, 1, 3]
size = [130, 100, 60]

# color value of the square
color = ["yellow", "red", "purple"]

# fill alpha value of the square
fill_alpha = [0.9, 0.7, 0.5]

# plotting the graph 
graph.square_x(x, y,
               size = size,
               color = color,
               fill_alpha = fill_alpha) 

# displaying the model 
show(graph)
```

**输出:**
![](img/83946106b4b50caca03a25a88aa33e8a.png)