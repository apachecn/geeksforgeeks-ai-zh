# 使用 Python 中的 OpenCV 连接图像

> 原文:[https://www . geeksforgeeks . org/concatenate-images-use-opencv-in-python/](https://www.geeksforgeeks.org/concatenate-images-using-opencv-in-python/)

为了用 Python 纵向和横向连接图像，cv2 库附带了两个函数:

1.  **hcontat ():** It is used as cv2.hconcat () to connect images horizontally. H here stands for level.
2.  **vcontat ():** is used as the vertical connection image of cv2.vconcat (). Here v stands for vertical.

## 在阵列上使用 hconcat()和 vconcat()实现

作为 n 维数组的图像列表被传递，其中列表中的图像被垂直或水平连接。不同大小的图像可以调整大小。下面的代码解释了连接图像的以下方法:

## python 3

```
# import cv2 library
import cv2

# read the images
img1 = cv2.imread('sea.jpg')
img2 = cv2.imread('man.jpeg')
```