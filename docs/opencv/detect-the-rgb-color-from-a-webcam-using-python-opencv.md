# 使用 Python–OpenCV 从网络摄像头检测 RGB 颜色

> 原文:[https://www . geeksforgeeks . org/通过网络摄像头检测 rgb 颜色-使用-python-opencv/](https://www.geeksforgeeks.org/detect-the-rgb-color-from-a-webcam-using-python-opencv/)

**先决条件:**T2【Python NumPy】T3、 [Python OpenCV](https://www.geeksforgeeks.org/opencv-python-tutorial/)

每幅图像都由红、绿、蓝三种颜色表示。让我们看看如何使用 Python 找到网络摄像头捕获的最主要的颜色。

**进场:**

1.  导入 cv2 和 NumPy 模块
2.  使用 **cv2 捕捉网络摄像头视频。VideoCapture(0)** 方法。
3.  使用 **cv2.imshow()** 方法显示当前帧。
4.  运行 while 循环，使用 **read()** 方法获取当前帧。
5.  将红色、蓝色和绿色元素存储在列表中。
6.  计算每个列表的平均值。
7.  无论哪个平均值具有最大值，都显示该颜色。

## 蟒蛇 3

```
# importing required libraries
import cv2
import numpy as np

# taking the input from webcam
vid = cv2.VideoCapture(0)

# running while loop just to make sure that
# our program keep running untill we stop it
while True:

    # capturing the current frame
    _, frame = vid.read()

    # displaying the current frame
    cv2.imshow("frame", frame) 

    # setting values for base colors
    b = frame[:, :, :1]
    g = frame[:, :, 1:2]
    r = frame[:, :, 2:]

    # computing the mean
    b_mean = np.mean(b)
    g_mean = np.mean(g)
    r_mean = np.mean(r)

    # displaying the most prominent color
    if (b_mean > g_mean and b_mean > r_mean):
        print("Blue")
    if (g_mean > r_mean and g_mean > b_mean):
        print("Green")
    else:
        print("Red")
```

**输出:**

![](img/ff1ca9069df9a0d161e53530a3da377e.png) ![](img/6d53335239953532b59cd0584cf5eb17.png)