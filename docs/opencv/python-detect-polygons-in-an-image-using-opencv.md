# Python |使用 OpenCV 检测图像中的多边形

> 原文:[https://www . geesforgeks . org/python-检测-图像中的多边形-使用-opencv/](https://www.geeksforgeeks.org/python-detect-polygons-in-an-image-using-opencv/)

**方法:**我们将用于检测给定多边形形状的方法将基于根据其具有的边数对检测到的形状进行分类。例如，如果检测到的多项式有 3 条边，那么它可以被认为是三角形，如果多项式有 4 条边，那么它可以被分类为正方形或矩形。

**先决条件:**

*   确保您的计算机上已经安装了 Python3、OpenCV 和 numpy。
*   关于 OpenCV 的基础知识会有帮助–[OpenCV 的基础知识](https://www.geeksforgeeks.org/set-opencv-anaconda-environment/)
*   确保将检测到形状的图像保存在本地目录中

**实现:**在下面的代码中，我们将从图像‘arrow . jpg’中检测一个箭头形状的物体。形状将根据它的边数来检测

**代码:检测图像中多边形的 Python 程序**

```
# Python code to detect an arrow (seven-sided shape) from an image.
import numpy as np
import cv2

# Reading image
img2 = cv2.imread('arrow.jpg', cv2.IMREAD_COLOR)

# Reading same image in another variable and 
# converting to gray scale.
img = cv2.imread('arrow.jpg', cv2.IMREAD_GRAYSCALE)

# Converting image to a binary image 
# (black and white only image).
_,threshold = cv2.threshold(img, 110, 255, 
                            cv2.THRESH_BINARY)

# Detecting shapes in image by selecting region 
# with same colors or intensity.
contours,_=cv2.findContours(threshold, cv2.RETR_TREE,
                            cv2.CHAIN_APPROX_SIMPLE)

# Searching through every region selected to 
# find the required polygon.
for cnt in contours :
    area = cv2.contourArea(cnt)

    # Shortlisting the regions based on there area.
    if area > 400: 
        approx = cv2.approxPolyDP(cnt, 
                                  0.009 * cv2.arcLength(cnt, True), True)

        # Checking if the no. of sides of the selected region is 7.
        if(len(approx) == 7): 
            cv2.drawContours(img2, [approx], 0, (0, 0, 255), 5)

# Showing the image along with outlined arrow.
cv2.imshow('image2', img2) 

# Exiting the window if 'q' is pressed on the keyboard.
if cv2.waitKey(0) & 0xFF == ord('q'): 
    cv2.destroyAllWindows()
```

**注:**阈值中的参数‘110’可以根据需要调整，如果物体是不同颜色的，并且是基于试错。

**结果:**

**带箭头的图像**

![Arrow](img/909b099b572e5afd6689f0e31ba09a16.png)

**二值图像**

![Binary Image](img/29fd71959f39349d6cbc2a181e46c5b8.png)

**轮廓箭头**

![Outlined Arrow](img/e163feeeeb33367e793db75ba9e87674.png)