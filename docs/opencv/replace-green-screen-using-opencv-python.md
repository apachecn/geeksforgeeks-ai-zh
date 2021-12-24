# 使用 OpenCV- Python 替换绿屏

> 原文:[https://www . geesforgeks . org/replace-green-screen-use-opencv-python/](https://www.geeksforgeeks.org/replace-green-screen-using-opencv-python/)

**先决条件:** [OpenCV Python 教程](https://www.geeksforgeeks.org/opencv-python-tutorial/)
OpenCV(开源计算机视觉)是一个计算机视觉库，包含对图片或视频执行操作的各种功能。这个库是跨平台的，因为它可以在多种编程语言上使用，如 Python、C++等。
绿屏移除在 VFX 工业中用于改变场景。在这里，我们将使用**Opencv–Python**来做同样的事情。

### 方法:

1.  导入所有必要的库
2.  加载图像或视频
3.  将图像和视频调整到相同的大小
4.  加载绿色的 BGR 上限值和下限值
5.  应用掩码，然后使用按位“与”
6.  从原始绿屏图像中减去按位“与”
7.  减法后检查矩阵值 0，并用第二个图像替换它
8.  你会得到想要的结果。

下面是实现。

## 蟒蛇 3

```
import cv2
import numpy as np

video = cv2.VideoCapture("green.mp4")
image = cv2.imread("bg.jpeg")

while True:

    ret, frame = video.read()

    frame = cv2.resize(frame, (640, 480))
    image = cv2.resize(image, (640, 480))

    u_green = np.array([104, 153, 70])
    l_green = np.array([30, 30, 0])

    mask = cv2.inRange(frame, l_green, u_green)
    res = cv2.bitwise_and(frame, frame, mask = mask)

    f = frame - res
    f = np.where(f == 0, image, f)

    cv2.imshow("video", frame)
    cv2.imshow("mask", f)

    if cv2.waitKey(25) == 27:
        break

video.release()
cv2.destroyAllWindows()
```