# 使用 Python 中的 OpenCV 添加和混合图像

> 原文:[https://www . geesforgeks . org/add-mixing-images-use-opencv-python/](https://www.geeksforgeeks.org/addition-blending-images-using-opencv-python/)

当我们谈论图像时，我们知道所有关于矩阵的信息，或者是*二值图像(0，1)* 、*灰度图像(0-255)* 或者是 *RGB 图像(255 255 255)* 。所以图像的加法就是将两个矩阵的数字相加。在 OpenCV 中，我们有一个命令 ***cv2.add()*** 来添加图像。

以下是使用 OpenCV 添加两幅图像的代码:

```py
# Python program for adding
# images using OpenCV

# import OpenCV file
import cv2

# Read Image1
mountain = cv2.imread('F:\mountain.jpg', 1)

# Read image2
dog = cv2.imread('F:\dog.jpg', 1)

# Add the images
img = cv2.add(mountain, dog)

# Show the image
cv2.imshow('image', img)

# Wait for a key
cv2.waitKey(0)

# Distroy all the window open
cv2.distroyAllWindows()
```

但是有时我们不想在图像中执行简单的加法，所以在这种情况下，我们有混合。这也是图像添加，但不同的权重赋予图像，使其给人一种混合或透明的感觉。按照以下等式添加图像:

```py
g(x) = (1 - *a*)f(x) + *a*f1(x)
```

通过将 *a* 从 0 - > 1 改变，您可以在一个图像到另一个图像之间执行冷过渡。在这里，两幅图像混合在一起。第一个图像的权重为 0.3，第二个图像的权重为 0.7，***cv2 . addweighted()***对图像应用以下等式:

```py
img = *a* . img1 + *b* . img 2 + *y*
```

这里 *y* 取零。

以下是使用 OpenCV 混合图像的代码:

```py
# Python program for blending of
# images using OpenCV

# import OpenCV file
import cv2

# Read Image1
mountain = cv2.imread('F:\mountain.jpg', 1)

# Read image2
dog = cv2.imread('F:\dog.jpg', 1)

# Blending the images with 0.3 and 0.7
img = cv2.addWeighted(mountain, 0.3, dog, 0.7, 0)

# Show the image
cv2.imshow('image', img)

# Wait for a key
cv2.waitKey(0)

# Distroy all the window open
cv2.distroyAllWindows()
```