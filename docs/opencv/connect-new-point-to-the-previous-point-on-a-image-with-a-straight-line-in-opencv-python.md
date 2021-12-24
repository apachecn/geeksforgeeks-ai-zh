# 在 Opencv-Python 中用直线将新点连接到图像上的前一点

> 原文:[https://www . geeksforgeeks . org/connect-new-point-to-the-previous-point-on-a-image-in-open cv-python 中的一条直线/](https://www.geeksforgeeks.org/connect-new-point-to-the-previous-point-on-a-image-with-a-straight-line-in-opencv-python/)

[**OpenCV-Python**](https://www.geeksforgeeks.org/opencv-python-tutorial/)是一个旨在解决计算机视觉问题的 Python 绑定库。让我们看看如何用直线将新点连接到图像上的前一点。

**第一步:**在图像上画点:

在一个图像上我们可以使用[**cv2 . circle()**](https://www.geeksforgeeks.org/python-opencv-cv2-circle-method/)方法来标记点。这种方法用于在任何图像上画一个圆。

> **语法:** cv2 .圆(图像，中心坐标，半径，颜色，厚度)
> 
> **参数:**该方法取以下参数:
> 
> *   **图像:**就是要画圆的图像。
> *   **中心 _ 坐标:**是圆的中心坐标。坐标表示为两个值的元组(即 **X** 坐标值， **Y** 坐标值)。
> *   **半径:**就是圆的半径。
> *   **颜色:**是要画的圆的边界线的颜色。对于 **BGR** ，我们传递一个元组。例如:(255，0，0)代表蓝色。
> *   **厚度:**是 **px** 中圆边界线的厚度。 **-1 px** 的厚度会以指定的颜色填充矩形。
> 
> **返回:**返回一个画有圆圈的图像。

**第二步:**通过直线连接两点:

我们可以使用[**cv2 . line()**](https://www.geeksforgeeks.org/python-opencv-cv2-line-method/)方法在一个图像上连接两个点。此方法用于在任何图像上画线。

> **语法:** cv2 .圆(图像，中心坐标，半径，颜色，厚度)
> 
> **参数:该方法取以下参数:**
> 
> *   **图像:**就是要画圆的图像。
> *   **中心 _ 坐标:**是圆的中心坐标。坐标表示为两个值的元组(即 **X** 坐标值， **Y** 坐标值)。
> *   **半径:**就是圆的半径。
> *   **颜色:**是要画的圆的边界线的颜色。对于 **BGR** ，我们传递一个元组。例如:(255，0，0)代表蓝色。
> *   **厚度:**是 **px** 中圆边界线的厚度。 **-1 px** 的厚度会以指定的颜色填充矩形。
> 
> **返回值:**返回一个上面画了一条线的图像。

下面是实现:

## 蟒蛇 3

```
# importing required packages
import cv2
import numpy as np

# mouse call back function
def click_event(event, x, y,
                flags, params):

    # if the left button of mouse
    # is clicked then this
    # condition executes
    if event == cv2.EVENT_LBUTTONDOWN:

        # appending the points we
        # clicked to list
        points.append((x,y))

        # marking the point with a circle
        # of center at that point and
        # small radius
        cv2.circle(img,(x,y), 4,
                   (0, 255, 0), -1)

        # if length of points list
        # greater than2 then this
        # condition executes
        if len(points) >= 2:

            # joins the current point and
            # the previous point in the
            # list with a line
            cv2.line(img, points[-1], points[-2],
                     (0, 255, 255), 5)

        # displays the image
        cv2.imshow('image', img)

# making an black image
# of size (512,512,3)
# create 3-d numpy
# zeros array
img = np.zeros((512, 512, 3),
             np.uint8)

# declare a list to append all the
# points on the image we clicked
points = []

# show the image
cv2.imshow('image',img)

# setting mouse call back
cv2.setMouseCallback('image',
                     click_event)

# no waiting
cv2.waitKey(0)

# To close the image
# window that we opened
cv2.destroyAllWindows()
```

<video class="wp-video-shortcode" id="video-453052-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200711091736/outputimg.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200711091736/outputimg.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200711091736/outputimg.mp4)</video>