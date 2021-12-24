# 使用 Python–OpenCV 获得视频时长

> 原文:[https://www . geesforgeks . org/get-video-duration-using-python-opencv/](https://www.geeksforgeeks.org/get-video-duration-using-python-opencv/)

**先决条件:**

*   [开简历昂儒昂](https://www.geeksforgeeks.org/opencv-python-tutorial/)
*   [日期时间模块](https://www.geeksforgeeks.org/python-datetime-module-with-examples/)

OpenCV 是最受欢迎的跨平台库之一，它被广泛用于深度学习、图像处理、视频捕获等。在本文中，我们将学习如何使用 python 和计算机视觉获得给定视频的持续时间。

## 装置

Opencv 可以通过在终端上运行给定的命令来下载:

```
pip install Opencv
```

## 方法

要获取视频的时长，必须遵循以下步骤:

*   Import the required module.
*   Create a VideoCapture object by providing the video URL to the VideoCapture () method.

**语法:**

```
VideoCapture("url")
```

*   Provide cv2 to count the total number of frames and frames per second of a given video. CAP_PROP_FRAME_COUNT and cv2\. CAP_PROP_FPS to get () method.
*   The video duration is calculated by framing and fps in seconds.
*   Similarly, the timedelta () method is used to calculate the video time.

**语法:**

```
timedelta(time)
```

下面是实现。

## 蟒 3

```
# import module
import cv2
import datetime

# create video capture object
data = cv2.VideoCapture('C:/Users/Asus/Documents/videoDuration.mp4')

# count the number of frames
frames = data.get(cv2.CAP_PROP_FRAME_COUNT)
fps = int(data.get(cv2.CAP_PROP_FPS))

# calculate dusration of the video
seconds = int(frames / fps)
video_time = str(datetime.timedelta(seconds=seconds))
print("duration in seconds:", seconds)
print("video time:", video_time)
```

**输出:**

```
duration in seconds: 32
video time: 0:00:28
```