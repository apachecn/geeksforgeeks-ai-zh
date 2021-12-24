# 使用 Python-OpenCV 使用自定义种子进行轮廓检测

> 原文:[https://www . geesforgeks . org/contour-detection-with-custom-seeds-use-python-opencv/](https://www.geeksforgeeks.org/contour-detection-with-custom-seeds-using-python-opencv/)

本文讨论了如何通过单击图像来动态检测轮廓，并为图像的不同部分分配不同的颜色。轮廓是形状分析和目标检测与识别的非常有用的工具。该程序使用 [OpenCV](https://www.geeksforgeeks.org/introduction-to-opencv/) 、 [Numpy](https://www.geeksforgeeks.org/python-numpy/) 和 [Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 库。它还使用内置的 OpenCV 分水岭算法来检测轮廓。

### 要求

*   Python 和 OpenCV 必须安装在本地机器上。
*   安装 Jupyter 笔记本，方便调试。
*   这里，Matplotlib 的 colormap 用于获得不同的颜色。在下面给出的例子中，我们将使用 tab10。你可以选择不同的颜色图。不同颜色参考[本](https://matplotlib.org/examples/color/colormaps_reference.html)站点。

### 说明

*   运行程序。
*   单击您想要制作轮廓的图像。
*   通过按从零到九的数字，为图像的不同部分选择不同的颜色。(一个数字代表一种颜色)

下面是实现。

## 蟒 3

```py
# Import modules
import cv2
import numpy as np
import matplotlib.pyplot as plt
from matplotlib import cm

# Upload the image in the same directory and then run the code
# If image not found you may get an error
# Reading Image
road = cv2.imread('road_image.jpg')

# Making Copy of Image
road_copy = np.copy(road)

# Creating two black image of same size as original image
marker_image = np.zeros(road.shape[:2], dtype=np.int32)
segments = np.zeros(road.shape, dtype=np.uint8)

# Function to return tuple of colors
def create_rgb(i):
    x = np.array(cm.tab10(i))[:3]*255
    return tuple(x)

# Storing Colors
colors = []

# One color for each single digit
for i in range(10):
    colors.append(create_rgb(i))

# Global Variables
# Color Choices
# Number of markers
no_markers = 10

# Current markers
current_marker = 1

# Flag
marks_updated = False

# CALLBACK FUNCTION
def mouse_callback(event, x, y, flags, param):
    global marks_updated

    if event == cv2.EVENT_LBUTTONDOWN:

        # TRACKING FOR MARKERS
        cv2.circle(marker_image, (x, y), 5, (current_marker), -1)

        # DISPLAY ON USER IMAGE
        cv2.circle(road_copy, (x, y), 5, colors[current_marker], -1)

        marks_updated = True

# Naming the window and setting call back function to it
cv2.namedWindow('Road Image')
cv2.setMouseCallback('Road Image', mouse_callback)

while True:

    # Show the 2 windows
    cv2.imshow('WaterShed Segments', segments)
    cv2.imshow('Road Image', road_copy)

    # Close everything if Esc is pressed
    k = cv2.waitKey(1)
    if k == 27:
        break

    # Clear all colors and start over if 'c' is pressed
    elif k == ord('c'):
        road_copy = road.copy()
        marker_image = np.zeros(road.shape[0:2], dtype=np.int32)
        segments = np.zeros(road.shape, dtype=np.uint8)

    # If a number 0-9 is chosen index the color
    elif k > 0 and chr(k).isdigit():

        # chr converts to printable digit
        current_marker = int(chr(k))

    # If we clicked somewhere, call the watershed
    # algorithm on our chosen markers
    if marks_updated:
        marker_image_copy = marker_image.copy()
        cv2.watershed(road, marker_image_copy)
        segments = np.zeros(road.shape, dtype=np.uint8)

        for color_ind in range(no_markers):

            # COLORING SEGMENTS
            segments[marker_image_copy == (color_ind)] = colors[color_ind]

        marks_updated = False

# Destroy all the windows at the end
cv2.destroyAllWindows()
```