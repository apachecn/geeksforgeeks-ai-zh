# Python |使用 OpenCV 的背景减法

> 原文:[https://www . geesforgeks . org/python-背景-减法-使用-opencv/](https://www.geeksforgeeks.org/python-background-subtraction-using-opencv/)

**背景减除**在日常生活中有几个用例，它被用于对象分割、安全增强、行人跟踪、统计访客数量、交通中的车辆数量等。它能够学习和识别前景遮罩。
顾名思义，它能够减去或消除图像中的背景部分。它的输出是一个二进制分割图像，本质上给出了图像中非静止物体的信息。在这种寻找非静止部分的概念中存在一个问题，因为运动物体的阴影可以是运动的，并且有时被分类在前景中。
流行的背景减除算法有:

*   【background 减法公式:是一种基于高斯混合的背景分割算法。
*   **background 减法公式 2** :它使用了相同的概念，但是它提供的主要优点是即使在亮度发生变化时也具有稳定性，并且对帧中的阴影具有更好的识别能力。
*   **几何多重网格**:利用统计方法和每像素贝叶斯分割算法。

## 蟒蛇 3

```
# Python code for Background subtraction using OpenCV
import numpy as np
import cv2

cap = cv2.VideoCapture('/home/sourabh/Downloads/people-walking.mp4')
fgbg = cv2.createBackgroundSubtractorMOG2()

while(1):
    ret, frame = cap.read()

    fgmask = fgbg.apply(frame)

    cv2.imshow('fgmask', fgmask)
    cv2.imshow('frame',frame )

    k = cv2.waitKey(30) & 0xff
    if k == 27:
        break

cap.release()
cv2.destroyAllWindows()
```