# 【Matplotlib VS Seaborn 的区别

> 原文:[https://www . geesforgeks . org/difference-matplotlib-vs-seaborn/](https://www.geeksforgeeks.org/difference-between-matplotlib-vs-seaborn/)

数据可视化是数据的图形表示。它将一个巨大的数据集转换成小图形，从而有助于数据分析和预测。它是数据科学中不可或缺的元素，使复杂的数据更容易理解和访问。Matplotlib 和 Seaborn 通过 Python 充当数据可视化的骨干。

**[Matplotlib:](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 它是一个 Python 库，用来在 Numpy 和 Pandas 等其他库的帮助下绘制图形。它是 Python 中可视化数据的强大工具。它用于创建静态干扰和绘制阵列的 2D 图。约翰·d·亨特于 2002 年首次提出。它使用 Pyplot 提供像 MATLAB 一样的接口自由和开源。它能够处理各种操作系统及其图形后端。

**[海伯恩](https://www.geeksforgeeks.org/plotting-graph-using-seaborn-python/) :** 它也是一个 Python 库，用于借助 Matplotlib、Pandas 和 Numpy 绘制图形。它建在 Matplotlib 的屋顶上，被认为是 Matplotlib 图书馆的超集。它有助于可视化单变量和双变量数据。它使用美丽的主题来装饰 Matplotlib 图形。它是描绘线性回归模型的重要工具。它用于制作静态时间序列数据的图表。它消除了图形的重叠，也有助于它们的美化。

## 马特普罗特利布和西伯恩的差异表

| 特征 | Matplotlib |  |
| --- | --- | --- |
| **功能性** | 用于制作基本图形。借助柱状图、直方图、饼状图、散点图、线条等，数据集被可视化。 | Seaborn 包含了很多数据可视化的模式和图。它使用迷人的主题。它有助于将整个数据汇编成一个单独的图表。它还提供数据分发。 |
| **句法** | 它用的是比较复杂冗长的句法。示例:条形图的语法- matplotlib.pyplot.bar(x 轴，y 轴)。 | 它使用比较简单的语法，更容易学习和理解。示例:条形图的语法- seaborn.barplot(x 轴，y 轴)。 |
| **处理多个图形** | 我们可以同时打开和使用多个图形。然而，它们显然是封闭的。一次关闭一个图形的语法:matplotlib.pyplot.close()。关闭所有图形的语法:matplotlib . pyplot . close(" all ") | Seaborn 设置创建每个图形的时间。但是可能会导致(OOM)内存不足的问题 |
| **可视化** | Matplotlib 与 Numpy 和 Pandas 连接良好，充当 python 中数据可视化的图形包。Pyplot 提供了与 MATLAB 类似的特性和语法。因此，MATLAB 用户可以轻松学习。 | 在处理 Pandas 数据帧时，Seaborn 更加游刃有余。它使用基本的方法集来提供 python 中漂亮的图形。 |
| **【柔性】** | Matplotlib 是一个高度定制和健壮的 | Seaborn 借助其默认主题 |
| **数据框和数组** | Matplotlib 可以高效地处理数据框和数组。它将图形和轴视为对象。它包含各种用于绘图的有状态 API。因此，类似 plot()的方法可以在没有参数的情况下工作。 | Seaborn 比 Matplotlib 功能更强、更有条理，将整个数据集视为一个单元。Seaborn 不是那么有状态，因此在调用 plot() |
| **等方法时需要参数【用例】** | Matplotlib 使用 Pandas 和 Numpy 绘制各种图形 | Seaborn 是 Matplotlib 的扩展版本，它使用 Matplotlib 以及 Numpy 和 Pandas 来绘制图形 |