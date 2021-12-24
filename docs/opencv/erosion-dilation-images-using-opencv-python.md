# 使用 python 中的 OpenCV 对图像进行腐蚀和膨胀

> 原文:[https://www . geesforgeks . org/糜烂-扩张-影像-使用-opencv-python/](https://www.geeksforgeeks.org/erosion-dilation-images-using-opencv-python/)

**形态运算**是一组基于形状处理图像的运算。他们将结构化元素应用于输入图像并生成输出图像。
最基本的形态操作有两个:**侵蚀和扩张**
**侵蚀基础:**

*   侵蚀掉前景对象的边界
*   用于减少图像的特征。

**侵蚀工作:**

1.  核(奇数大小(3，5，7)的矩阵)与图像卷积。
2.  只有当内核下的所有像素都为 1 时，原始图像中的像素(1 或 0)才会被视为 1，否则，它会被侵蚀(变为零)。
3.  因此，根据内核的大小，边界附近的所有像素都将被丢弃。
4.  因此，前景对象的厚度或大小减小，或者只是图像中的白色区域减小。

**膨胀基础:**

*   增加对象面积
*   用来突出特征

**膨胀工作:**

1.  核(奇数大小(3，5，7)的矩阵)与图像卷积
2.  如果内核下至少有一个像素为“1”，则原始图像中的像素元素为“1”。
3.  它增加了图像中的白色区域或前景物体的尺寸增加

## 计算机编程语言

```py
# Python program to demonstrate erosion and
# dilation of images.
import cv2
import numpy as np

# Reading the input image
img = cv2.imread('input.png', 0)

# Taking a matrix of size 5 as the kernel
kernel = np.ones((5,5), np.uint8)

# The first parameter is the original image,
# kernel is the matrix with which image is
# convolved and third parameter is the number
# of iterations, which will determine how much
# you want to erode/dilate a given image.
img_erosion = cv2.erode(img, kernel, iterations=1)
img_dilation = cv2.dilate(img, kernel, iterations=1)

cv2.imshow('Input', img)
cv2.imshow('Erosion', img_erosion)
cv2.imshow('Dilation', img_dilation)

cv2.waitKey(0)
```

**第二张图像是原图像的侵蚀形态，第三张图像是扩张形态。**

![](img/d96a9e2799e495a9ccb7a599a3d59e19.png)

**侵蚀和扩张的用途:**

1.  侵蚀:
    *   这对于去除小的白色噪声是有用的。
    *   用于分离两个连接的对象等。
2.  膨胀:
    *   在像去除噪声这样的情况下，腐蚀之后是膨胀。因为，侵蚀去除了白噪音，但也缩小了我们的物体。所以我们扩大了它。既然噪音没了，他们就不会回来了，但是我们的物体面积增加了。
    *   它在连接对象的破损部分时也很有用。

本文由 **Pratima Upadhyay** 供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。