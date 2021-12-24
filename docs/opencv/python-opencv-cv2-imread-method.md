# Python OpenCV | cv2.imread()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-imread-method/](https://www.geeksforgeeks.org/python-opencv-cv2-imread-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。
`cv2.imread()`方法从指定文件加载图像。如果无法读取图像(因为缺少文件、权限不当、格式不受支持或无效)，则此方法返回一个空矩阵。

> **语法:** cv2.imread(path，flag)
> 
> **参数:**
> **路径:**代表待读图像路径的字符串。
> **标志:**指定读取图像的方式。它的默认值是 **cv2。IMREAD_COLOR**
> 
> **返回值:**该方法返回从指定文件加载的图像。

**注意:**图像应该在工作目录中，或者应该给出图像的完整路径。

所有三种类型的标志描述如下:

> **cv2。IMREAD_COLOR:** 指定加载彩色图像。图像的任何透明度都将被忽略。这是默认标志。或者，我们可以为该标志传递整数值 **1** 。
> **cv2。IMREAD _ GRADE:**指定以灰度模式加载图像。或者，我们可以为该标志传递整数值 **0** 。
> **cv2。IMREAD_UNCHANGED:** 指定加载包含 alpha 通道的图像。或者，我们可以为该标志传递整数值 **-1** 。

**图像用于以下所有示例:**
![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例#1:** 使用默认标志

```py
# Python program to explain cv2.imread() method

# importing cv2 
import cv2

# path
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks.png'

# Using cv2.imread() method
img = cv2.imread(path)

# Displaying the image
cv2.imshow('image', img)
```

**输出:**
![](img/996f52713f26dd21ef93a947d4ed5ce4.png)

**示例#2:**
以**灰度**模式加载图像

```py
# Python program to explain cv2.imread() method

# importing cv2 
import cv2

# path
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks.png'

# Using cv2.imread() method
# Using 0 to read image in grayscale mode
img = cv2.imread(path, 0)

# Displaying the image
cv2.imshow('image', img)
```

**输出:**
![](img/9eac563803dd3d586b153f5f3a5db1e4.png)