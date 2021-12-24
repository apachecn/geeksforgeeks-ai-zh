# Python Bokeh–在图形上绘制椭圆

> 原文:[https://www . geesforgeks . org/python-bokeh-绘图-图形上的椭圆/](https://www.geeksforgeeks.org/python-bokeh-plotting-ellipses-on-a-graph/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用 HTML 和 JavaScript 来渲染它的图。它以现代网络浏览器为呈现目标，提供优雅、简洁的新颖图形结构和高性能交互性。

Bokeh 可用于在图形上绘制椭圆。可以使用`plotting`模块的`ellipse()`方法在图形上绘制椭圆。

## 绘图.图形.椭圆()

> **语法:**椭圆(参数)
> 
> **参数:**
> 
> *   **x :** 椭圆中心的 x 坐标
> *   **y :** 椭圆中心的 y 坐标
> *   **宽度:**每个椭圆的宽度
> *   **高度:**每个椭圆的高度
> *   **角度:**椭圆的旋转角度，默认为 0
> *   **角度 _ 单位:**角度单位，默认为 rad
> *   **填充α:**填充椭圆的α值
> *   **填充颜色:**椭圆的填充颜色值
> *   **高度单位:**高度单位，默认为数据
> *   **line _ alpha:**line alpha 的百分比值，默认为 1
> *   **线帽:**线的线帽值，默认为对接
> *   **线条 _ 颜色:**线条的颜色，默认为黑色
> *   **line_dash :** value of line dash such as :
>     *   固体
>     *   虚线
>     *   有点的
>     *   dotdash！dotdash！dotdash
>     *   达什特
>     
>     默认为实心
>     
>     
> *   **线划偏移量:**线划偏移量的值，默认为 0
> *   **线连接:**线连接的值，默认为斜角
> *   **线宽:**线宽值，默认为 1
> *   **名称:**用户提供的型号名称
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

**示例 1 :** 在本例中，我们将使用默认值绘制图表。

```py
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Ellipse Graph",
               match_aspect = True)

# the points to be plotted
x = 0
y = 0

# width of the ellipse
width = 60

# height of the ellipse
height = 20

# plotting the graph
graph.ellipse(x, y,
              width = width,
              height = height)

# displaying the model
show(graph)
```

**输出:**
![](img/533b2ec48c28c60366ec36fd1d5f6545.png)

**示例 2 :** 在本例中，我们将绘制多个具有不同参数的椭圆。

```py
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Ellipse Graph")

# name of the x-axis
graph.xaxis.axis_label = "x-axis"

# name of the y-axis
graph.yaxis.axis_label = "y-axis"

# the points to be plotted
x = [0, 30, 0]
y = [0, 30, -30]

# width of the ellipse
width = [60, 20, 40]

# height of the ellipse
height = [20, 180, 80]

# angle of the ellipse
angle = [0, 150, 20]

# fill alpha values
fill_alpha = 0.3

# fill color values
fill_color = ["red", "yellow", "blue"]

# line color value
line_color = "black"

# plotting the graph
graph.ellipse(x, y,
              width = width,
              height = height,
              angle = angle,
              fill_alpha = fill_alpha,
              fill_color = fill_color,
              line_color = line_color)

# displaying the model
show(graph)
```

**输出:**
![](img/69630bdddbf0b511e1fee5a9ba4f8ef9.png)