# Opencv 中的直方图均衡化

> 原文:[https://www . geesforgeks . org/直方图-均衡-opencv/](https://www.geeksforgeeks.org/histograms-equalization-opencv/)

先决条件:[分析-图像使用-直方图](https://www.geeksforgeeks.org/opencv-python-program-analyze-image-using-histogram)

**直方图均衡化**是图像处理中利用图像的直方图进行对比度调整的一种方法。

这种方法通常会提高许多图像的全局对比度，尤其是当图像的可用数据由接近的对比度值表示时。通过这种调整，强度可以更好地分布在直方图上。这允许局部对比度较低的区域获得较高的对比度。直方图均衡化通过有效地分散最频繁的强度值来实现这一点。该方法在背景和前景都是亮的或者都是暗的图像中是有用的。

OpenCV 有一个功能可以做到这一点，**cv2 . equation hist()**。它的输入只是灰度图像，输出是我们的直方图均衡化图像。

**输入图像:**
![](img/b3af9c5da165665ef7b294bcd15c3bd7.png)

下面是实现直方图均衡化的 Python3 代码:

```py
# import Opencv
import cv2

# import Numpy
import numpy as np

# read a image using imread
img = cv2.imread(\'F:\\do_nawab.png\', 0)

# creating a Histograms Equalization
# of a image using cv2.equalizeHist()
equ = cv2.equalizeHist(img)

# stacking images side-by-side
res = np.hstack((img, equ))

# show image input vs output
cv2.imshow(\'image\', res)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

输出: