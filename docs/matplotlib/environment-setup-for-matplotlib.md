# 【Matplotlib 的环境设置

> 原文:[https://www . geesforgeks . org/environment-setup-for-matplotlib/](https://www.geeksforgeeks.org/environment-setup-for-matplotlib/)

**Matplotlib** 是一个整体包，用于在 Python 中创建静态、动画和交互式可视化。它为你打开了一个全新的可能性世界！尤其是和 [Numpy](https://www.geeksforgeeks.org/python-numpy/) 或者[熊猫](https://www.geeksforgeeks.org/pandas-tutorial/)库一起使用，可以做出难以想象的事情。这些情节可能会给我们一个全新的视角。现在，问题出现了，即如何使它在您的计算机上运行？但是一个更主要的问题是，软件在你的计算机上运行的先决条件或者我们称之为依赖是什么？

#### 属国

*   [蟒蛇](https://www.python.org/downloads/) ( > = 3.6)
*   [FreeType](https://www.freetype.org/) ( > = 2.3)
*   [libpng](http://www.libpng.org/) ( > = 1.2)
*   num py(>= 1.11)
*   安装工具
*   [循环仪](https://matplotlib.org/cycler/) ( > = 0.10.0)
*   [dateutil](https://pypi.org/project/python-dateutil/) ( > = 2.1)
*   [猕猴桃粉](https://github.com/nucleic/kiwi) ( > = 1.0.0)
*   [语法分析](https://pypi.org/project/pyparsing/)

我们准备好在系统上安装 Matplotlib 了！

### 安装

在 macOS 上

*   使用 brew 安装 libpng 和 Freetype:

    ```py
    brew install libpng freetype pkg-config
    ```

*   如果您正在使用 MacPorts，请执行以下命令:

    ```py
    port install libpng freetype pkgconfig
    ```

*   现在使用

    ```py
    python -mpip install 
    ```

    从源代码安装 matplotlib

**在 Linux 上**
这是在 Ubuntu 上最容易得到的，因为你只需使用下面的命令就可以得到所有的依赖项:

```py
sudo apt-get build-dep python-matplotlib
```