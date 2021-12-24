# Python–使用 OpenCV 处理视频图像

> 原文:[https://www . geesforgeks . org/python-process-images-of-a-video-use-opencv/](https://www.geeksforgeeks.org/python-process-images-of-a-video-using-opencv/)

处理视频意味着逐帧对视频执行操作。帧只不过是视频在单个时间点的特定实例。我们可能在一秒钟内有多个帧。帧可以被视为类似于图像。
因此，无论我们对图像执行什么操作，也可以对帧执行。让我们用例子来看一些操作。

## 自适应阈值–

通过使用这种技术，我们可以对帧的小区域应用阈值处理。所以整体框架的集体价值是不一样的。

## 蟒蛇 3

```
# importing the necessary libraries
import cv2
import numpy as np

# Creating a VideoCapture object to read the video
cap = cv2.VideoCapture('sample.mp4')

# Loop until the end of the video
while (cap.isOpened()):

    # Capture frame-by-frame
    ret, frame = cap.read()
    frame = cv2.resize(frame, (540, 380), fx = 0, fy = 0,
                         interpolation = cv2.INTER_CUBIC)

    # Display the resulting frame
    cv2.imshow('Frame', frame)

    # conversion of BGR to grayscale is necessary to apply this operation
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)

    # adaptive thresholding to use different threshold
    # values on different regions of the frame.
    Thresh = cv2.adaptiveThreshold(gray, 255, cv2.ADAPTIVE_THRESH_MEAN_C,
                                           cv2.THRESH_BINARY_INV, 11, 2)

    cv2.imshow('Thresh', Thresh)
    # define q as the exit button
    if cv2.waitKey(25) & 0xFF == ord('q'):
        break

# release the video capture object
cap.release()
# Closes all the windows currently opened.
cv2.destroyAllWindows()
```