# python opencv–getremotion matrix 2d()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-opencv-getremotion matrix 2d-function/

**cv2 . getrotationmatrix2d()**函数用于生成变换矩阵 M，该矩阵将用于旋转图像。

**语法:**

> cv2.getRotationMatrix2D(中心、角度、比例)
> 
> **参数:**
> 
> *   **中心:**旋转中心
> *   **角度(θ):** 旋转角度。逆时针方向的角度为正，顺时针方向的角度为负。
> *   **比例:**缩放图像的比例因子
> 
> **返回:** 2×3 旋转矩阵 M

M = ![\begin{bmatrix} \alpha & \beta & (1-\alpha)\cdot c_x-\beta \cdot c_y\\ -\beta & \alpha & \beta\cdot c_x+(1-\alpha) \cdot c_y \end{bmatrix}](img/4f5c26bb870e3e11582c0de8aff4a6b1.png "Rendered by QuickLaTeX.com")

哪里，

![\alpha = scale\cdot cos(\theta)\\ \beta = scale\cdot sin(\theta)\\ c_x\ and\ c_y\ are\ the\ coordinates\ of\ the\ center\ of\ the\ image.\\](img/1c6cd448745eeb3601189a501e35dd23.png "Rendered by QuickLaTeX.com")

这是一种**仿射变换。**仿射变换是保持直线和平行度的变换。warpaffine()函数将这些变换矩阵作为参数，并返回旋转后的图像。

**使用的图像:**

![](img/20648dd36df67499fbbaf373412b93d0.png)

**例 1:**

## 蟒蛇 3

```
import cv2

# Reading the image
image = cv2.imread('image.jpeg')

# Extracting height and width from 
# image shape
height, width = image.shape[:2]

# get the center coordinates of the
# image to create the 2D rotation
# matrix
center = (width/2, height/2)

# using cv2.getRotationMatrix2D() 
# to get the rotation matrix
rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=90, scale=1)

# rotate the image using cv2.warpAffine 
# 90 degree anticlockwise
rotated_image = cv2.warpAffine(
    src=image, M=rotate_matrix, dsize=(width, height))

cv2.imshow("rotated image:", rotated_image)
cv2.imwrite('rotated_image.jpg', rotated_image)
```

**输出-**

![](img/6ac15c4f304f94708ca430e7c910de19.png)

**例 2:**

## 蟒蛇 3

```
import cv2

# Reading the image
image = cv2.imread('image.jpeg')

# Extracting height and width from 
# image shape
height, width = image.shape[:2]

# get the center coordinates of the 
# image to create the 2D rotation matrix
center = (width/2, height/2)

# using cv2.getRotationMatrix2D() to get
# the rotation matrix
rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=-90, scale=1)

# rotate the image using cv2.warpAffine 90 
# degree clockwise
rotated_image = cv2.warpAffine(
    src=image, M=rotate_matrix, dsize=(width, height))

cv2.imshow("rotated image:",rotated_image)
cv2.imwrite('rotated_image.jpg', rotated_image)
```

**输出-**

![](img/e78e76cee56f0456050d1bcf98854427.png)

## 蟒蛇 3

```
import cv2

# Reading the image
image = cv2.imread('image.jpeg')

# Extracting height and width from image shape
height, width = image.shape[:2]

# get the center coordinates of the image to 
# create the 2D rotation matrix
center = (width/2, height/2)

# using cv2.getRotationMatrix2D() to get 
# the rotation matrix
rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=180, scale=1)

# rotate the image using cv2.warpAffine 180 
# degree anticlockwise
rotated_image = cv2.warpAffine(
    src=image, M=rotate_matrix, dsize=(width, height))

cv2.imshow("rotated image:", rotated_image)
cv2.imwrite('rotated_image.jpg', rotated_image)
```

**输出-**

![](img/2741db52b6f3e08893c3f249a35a9116.png)

**例 4:**

## 蟒蛇 3

```
import cv2

# Reading the image
image = cv2.imread('image.jpeg')

# Extracting height and width from image shape
height, width = image.shape[:2]

# get the center coordinates of the image to
# create the 2D rotation matrix
center = (width/2, height/2)

# using cv2.getRotationMatrix2D() to get the
# rotation matrix
rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=-180, scale=1)

# rotate the image using cv2.warpAffine 180
# degree clockwise
rotated_image = cv2.warpAffine(
    src=image, M=rotate_matrix, dsize=(width, height))

cv2.imshow("rotated image:", rotated_image)
cv2.imwrite('rotated_image.jpg', rotated_image)
```

**输出–**

![](img/2741db52b6f3e08893c3f249a35a9116.png)