# Python–显示使用 OpenCV 处理网络摄像头/视频文件的实时 FPS

> 原文:[https://www . geesforgeks . org/python-display-real-time-fps-at-at-web 摄像头-视频文件-正在处理-使用-opencv/](https://www.geeksforgeeks.org/python-displaying-real-time-fps-at-which-webcam-video-file-is-processed-using-opencv/)

根据我们的选择，我们将显示视频文件或网络摄像头的实时处理 FPS。
**FPS** 或**每秒帧数**或**帧率**可以定义为每秒显示的帧数。一个视频可以被假设为一组图像，或者我们可以说是以某种速率显示以产生运动的帧。如果您希望识别视频中的物体，15 fps 以上就足够了，但如果您希望识别以 40km/h 的速度行驶的车号，那么您至少需要 30 fps 才能轻松识别。因此，如果我们知道**在我们的计算机视觉项目中如何计算 FPS 就好了。**
**计算实时 FPS 的步骤:**

*   第一步是使用[cv2**创建一个视频捕获对象**。VideoCapture()](https://www.geeksforgeeks.org/python-play-a-video-using-opencv/) 。根据我们的选择，我们可以从**网络摄像头**或**视频文件**中读取视频。
*   现在我们将逐帧处理捕获的素材，直到 [**capture.read()**](https://www.geeksforgeeks.org/python-program-extract-frames-using-opencv/) 为真(此处 capture 表示一个对象，此函数还会返回 bool，并提供帧是否被成功读取的信息)。
*   为了计算 FPS，我们将记录最后一帧处理的时间和当前帧处理的结束时间。因此，一帧的处理时间将是当前时间和前一帧时间之间的时间差。

```py
Processing time for this frame = Current time – time when previous frame processed
```

**所以 fps 在当前时刻会是:**

```py
 FPS = 1/ (Processing time for this frame)
```

*   由于 FPS 总是整数，我们将把 FPS 转换成整数，然后将其类型转换成字符串，因为在框架上使用 [cv2.putText()](https://www.geeksforgeeks.org/python-opencv-cv2-puttext-method/) 显示字符串会更容易更快。现在在 **cv2.putText()** 方法的帮助下，我们将在此帧上打印 FPS，然后在[T5【cv2 . imshow()](https://www.geeksforgeeks.org/python-opencv-cv2-imshow-method/#:~:text=imshow()%20method%20is%20used, fits%20to%20the%20image%20size.&text=Parameters%3A, which%20image%20to%20be%20displayed.)功能的帮助下显示此帧。

**代码:上述方法的 Python 代码实现**

## 蟒蛇 3

```py
import numpy as np
import cv2
import time

# creating the videocapture object
# and reading from the input file
# Change it to 0 if reading from webcam

cap = cv2.VideoCapture('vid.mp4')

# used to record the time when we processed last frame
prev_frame_time = 0

# used to record the time at which we processed current frame
new_frame_time = 0

# Reading the video file until finished
while(cap.isOpened()):

    # Capture frame-by-frame

    ret, frame = cap.read()

    # if video finished or no Video Input
    if not ret:
        break

    # Our operations on the frame come here
    gray = frame

    # resizing the frame size according to our need
    gray = cv2.resize(gray, (500, 300))

    # font which we will be using to display FPS
    font = cv2.FONT_HERSHEY_SIMPLEX
    # time when we finish processing for this frame
    new_frame_time = time.time()

    # Calculating the fps

    # fps will be number of frame processed in given time frame
    # since their will be most of time error of 0.001 second
    # we will be subtracting it to get more accurate result
    fps = 1/(new_frame_time-prev_frame_time)
    prev_frame_time = new_frame_time

    # converting the fps into integer
    fps = int(fps)

    # converting the fps to string so that we can display it on frame
    # by using putText function
    fps = str(fps)

    # putting the FPS count on the frame
    cv2.putText(gray, fps, (7, 70), font, 3, (100, 255, 0), 3, cv2.LINE_AA)

    # displaying the frame with fps
    cv2.imshow('frame', gray)

    # press 'Q' if you want to exit
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# When everything done, release the capture
cap.release()
# Destroy the all windows now
cv2.destroyAllWindows()
```

**输出:以绿色显示现场 FPS 的视频文件。**

<video class="wp-video-shortcode" id="video-457808-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200602121506/perfectfi1.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200602121506/perfectfi1.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200602121506/perfectfi1.mp4)</video>