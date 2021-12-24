# 使用 Python 中的 OpenCV 将图像分成相等的部分

> 原文:[https://www . geeksforgeeks . org/使用 python 中的-opencv/](https://www.geeksforgeeks.org/dividing-images-into-equal-parts-using-opencv-in-python/)将图像分成相等的部分

在本文中，我们将看到如何使用 Python 中的 OpenCV 将图像分成相等的部分。我们熟悉 python 列表和一维列表切片。但是在这里，对于图像，我们将使用 2D 列表理解，因为图像是像素强度的 2D 矩阵。

### 使用的图像:

![](img/33b74efb771a63e7fb425fecec5cccc6.png)

## 蟒蛇 3

```py
import cv2

img = cv2.imread('img.jpg')

# cv2.imread() -> takes an image as an input
h, w, channels = img.shape

half = w//2

# this will be the first column
left_part = img[:, :half] 

# [:,:half] means all the rows and
# all the columns upto index half

# this will be the second column
right_part = img[:, half:]  

# [:,half:] means al the rows and all
# the columns from index half to the end
# cv2.imshow is used for displaying the image
cv2.imshow('Left part', left_part)
cv2.imshow('Right part', right_part)

# this is horizontal division
half2 = h//2

top = img[:half2, :]
bottom = img[half2:, :]

cv2.imshow('Top', top)
cv2.imshow('Bottom', bottom)

# saving all the images
# cv2.imwrite() function will save the image 
# into your pc
cv2.imwrite('top.jpg', top)
cv2.imwrite('bottom.jpg', bottom)
cv2.imwrite('right.jpg', right_part)
cv2.imwrite('left.jpg', left_part)
cv2.waitKey(0)
```