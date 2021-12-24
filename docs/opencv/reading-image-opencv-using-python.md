# 使用 Python 在 OpenCV 中读取图像

> 原文:[https://www . geesforgeks . org/reading-image-opencv-using-python/](https://www.geeksforgeeks.org/reading-image-opencv-using-python/)

**先决条件:**[OpenCV 基础知识](https://www.geeksforgeeks.org/set-opencv-anaconda-environment/)

在本文中，我们将尝试使用 OpenCV(开源计算机视觉)打开一个图像。要在 python 中使用 OpenCV 库，我们需要安装这些库作为先决条件:

1.  Numpy 库(必要的，因为 OpenCV 在后台使用它)。
2.  opencv python〔t0〕

**要安装这些库，我们需要在 cmd 中运行这些 pip 命令:**

```py
pip install opencv-python
pip install numpy
pip install matplotlib
```

为了读取图像，使用了 cv2.imread()方法。此方法从指定文件加载图像。如果无法读取图像(因为缺少文件、权限不当、格式不受支持或无效)，则此方法返回一个空矩阵。

> **语法:** cv2.imread(path，flag)
> 
> ***参数:***
> ***路径:**代表待读图像路径的字符串。*
> ***标志:**它指定了应该以何种方式读取图像。它的默认值是 **cv2。**IMREAD _ COLOR*
> 
> ***返回值:**该方法返回从指定文件加载的图像。*

**注意:**图像应该在工作目录中，或者应该给出图像的完整路径。

所有三种类型的标志描述如下:

> ***cv2。**指定加载彩色图像。图像的任何透明度都将被忽略。这是默认标志。或者，我们可以为该标志传递整数值 **1** 。*
> ***cv2。IMREAD _ GRADE:**指定以灰度模式加载图像。或者，我们可以为该标志传递整数值 **0** 。*
> ***cv2。IMREAD_UNCHANGED:** 指定加载包含 alpha 通道的图像。或者，我们可以为该标志传递整数值 **-1** 。*

下面的代码是使用 OpenCV 和 matplotlib 库函数读取图像并在屏幕上显示图像的实现。

**示例#1(使用 OpenCV) :**

**使用的图像:**

![](img/c8773af5d93591c46b33a4bf4342545d.png)

## 蟒蛇 3

```py
# Python code to read image
import cv2

# To read image from disk, we use
# cv2.imread function, in below method,
img = cv2.imread("geeksforgeeks.png", cv2.IMREAD_COLOR)

# Creating GUI window to display an image on screen
# first Parameter is windows title (should be in string format)
# Second Parameter is image array
cv2.imshow("Cute Kitens", img)

# To hold the window on screen, we use cv2.waitKey method
# Once it detected the close input, it will release the control
# To the next line
# First Parameter is for holding screen for specified milliseconds
# It should be positive integer. If 0 pass an parameter, then it will
# hold the screen until user close it.
cv2.waitKey(0)

# It is for removing/deleting created GUI window from screen
# and memory
cv2.destroyAllWindows()
```

**输出:**

![](img/996f52713f26dd21ef93a947d4ed5ce4.png)

**示例#2:** 以 grascale 模式打开

## 计算机编程语言

```py
# Python program to explain cv2.imread() method

# importing cv2
import cv2

# path
path = r'geeksforgeeks.png'

# Using cv2.imread() method
# Using 0 to read image in grayscale mode
img = cv2.imread(path, 0)

# Displaying the image
cv2.imshow('image', img)
```

**输出:**

![](img/9eac563803dd3d586b153f5f3a5db1e4.png)