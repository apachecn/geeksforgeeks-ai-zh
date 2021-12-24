# Python |使用 OpenCV 的哈里斯角点检测方法进行角点检测

> 原文:[https://www . geesforgeks . org/python-corner-detection-with-Harris-corner-detection-method-use-opencv/](https://www.geeksforgeeks.org/python-corner-detection-with-harris-corner-detection-method-using-opencv/)

**哈里斯角点检测**算法被开发用于识别图像的内部角点。图像的角基本上被识别为在所有可能的维度和方向上梯度的大强度存在变化的区域。提取的角点可以是图像特征的一部分，可以与其他图像的特征相匹配，可以用来提取准确的信息。哈里斯角点检测是一种从输入图像中提取角点并从输入图像中提取特征的方法。

**关于使用的功能:**

> **语法:**cv 2 . cornerrelis(src、dest、blockSize、kSize、freeParameter、borderType)
> 
> **参数:**
> **src**–输入图像(单通道、8 位或浮点)
> **dest**–存储哈里斯检测器响应的图像。大小与源图像相同
> **块大小**–邻域大小(针对每个像素值考虑块大小*块大小邻域)
> **ksize**–用于 [Sobel()](https://docs.opencv.org/2.4/modules/imgproc/doc/filtering.html#void%20Sobel(InputArray%20src, %20OutputArray%20dst, %20int%20ddepth, %20int%20dx, %20int%20dy, %20int%20ksize, %20double%20scale, %20double%20delta, %20int%20borderType)) 运算符的 Aperture 参数
> **free parameter**–Harris 检测器自由参数
> **border type**–像素外推方法(使用的外推模式返回指定外推像素对应的像素坐标)

下面是 Python 实现:

```py
# Python programe to illustrate
# corner detection with
# Harris Corner Detection Method

# organizing imports
import cv2
import numpy as np

# path to input image specified and 
# image is loaded with imread command
image = cv2.imread('GeekforGeeks.jpg')

# convert the input image into
# grayscale color space
operatedImage = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# modify the data type
# setting to 32-bit floating point
operatedImage = np.float32(operatedImage)

# apply the cv2.cornerHarris method
# to detect the corners with appropriate
# values as input parameters
dest = cv2.cornerHarris(operatedImage, 2, 5, 0.07)

# Results are marked through the dilated corners
dest = cv2.dilate(dest, None)

# Reverting back to the original image,
# with optimal threshold value
image[dest > 0.01 * dest.max()]=[0, 0, 255]

# the window showing output image with corners
cv2.imshow('Image with Borders', image)

# De-allocate any associated memory usage 
if cv2.waitKey(0) & 0xff == 27:
    cv2.destroyAllWindows()
```

**输入:**
[![](img/6bebe2698666bbbdd7e590952fe9de13.png)](https://media.geeksforgeeks.org/wp-content/uploads/download-43.png)

**输出:**
[![](img/38087f1714a12e71bf9d8b28e2a44da1.png)](https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-7-12.png)