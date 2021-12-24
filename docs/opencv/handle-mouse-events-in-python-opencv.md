# 用 Python 处理鼠标事件–OpenCV

> 原文:[https://www . geesforgeks . org/handle-mouse-events-in-python-opencv/](https://www.geeksforgeeks.org/handle-mouse-events-in-python-opencv/)

**OpenCV** 是最受欢迎的计算机视觉库之一。如果你想开始你在计算机视觉领域的旅程，那么彻底理解 OpenCV 的概念是至关重要的。

**注:**详见[OpenCV 简介](http://geeksforgeeks.org/introduction-to-opencv/)

## 处理鼠标事件

OpenCV 有时有助于控制和管理不同类型的鼠标事件，并为我们提供了管理它们的灵活性。可以有不同类型的鼠标事件，如左键点击、右键点击、双击等。为了管理这些事件，我们需要在 OpenCV 打开窗口或框架时为每种类型的鼠标点击事件设计回调函数。回调函数将有助于通过特定的鼠标点击事件实现您想要的功能类型。

下面的代码展示了我们如何使用右键单击和左键单击事件来执行操作。

**代码:**

```
import cv2

# read image
img = cv2.imread('image.jpg')

# show image
cv2.imshow('image', img)

#define the events for the
# mouse_click.
def mouse_click(event, x, y, 
                flags, param):

    # to check if left mouse 
    # button was clicked
    if event == cv2.EVENT_LBUTTONDOWN:

        # font for left click event
        font = cv2.FONT_HERSHEY_TRIPLEX
        LB = 'Left Button'

        # display that left button 
        # was clicked.
        cv2.putText(img, LB, (x, y), 
                    font, 1, 
                    (255, 255, 0), 
                    2) 
        cv2.imshow('image', img)

    # to check if right mouse 
    # button was clicked
    if event == cv2.EVENT_RBUTTONDOWN:

        # font for right click event
        font = cv2.FONT_HERSHEY_SCRIPT_SIMPLEX
        RB = 'Right Button'

        # display that right button 
        # was clicked.
        cv2.putText(img, RB, (x, y),
                    font, 1, 
                    (0, 255, 255),
                    2)
        cv2.imshow('image', img)

cv2.setMouseCallback('image', mouse_click)

cv2.waitKey(0)

# close all the opened windows.
cv2.destroyAllWindows()
```

**输出:**

<video class="wp-video-shortcode" id="video-388108-1" width="665" height="374" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200324221203/handle-mouse-events-python-opencv.webm?_=1">[https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200324221203/handle-mouse-events-python-opencv.webm](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200324221203/handle-mouse-events-python-opencv.webm)</video>