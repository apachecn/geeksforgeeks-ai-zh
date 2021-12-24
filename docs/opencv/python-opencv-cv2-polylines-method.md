# Python OpenCV–cv2 . multilles()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-折线-方法/](https://www.geeksforgeeks.org/python-opencv-cv2-polylines-method/)

OpenCV 是用于计算机视觉、机器学习和图像处理的巨大开源库，现在它在实时操作中发挥着重要作用，这在当今的系统中非常重要。通过使用它，人们可以处理图像和视频来识别物体、人脸，甚至是人类的笔迹。当它与各种库(如 Numpuy)集成时，python 能够处理 OpenCV 数组结构进行分析。

**注意:**更多信息请参考 [OpenCV Python 教程](http://geeksforgeeks.org/opencv-python-tutorial/)

## cv2 .聚合线()

**cv2 .折线()**方法用于在任意图像上绘制多边形。

> **语法:** cv2 .折线(图像，[pts]，封闭，颜色，厚度)
> 
> **参数:**
> **图像:**就是要画圆的图像。
> **pts:** 多边形曲线阵列。
> **NPT:**多边形顶点计数器阵列。
> **ncontours:** 曲线数。
> **闭合:**表示绘制的折线是否闭合的标志。如果它们是闭合的，该函数从每条曲线的最后一个顶点到其第一个
> 顶点绘制一条线。
> **颜色:**是需要绘制折线的颜色。对于 BGR，我们传递一个元组。
> **厚度:**是折线边的厚度。
> 
> **返回值:**返回图像。

用于以下所有示例的图像:

![](img/9e0644b615a2ef693a35a09812be79ac.png)

用于以下所有示例的图像:

**示例#1:**

```
# Python program to explain 
# cv2.polylines() method 

import cv2
import numpy as np

# path
path = gfg.jpeg'

# Reading an image in default
# mode
image = cv2.imread(path)

# Window name in which image is
# displayed
window_name = 'Image'

# Polygon corner points coordinates
pts = np.array([[25, 70], [25, 160], 
                [110, 200], [200, 160], 
                [200, 70], [110, 20]],
               np.int32)

pts = pts.reshape((-1, 1, 2))

isClosed = True

# Blue color in BGR
color = (255, 0, 0)

# Line thickness of 2 px
thickness = 2

# Using cv2.polylines() method
# Draw a Blue polygon with 
# thickness of 1 px
image = cv2.polylines(image, [pts], 
                      isClosed, color, thickness)

# Displaying the image
while(1):

    cv2.imshow('image', image)
    if cv2.waitKey(20) & 0xFF == 27:
        break

cv2.destroyAllWindows()
```

**输出:**
![ cv2.polylines()](img/46a0d31f570298481d27627ac08df64d.png)

**例 2:**

```
# Python program to explain 
# cv2.polylines() method

import cv2
import numpy as np

# path
path = r'gfg.jpeg'

# Reading an image in default 
# mode
image = cv2.imread(path)

# Window name in which image is 
# displayed
window_name = 'Image'

# Polygon corner points coordinates
pts = np.array([[25, 70], [25, 145],
                [75, 190], [150, 190],
                [200, 145], [200, 70], 
                [150, 25], [75, 25]],
               np.int32)

pts = pts.reshape((-1, 1, 2))

isClosed = True

# Green color in BGR
color = (0, 255, 0)

# Line thickness of 8 px
thickness = 8

# Using cv2.polylines() method
# Draw a Green polygon with 
# thickness of 1 px
image = cv2.polylines(image, [pts], 
                      isClosed, color, 
                      thickness)

# Displaying the image
while(1):

    cv2.imshow('image', image)
    if cv2.waitKey(20) & 0xFF == 27:

        break
cv2.destroyAllWindows()
```

**输出:**
![ cv2.polylines()](img/d50785d2e89660daed638350f28ac495.png)