# Python Bokeh–在图形上绘制六边形图块

> 原文:[https://www . geesforgeks . org/python-bokeh-绘图-六边形-平铺在图形上/](https://www.geeksforgeeks.org/python-bokeh-plotting-hexagon-tiles-on-a-graph/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用 HTML 和 JavaScript 来渲染它的图。它以现代网络浏览器为呈现目标，提供优雅、简洁的新颖图形结构和高性能交互性。

Bokeh 可用于在图形上绘制六边形图块。可以使用`plotting`模块的`hex_tile()`方法在图形上绘制六边形图块。

## 绘图. figure.hex_tile()

> **语法:** hex_tile(参数)
> 
> **参数:**
> 
> *   **q :** 六边形瓷砖中心的柱轴坐标
> *   **r :** 六边形瓷砖中心的行轴坐标
> *   **长宽比例:**长宽比例值，默认为 1
> *   **填充α:**六边形图块标记的填充α值
> *   **fill_color :** 六边形图块标记的填充颜色值
> *   **line _ alpha:**line alpha 的百分比值，默认为 1
> *   **线帽:**线的线帽值，默认为对接
> *   **线条 _ 颜色:**线条的颜色，默认为黑色
> *   **线划:**线划的值，如:实线、虚线、虚线、点划线、点划线[默认为实线]
> *   **线划偏移量:**线划偏移量的值，默认为 0
> *   **线连接:**线连接的值，默认为斜角
> *   **线宽:**线宽值，默认为 1
> *   **名称:**用户提供的型号名称
> *   **方向:**方向值，默认为点
> *   **比例:**单个图块的比例因子，默认为 1
> *   **尺寸:**六边形瓷砖的半径，默认为 1
> *   **标签:**用户为模型提供的值
> 
> **其他参数:**
> 
> *   **alpha :** 一次性设置所有 alpha 关键字参数
> *   **颜色:**一次性设置所有颜色关键字参数
> *   **legend_field :** 数据源中应使用的列的名称
> *   **legend_group :** 数据源中应使用的列的名称
> *   **图例 _ 标签:**标记图例条目
> *   **静音:**确定字形是否应该渲染为静音，默认为假
> *   **名称:**附加到渲染器的可选用户提供的名称
> *   **来源:**用户提供的数据源
> *   **视图:**用于过滤数据源的视图
> *   **可见:**决定是否渲染字形，默认为真
> *   **x_range_name :** 用于映射 x 坐标的额外范围的名称
> *   **y_range_name :** 用于映射 y 坐标的额外范围的名称
> *   **等级:**指定此字形的渲染等级顺序
> 
> **返回:**类的一个对象`GlyphRenderer`

**示例 1 :** 在本例中，我们将使用默认值绘制图表。我们已经提供了尺寸和填充颜色属性来使字形可见。

```py
# importing the modules 
from bokeh.plotting import figure, output_file, show 

# file to save the model 
output_file("gfg.html") 

# instantiating the figure object 
graph = figure(title = "Bokeh Hexagon Tiles Graph",
               match_aspect = True) 

# the points to be plotted 
r = [0, 0, 1] 
q = [1, 2, 2] 

# plotting the graph 
graph.hex_tile(r, q) 

# displaying the model 
show(graph) 
```

**输出:**
![](img/a3fe5e504baed1fad03ea0641b5f4290.png)

**示例 2 :** 在本例中，我们将绘制具有不同参数的六边形瓷砖

```py
# importing the modules 
from bokeh.plotting import figure, output_file, show 

# file to save the model 
output_file("gfg.html") 

# instantiating the figure object 
graph = figure(title = "Bokeh Hexagon Tiles Graph",
               match_aspect = True) 

# name of the x-axis 
graph.xaxis.axis_label = "x-axis"

# name of the y-axis 
graph.yaxis.axis_label = "y-axis"

# the points to be plotted 
r = [0, -1,  0,  1, -1, 0, 1]
q = [0,  0, -1, -1,  1, 1, 0] 

# fill color values
fill_color = ["yellow", "blue", "pink", "green", "orange", "red", "purple"]

# line color values
line_color = ["yellow", "blue", "pink", "green", "orange", "red", "purple"]

# plotting the graph 
graph.hex_tile(r, q,
               fill_color = fill_color,
               line_color = line_color) 

# displaying the model 
show(graph) 
```

**输出:**
![](img/dd68dee9977b43a303d69186d70589e5.png)