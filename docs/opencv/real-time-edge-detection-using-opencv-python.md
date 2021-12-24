# 利用 Python 中的 OpenCV 进行实时边缘检测| Canny 边缘检测方法

> 原文:[https://www . geesforgeks . org/实时-边缘检测-使用-opencv-python/](https://www.geeksforgeeks.org/real-time-edge-detection-using-opencv-python/)

给定程序的目标是实时执行图像的边缘检测。本文采用流行的 canny 边缘检测算法来检测图像中的大范围边缘。OpenCV 内置函数 cv2。Canny()将我们的输入图像作为第一个参数，其孔径大小(最小值和最大值)作为最后两个参数。这是一个如何在 Python 中检测边缘的简单示例。

**下载要求的步骤如下:**

1.  下载 Python 2.7.x 版本、numpy 和 OpenCV 2.7.x 或 3.1.0 版本。检查您的 Windows 位或 64 位是否兼容，并相应地安装。
2.  确保 numpy 在 python 中运行，然后尝试安装 opencv。

**实施
T2】**

```
# OpenCV program to perform Edge detection in real time
# import libraries of python OpenCV 
# where its functionality resides
import cv2 

# np is an alias pointing to numpy library
import numpy as np

# capture frames from a camera
cap = cv2.VideoCapture(0)

# loop runs if capturing has been initialized
while(1):

    # reads frames from a camera
    ret, frame = cap.read()

    # converting BGR to HSV
    hsv = cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)

    # define range of red color in HSV
    lower_red = np.array([30,150,50])
    upper_red = np.array([255,255,180])

    # create a red HSV colour boundary and 
    # threshold HSV image
    mask = cv2.inRange(hsv, lower_red, upper_red)

    # Bitwise-AND mask and original image
    res = cv2.bitwise_and(frame,frame, mask= mask)

    # Display an original image
    cv2.imshow('Original',frame)

    # finds edges in the input image image and
    # marks them in the output map edges
    edges = cv2.Canny(frame,100,200)

    # Display edges in a frame
    cv2.imshow('Edges',edges)

    # Wait for Esc key to stop
    k = cv2.waitKey(5) & 0xFF
    if k == 27:
        break

# Close the window
cap.release()

# De-allocate any associated memory usage
cv2.destroyAllWindows() 
```

输出:

[![output](img/c025cef3407ebf9dcd5a012bb5891204.png)](https://media.geeksforgeeks.org/wp-content/uploads/op2.jpg)

**参考文献:**

*   http://docs.opencv.org/2.4/doc/tutorials/imgproc/imgtrans/canny_detector/canny_detector.html
*   http://docs.opencv.org/trunk/da/d22/tutorial_py_canny.html
*   https://en.wikipedia.org/wiki/Canny_edge_detector
*   http://www.ijcsmc.com/docs/papers/July2013/V2I7201329.pdf

本文由 **阿夫扎尔·安萨里** 供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。