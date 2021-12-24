# 使用 Python-OpenCV

显示图像上点击点的坐标

> 原文:[https://www . geesforgeks . org/display-the-coordinates-on-image-using-python-opencv/](https://www.geeksforgeeks.org/displaying-the-coordinates-of-the-points-clicked-on-the-image-using-python-opencv/)

OpenCV 帮助我们控制和管理不同类型的鼠标事件，并为我们提供操作它们的灵活性。鼠标事件有多种类型。这些事件可以通过运行以下代码段来显示:

```
import cv2
[print(i) for i in dir(cv2) if 'EVENT' in i]
```

**输出:**

```
EVENT_FLAG_ALTKEY
EVENT_FLAG_CTRLKEY
EVENT_FLAG_LBUTTON
EVENT_FLAG_MBUTTON
EVENT_FLAG_RBUTTON
EVENT_FLAG_SHIFTKEY
EVENT_LBUTTONDBLCLK
EVENT_LBUTTONDOWN
EVENT_LBUTTONUP
EVENT_MBUTTONDBLCLK
EVENT_MBUTTONDOWN
EVENT_MBUTTONUP
EVENT_MOUSEHWHEEL
EVENT_MOUSEMOVE
EVENT_MOUSEWHEEL
EVENT_RBUTTONDBLCLK
EVENT_RBUTTONDOWN
EVENT_RBUTTONUP
```

现在让我们看看如何显示图像上点击的点的坐标。我们将显示右键单击和左键单击的点。

**算法:**

1.  导入 cv2 模块。
2.  使用 cv2.imread()函数导入图像。
3.  使用 cv2.imshow()函数显示图像。
4.  调用 cv2.setMouseCallback()函数，并将图像窗口和用户定义函数作为参数传递。
5.  在用户定义的函数中，使用 cv2 检查鼠标左键点击。EVENT _ LBUTTONDOWN 属性。
6.  在外壳上显示坐标。
7.  在创建的窗口上显示坐标。
8.  使用 cv2 对鼠标右键单击进行同样的操作。EVENT _ RBUTTONDOWN 属性。在图像上显示坐标时更改颜色，以区别于左键单击。
9.  在用户定义的函数之外，使用 cv2.waitKey(0)和 cv2.destroyAllWindows()函数关闭窗口并终止程序。

我们将使用彩色版本的[莉娜图像](https://en.wikipedia.org/wiki/Lenna)。

![](img/e05c7137e021914ea7df96beddbed784.png)

## 蟒蛇 3

```
# importing the module
import cv2

# function to display the coordinates of
# of the points clicked on the image
def click_event(event, x, y, flags, params):

    # checking for left mouse clicks
    if event == cv2.EVENT_LBUTTONDOWN:

        # displaying the coordinates
        # on the Shell
        print(x, ' ', y)

        # displaying the coordinates
        # on the image window
        font = cv2.FONT_HERSHEY_SIMPLEX
        cv2.putText(img, str(x) + ',' +
                    str(y), (x,y), font,
                    1, (255, 0, 0), 2)
        cv2.imshow('image', img)

    # checking for right mouse clicks    
    if event==cv2.EVENT_RBUTTONDOWN:

        # displaying the coordinates
        # on the Shell
        print(x, ' ', y)

        # displaying the coordinates
        # on the image window
        font = cv2.FONT_HERSHEY_SIMPLEX
        b = img[y, x, 0]
        g = img[y, x, 1]
        r = img[y, x, 2]
        cv2.putText(img, str(b) + ',' +
                    str(g) + ',' + str(r),
                    (x,y), font, 1,
                    (255, 255, 0), 2)
        cv2.imshow('image', img)

# driver function
if __name__=="__main__":

    # reading the image
    img = cv2.imread('lena.jpg', 1)

    # displaying the image
    cv2.imshow('image', img)

    # setting mouse handler for the image
    # and calling the click_event() function
    cv2.setMouseCallback('image', click_event)

    # wait for a key to be pressed to exit
    cv2.waitKey(0)

    # close the window
    cv2.destroyAllWindows()
```

**输出:**

<video class="wp-video-shortcode" id="video-451848-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200714083457/cv2-clicking.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200714083457/cv2-clicking.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200714083457/cv2-clicking.mp4)</video>