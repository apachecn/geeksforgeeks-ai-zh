# 使用 OpenCV–Python 在视频中显示日期和时间

> 原文:[https://www . geesforgeks . org/display-date-time-in-video-use-python-opencv/](https://www.geeksforgeeks.org/display-date-and-time-in-videos-using-python-opencv/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。它可以处理图像和视频来识别物体、人脸，甚至是人的笔迹
**注:**更多信息，请参考[OpenCV 简介](https://www.geeksforgeeks.org/introduction-to-opencv/)

## 在视频中显示日期和时间

当我们处理直播视频或时长较长的视频时，有时需要在视频上显示日期和时间。时间和日期将有助于了解和分析视频中参照其时间和日期检测到的任何异常。为了在视频上显示日期和时间，我们执行以下操作。
**代号**

## 蟒蛇 3

```py
# Import libraries
import numpy
import cv2
import datetime

# open the video
vid = cv2.VideoCapture('sample.mp4')

# Process until end.
while(vid.isOpened()):
    ret, frame = vid.read()

    if ret:
        # describe the type of
        # font you want to display
        font = cv2.FONT_HERSHEY_SCRIPT_COMPLEX

        # Get date and time and
        # save it inside a variable
        dt = str(datetime.datetime.now())

        # put the dt variable over the
        # video frame
        frame = cv2.putText(frame, dt,
                            (10, 100),
                            font, 1,
                            (210, 155, 155),
                            4, cv2.LINE_8)

        # show the video
        cv2.imshow('frame', frame)

        key = cv2.waitKey(1)

        # define the key to
        # close the window
        if key == 'q' or key == 27:
            break
    else:

        break

# release the vid object
vid.release()

# close all the opened windows.
cv2.destroyAllWindows()
```