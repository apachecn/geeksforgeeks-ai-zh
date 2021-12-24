# 蟒蛇海鸟教程

> 原文:[https://www.geeksforgeeks.org/python-seaborn-tutorial/](https://www.geeksforgeeks.org/python-seaborn-tutorial/)

**Seaborn** 是 Python 中主要用于统计绘图的库。它建立在 Matplotlib 之上，并提供了漂亮的默认样式和调色板，使统计图更具吸引力。

在本教程中，我们将从基础知识开始学习 Python Seaborn，并使用 Seaborn 基础知识、概念和可以绘制的不同图形的庞大数据集来推进。

**目录**

> *   [Introduction](#Getting)
> *   [九月 Matplotlib 僧曰 seaborn〔t1〕](#Seaborn)
> *   [Customize the Seaborn plot](#Customizing)
>     *   [Change the graphic aesthetic feeling](#Aesthetic)
>     *   [Remove thorns](#Removal)
>     *   [Change the graphic size](#Size)
>     *   [Zoom plot](#Scaling)
>     *   T30] Set the style temporarily
>     *   [Set the default palette](#default)
> *   [Create multiple plots with Seaborn](#Multiple)
>     *   [僧曰 matplot lib〔t1〕](#Matplotlib)
>     *   [使用海鸟](#Seaborn)
> *   [Create different types of plots](#Different)
>     *   [Relational plot](#Relational)

[**近期关于 Seaborn 的文章！！**T3】](https://www.geeksforgeeks.org/tag/python-seaborn/)

## 入门指南

首先，让我们安装 Seaborn。Seaborn 可以使用 pip 安装。在终端中键入以下命令。

```py
pip install seaborn
```

在终端中，它看起来像这样–

安装完成后，您将在终端的末尾看到一条成功安装的消息，如下所示。

**注意:**海博恩有以下依赖关系–

*   Python 2.7 或 3.4+
*   numpy
*   我的天啊
*   熊猫
*   马特普洛特利布

安装完成后，让我们看一个使用 Seaborn 的简单绘图示例。我们将使用虹膜数据集绘制一个简单的线图。虹膜数据集包含花瓣长度、花瓣宽度、萼片长度、萼片宽度和物种类型五列。鸢尾是一种开花植物，研究人员测量了不同鸢尾花的各种特征，并以数字方式记录下来。

**示例:**

## 蟒蛇 3

```py
# importing packages 
import seaborn as sns 

# loading dataset 
data = sns.load_dataset("iris") 

# draw lineplot 
sns.lineplot(x="sepal_length", y="sepal_width", data=data)
```