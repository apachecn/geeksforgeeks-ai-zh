# 在 Matplotlib 中定位颜色条

> 原文:[https://www . geesforgeks . org/positioning-the-color bar-in-matplotlib/](https://www.geeksforgeeks.org/positioning-the-colorbar-in-matplotlib/)

[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 python 编程语言中的绘图库，默认情况下是 Python 语言中 NumPy 库的数值数学扩展。在用 python 语言编程时，我们使用 matplotlib 库包进行图形和直方图可视化。但是在 python 中使用 matplotlib 绘制直方图时，它缺少相邻条之间的分割或间隔。这使得直方图的处理变得非常繁琐，并且变得非常难以解释。在本文中，我们将在 Matplotlib 中看到 colorbar 的定位。

matplotlib 的 pyplot 模块中的 **colorbar()函数**在绘图中添加一个 colorbar，用于指示色标。

> **语法:**matplotlib . pyplot . colorbar(mappable = none，cax=None，ax=None，**kwarg)
> 
> **参数:**
> 
> *   **ax:** 该参数为可选参数，包含 Axes 或**Axes 列表。**
> *   ******kwarg** (关键字参数):该参数为可选参数，有两种:**
> 
> ****返回:** colorbar，它是类‘matplotlib . color bar . color bar’的实例。**

### ****进场:****

*   **导入所需模块。**
*   **为两个坐标准备数据点。**
*   **用 pyplot 绘制图表。**
*   **使用适当的关键字和适当的值，用 pyplot.colorbar 定位 colorbar**
*   **显示图**

****示例 1:** *在地块右侧添加彩条。***

**在本例中，我们将用不同的数据点绘制散点图，然后使用颜色条方法 在图表的右侧放置一个颜色条。默认情况下，颜色条显示在右边。**

## **蟒蛇 3**

```py
import matplotlib.pyplot as plt

x = [5, 7, 8, 7, 2, 17, 2, 9,
     4, 11, 12, 9, 6]

y = [99, 86, 87, 88, 100, 86,
     103, 87, 94, 78, 77, 85, 86]

plt.scatter(x, y, c="blue")

# Plot colorbar
plt.colorbar(label="Color Ratio")

# To show the plot
plt.show()
```

****输出:****

**![](img/800b4404022e471f19438cf126b099ff.png)**

****示例 2:** *在地块下方添加彩条。***

**在本例中，我们将用不同的数据点绘制散点图，然后使用颜色条方法 在图表下方放置一个颜色条。要做到这一点，需要为其方向关键字赋予“水平”值。**

## **蟒蛇 3**

```py
import matplotlib.pyplot as plt

x = [5, 7, 8, 7, 2, 17, 2, 9,
     4, 11, 12, 9, 6]

y = [99, 86, 87, 88, 100, 86,
     103, 87, 94, 78, 77, 85, 86]

plt.scatter(x, y, c="blue")

# Plot horizontal colorbar
plt.colorbar(label="Color Ratio",
             orientation="horizontal")

# To show the plot
plt.show()
```