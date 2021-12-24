# 如何将图像转换成 NumPy 数组？

> 原文:[https://www . geeksforgeeks . org/如何将图像转换为 numpy-array/](https://www.geeksforgeeks.org/how-to-convert-images-to-numpy-array/)

图像是表示工作模型的一种更简单的方式。在机器学习中，Python 使用高度、宽度、通道格式的图像数据。即图像被转换成高度、宽度、通道格式的数字阵列。

### 所需模块:

*   [**NumPy:**](https://www.geeksforgeeks.org/python-numpy/) 默认情况下，从 3.x 开始，在 Python 的更高版本中，NumPy 是可用的，如果不可用(在较低版本中)，可以使用安装

```
pip install numpy
```

*   [**枕头:**](https://www.geeksforgeeks.org/python-pillow-a-fork-of-pil/) 这个也要在以后的版本中明确安装。它是首选的图像处理工具。在 Python 3 中，枕头 Python 库只不过是 PIL 的升级版。它可以使用安装

```
pip install Pillow
```

使用下面的代码

## python 3

可以轻松检查已安装枕头的版本

```
import PIL

print('Installed Pillow Version:', PIL.__version__)
```