# 使用 Matplotlib 的数据可视化

> 原文:[https://www . geesforgeks . org/data-visualization-use-matplotlib/](https://www.geeksforgeeks.org/data-visualization-using-matplotlib/)

**数据可视化**是以图形或图表的形式呈现数据的过程。它有助于非常容易地理解大量复杂的数据。它允许决策者非常有效地做出决策，也允许他们非常容易地识别新的趋势和模式。它也用于机器学习和探索性数据分析(EDA)的高级数据分析。数据可视化可以用各种工具来完成，比如 Tableau、Power BI、Python。

在本文中，我们将讨论如何借助 Python 的 Matplotlib 库来可视化数据。

## Matplotlib

Matploptib 是 Python 的一个低级库，用于数据可视化。它易于使用，并且像图形和可视化一样仿真 MATLAB。这个库建立在 NumPy 数组之上，由折线图、条形图、直方图等几个图组成。它提供了很大的灵活性，但代价是编写更多的代码。

## 装置

我们将使用 pip 命令来安装这个模块。如果您没有安装 pip，请参考文章， [**下载并安装 pip 最新版本。**T3】](https://www.geeksforgeeks.org/download-and-install-pip-latest-version/)

要安装 Matplotlib，请在终端中键入以下命令。

```
pip install matplotlib
```

![install matplotlib](img/504f02bdb1fee23d769cc38245578b3c.png)

> 参考下面的文章来获得更多关于用 Matplotlib 设置环境的信息。
> 
> *   【Matplotlib 的环境设置
> *   [使用 Matplotlib 搭配 Jupyter 笔记本](https://www.geeksforgeeks.org/using-matplotlib-with-jupyter-notebook/)

## Pyplot

[**Pyplot**](https://www.geeksforgeeks.org/pyplot-in-matplotlib/) 是一个提供类似 MATLAB 界面的 Matplotlib 模块。Matplotlib 被设计成和 MATLAB 一样好用，具有使用 Python 的能力和免费开源的优势。每个 pyplot 函数都会对图形进行一些更改:例如，创建图形、在图形中创建绘图区域、在绘图区域中绘制一些线条、用标签装饰图形等。我们可以使用 Pyplot 的各种图包括线图、直方图、散点图、三维图、图像图、等高线图和极坐标图。

在简单了解了 Matplotlib 和 pyplot 之后，让我们看看如何创建一个简单的情节。

**示例:**

## 蟒蛇 3

```
import matplotlib.pyplot as plt

# initializing the data
x = [10, 20, 30, 40]
y = [20, 25, 35, 55]

# plotting the data
plt.plot(x, y)

plt.show()
```