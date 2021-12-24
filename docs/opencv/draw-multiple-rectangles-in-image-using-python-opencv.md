# 使用 Python-Opencv 在图像中绘制多个矩形

> 原文:[https://www . geesforgeks . org/draw-multi-矩形-in-image-using-python-opencv/](https://www.geeksforgeeks.org/draw-multiple-rectangles-in-image-using-python-opencv/)

在本文中，我们将看到如何使用 Python 和 OpenCV 在图像中绘制多个矩形。

## 使用的功能:

*   **imread():** 在 OpenCV 中，cv2.imread()函数用于读取 Python 中的图像。

> **语法:** cv2.imread(path_of_image，flag)

*   **矩形():**在 OpenCV 中，使用 cv2.rectangle 函数在 Python 中的图像上绘制矩形。

> **语法:** cv2 .矩形(图像、起始坐标、结束坐标、颜色、厚度)

*   **imshow():** 在 OpenCV 中，cv2.imshow()函数用于显示 Python 中的图像。

> **语法:** cv2.imshow(window_name，image)

*   **waitKey():** 在 OpenCV 中，cv2.waitkey()函数允许您等待特定的时间(以毫秒为单位)。
*   **destroyAllWindows():** 在 OpenCV 中，destroyAllWindows()函数用于关闭所有使用 OpenCV 方法创建的窗口。

### **下面是实现:**

## 蟒蛇 3

```py
# importing OpenCV(cv2) module
import cv2

# Read RGB image
img = cv2.imread("D:\Naveen\gfg.PNG")

# Draw rectangles
# Red rectangle
cv2.rectangle(img, (100, 560), (700, 480),
              (0, 0, 255), 3)

# Blue rectangle
cv2.rectangle(img, (650, 450), (420, 240),
              (255, 0, 0), 5)

# Green rectangle
cv2.rectangle(img, (150, 450), (380, 240),
              (0, 255, 0), 4)

# Output img with window name as 'image'
cv2.imshow('image', img)

# Maintain output window utill
# user presses a key
cv2.waitKey(0)

# Destroying present windows on screen
cv2.destroyAllWindows()
```

**输出:**

![](img/615e53f3cc84aa893b731fe371c5d006.png)