# 使用 Python 中的 OpenCV 打开多个颜色窗口进行捕捉

> 原文:[https://www . geesforgeks . org/open-多色-windows-to-capture-using-opencv-in-python/](https://www.geeksforgeeks.org/opening-multiple-color-windows-to-capture-using-opencv-in-python/)

OpenCV 是一个开源的计算机视觉库，与许多编程语言一起工作，并提供了理解计算机视觉主题的广阔范围。在这个例子中，我们将使用 OpenCV 打开系统的摄像头，并以两种不同的颜色捕获视频。
**方法:**利用下面 OpenCV-Python 中可用的库，我们将打开两个不同的窗口，一个窗口将以彩色形式显示实时相机结果，另一个窗口将以灰度(黑色和白色)显示相同的结果。代码如下
使用的库:

*   cv2
*   numpy

安装 openCV 时，cv2 库会自动安装。要安装 numpy，请在 cmd/linux 终端使用以下命令:
`pip install numpy`

```py
# importing the required modules
import cv2
import numpy as np

# capturing from the first camera attached
cap = cv2.VideoCapture(0)

# will continue to capture until 'q' key is pressed
while True:
    ret, frame = cap.read()

    # Capturing in grayscale
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)

    cv2.imshow('frame', frame)
    cv2.imshow('gray', gray)

    # Program will terminate when 'q' key is pressed
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# Releasing all the resources
cap.release()
cv2.destroyAllWindows()
```

输出:

<video class="wp-video-shortcode" id="video-224659-1" width="665" height="416" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/uploads/Screencast_Sunday-11-March-2018_090739-IST.webm.webm?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/Screencast_Sunday-11-March-2018_090739-IST.webm.webm](https://media.geeksforgeeks.org/wp-content/uploads/Screencast_Sunday-11-March-2018_090739-IST.webm.webm)</video>

**在自己的系统上运行上面的代码，这样就可以安装所需的库以及更多**