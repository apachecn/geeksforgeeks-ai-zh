# Python OpenCV–获取和设置像素

> 原文:[https://www . geesforgeks . org/python-opencv-get-and-setting-pixels/](https://www.geeksforgeeks.org/python-opencv-getting-and-setting-pixels/)

在本文中，我们将讨论通过 Python 中的 OpenCV 获取和设置像素。

图像由像素组成。像素将被表示为阵列。这 3 个整数以相同的顺序表示红、绿、蓝的强度。RGB 模式下的[0，0，0]代表黑色。还有其他模式-

*   hsv 色彩模型
*   灰度等级
*   减色系统

可以使用 [imread()](https://www.geeksforgeeks.org/python-opencv-cv2-imread-method/) 函数读取图像，该函数返回像素矩阵(默认为 RGB 模式)。

**使用的图像:**

![](img/20648dd36df67499fbbaf373412b93d0.png)

**语法:**

```
For Image shape: image.shape
For getting a pixel: image[row][col]
For setting a pixel: image[row][col] = [r,g,b]
```

**示例 1** :显示图像细节的 Python 代码

## 蟒蛇 3

```
# import cv2 module
import cv2

# resd the image
img = cv2.imread('image.png')

# shape prints the tuple (height,weight,channels)
print(img.shape)

# img will be a numpy array of the above shape
print(img)
```

**输出:**

```
(225, 225, 3)
[[[ 87 157  14]
 [ 87 157  14]
 [ 87 157  14]
 ...
 [ 87 157  14]
 [ 87 157  14]
 [ 87 157  14]]

[[ 87 157  14]
 [ 87 157  14]
 [ 87 157  14]
 ...
 [ 87 157  14]
 [ 87 157  14]
 [ 87 157  14]]

...

[[ 72 133   9]
 [ 72 133   9]
 [ 72 133   9]
 ...
 [ 87 157  14]
 [ 87 157  14]
 [ 87 157  14]]

[[ 72 133   9]
 [ 72 133   9]
 [ 72 133   9]
 ...
 [ 87 157  14]
 [ 87 157  14]
 [ 87 157  14]]]
```

这里有 225*225 个像素，每个像素都是 3 个整数(红、绿、蓝)的数组。

**例 2** :在本例中，可以使用索引提取单个像素。

## 蟒蛇 3

```
import cv2

# read the image
img = cv2.imread('image.png')

# this is pixel of 0th row and 0th column
print(img[0][0])
```

**输出:**

```
[ 87 157  14]
```

**例 3** :在图像上做黑色十字的 Python 代码。

为此，我们将提取所有(I，j)，使得 **i==j 或 i+j ==图像宽度**并且对于具有索引(I，j)的所有像素，像素的值将设置为[0，0，0]。

## 蟒蛇 3

```
# import the cv2 package
import cv2

# read the image
img = cv2.imread('image.png')
for i, row in enumerate(img):

  # get the pixel values by iterating
    for j, pixel in enumerate(img):
        if(i == j or i+j == img.shape[0]):

                # update the pixel value to black
            img[i][j] = [0, 0, 0]

# display image
cv2.imshow("output", img)
cv2.imwrite("output.png", img)
```

**输出:**

![](img/60b34bea89b22d2af2c2c0def8df0df1.png)

**示例 4:** 获得灰度，那么像素将只是一个代表白色强度的数字。

## 蟒蛇 3

```
import cv2
img = cv2.imread('image.png', 0)

# shape prints the tuple (height,weight,channels)
print("image shape = ", img.shape)

# img will be a numpy array of the above shape
print("image array = ", img)

print("pixel at index (5,5): ", img[5][5])
```

**灰度图像:**

![](img/d7a36005adc8758a112f2f41d9f164f0.png)

**输出:**

```
image shape =  (225, 225)
image array =  
[[106 106 106 ... 106 106 106]
 [106 106 106 ... 106 106 106]
 [106 106 106 ... 106 106 106]
 ...
 [ 88  88  88 ... 106 106 106]
 [ 88  88  88 ... 106 106 106]
 [ 88  88  88 ... 106 106 106]]
pixel at index (5,5):  106
```