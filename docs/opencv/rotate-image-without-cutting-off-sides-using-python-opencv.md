# 使用 Python–OpenCV

旋转图像而不切边

> 原文:[https://www . geesforgeks . org/rotate-image-不带切边-sides-use-python-opencv/](https://www.geeksforgeeks.org/rotate-image-without-cutting-off-sides-using-python-opencv/)

**先决条件**:[Python 中的图像处理(缩放、旋转、移位和边缘检测)](https://www.geeksforgeeks.org/image-processing-in-python-scaling-rotating-shifting-and-edge-detection/)

使用 OpenCV 旋转图像很容易，但有时简单的旋转任务会裁剪/剪切图像的侧面，从而产生半幅图像。现在，在本教程中，我们将探索一种安全旋转图像而不裁剪/剪切图像侧面的解决方案，以便整个图像都包括在旋转中，并且还将传统旋转方法与修改后的旋转版本进行比较。

**循序渐进法:**

*   为了在不切边的情况下旋转图像，我们将创建一个名为*modified way()*的显式函数，该函数将图像本身和图像旋转的角度作为参数。
*   在函数中，首先，获取图像的高度和宽度。
*   找到图像的中心。
*   然后计算 2D 旋转矩阵
*   从旋转矩阵中提取绝对 *sin* 和 *cos* 值。
*   获取图像的新高度和宽度，并更新旋转矩阵的值，以确保没有裁剪。
*   最后，使用*wrappeafy()*方法执行图像的实际旋转。

**以下是实施办法:**

## 蟒蛇 3

```py
def ModifiedWay(rotateImage, angle):

    # Taking image height and width
    imgHeight, imgWidth = rotateImage.shape[0], rotateImage.shape[1]

    # Computing the centre x,y coordinates
    # of an image
    centreY, centreX = imgHeight//2, imgWidth//2

    # Computing 2D rotation Matrix to rotate an image
    rotationMatrix = cv2.getRotationMatrix2D((centreY, centreX), angle, 1.0)

    # Now will take out sin and cos values from rotationMatrix
    # Also used numpy absolute function to make positive value
    cosofRotationMatrix = np.abs(rotationMatrix[0][0])
    sinofRotationMatrix = np.abs(rotationMatrix[0][1])

    # Now will compute new height & width of
    # an image so that we can use it in
    # warpAffine function to prevent cropping of image sides
    newImageHeight = int((imgHeight * sinofRotationMatrix) +
                         (imgWidth * cosofRotationMatrix))
    newImageWidth = int((imgHeight * cosofRotationMatrix) +
                        (imgWidth * sinofRotationMatrix))

    # After computing the new height & width of an image
    # we also need to update the values of rotation matrix
    rotationMatrix[0][2] += (newImageWidth/2) - centreX
    rotationMatrix[1][2] += (newImageHeight/2) - centreY

    # Now, we will perform actual image rotation
    rotatingimage = cv2.warpAffine(
        rotateImage, rotationMatrix, (newImageWidth, newImageHeight))

    return rotatingimage
```

**以下是一些示例，描述了如何使用上述功能旋转图像而不切边:**

**例 1:**

下面是修改后的旋转版本的实现及其与正常旋转版本的比较:

## 蟒蛇 3

```py
# Importing Required Libraries
import cv2
import numpy as np

# The below function is for conventionally way of rotating
# an Image without preventing cutting off sides
def SimpleWay(rotateImage, angle):

    # Taking image height and width
    imgHeight, imgWidth = rotateImage.shape[0], rotateImage.shape[1]

    # Computing the centre x,y coordinates
    # of an image
    centreY, centreX = imgHeight//2, imgWidth//2

    # Computing 2D rotation Matrix to rotate an image
    rotationMatrix = cv2.getRotationMatrix2D((centreY, centreX), angle, 1.0)

    # Now, we will perform actual image rotation
    rotatingimage = cv2.warpAffine(
        rotateImage, rotationMatrix, (imgWidth, imgHeight))

    return rotatingimage

# The Below function is a modified version of the
# conventional way to rotate an image without
# cropping/cutting sides.
def ModifiedWay(rotateImage, angle):

    # Taking image height and width
    imgHeight, imgWidth = rotateImage.shape[0], rotateImage.shape[1]

    # Computing the centre x,y coordinates
    # of an image
    centreY, centreX = imgHeight//2, imgWidth//2

    # Computing 2D rotation Matrix to rotate an image
    rotationMatrix = cv2.getRotationMatrix2D((centreY, centreX), angle, 1.0)

    # Now will take out sin and cos values from rotationMatrix
    # Also used numpy absolute function to make positive value
    cosofRotationMatrix = np.abs(rotationMatrix[0][0])
    sinofRotationMatrix = np.abs(rotationMatrix[0][1])

    # Now will compute new height & width of
    # an image so that we can use it in
    # warpAffine function to prevent cropping of image sides
    newImageHeight = int((imgHeight * sinofRotationMatrix) +
                         (imgWidth * cosofRotationMatrix))
    newImageWidth = int((imgHeight * cosofRotationMatrix) +
                        (imgWidth * sinofRotationMatrix))

    # After computing the new height & width of an image
    # we also need to update the values of rotation matrix
    rotationMatrix[0][2] += (newImageWidth/2) - centreX
    rotationMatrix[1][2] += (newImageHeight/2) - centreY

    # Now, we will perform actual image rotation
    rotatingimage = cv2.warpAffine(
        rotateImage, rotationMatrix, (newImageWidth, newImageHeight))

    return rotatingimage

# Driver Code

# Loading an Image from Disk
DogImage = cv2.imread("doggy.png", 1)

# Performing 40 degree rotation
NormalRotation = SimpleWay(DogImage, 40)
ModifiedVersionRotation = ModifiedWay(DogImage, 40)

# Display image on Screen
cv2.imshow("Original Image", DogImage)

# Display rotated image on Screen
cv2.imshow("Normal Rotation", NormalRotation)
cv2.imshow("Modified Version Rotation", ModifiedVersionRotation)

# To hold the GUI screen and control until it is detected
# the input for closing it, Once it is closed
# control will be released
cv2.waitKey(0)

# To destroy and remove all created GUI windows from
#screen and memory
cv2.destroyAllWindows()
```

**输出:**

![](img/411c1efcb7e12bef5a4d5ddded7fd0f6.png)

原象

![](img/7b9fa27c3802f61fadf8d64493c30f22.png)

使用 SimpleWay()函数的正常旋转

![](img/0814b83ba833df4b306853b5e07931a5.png)

带 ModifiedWay()函数的旋转

**例 2:**

下面是另一个描述现代旋转方法的例子:

## 蟒蛇 3

```py
# Importing Required Libraries
import cv2
import numpy as np

# The Below function is a modified version of the
# conventional way to rotate an image without
# cropping/cutting sides.
def ModifiedWay(rotateImage, angle):

    # Taking image height and width
    imgHeight, imgWidth = rotateImage.shape[0], rotateImage.shape[1]

    # Computing the centre x,y coordinates
    # of an image
    centreY, centreX = imgHeight//2, imgWidth//2

    # Computing 2D rotation Matrix to rotate an image
    rotationMatrix = cv2.getRotationMatrix2D((centreY, centreX), angle, 1.0)

    # Now will take out sin and cos values from rotationMatrix
    # Also used numpy absolute function to make positive value
    cosofRotationMatrix = np.abs(rotationMatrix[0][0])
    sinofRotationMatrix = np.abs(rotationMatrix[0][1])

    # Now will compute new height & width of
    # an image so that we can use it in
    # warpAffine function to prevent cropping of image sides
    newImageHeight = int((imgHeight * sinofRotationMatrix) +
                         (imgWidth * cosofRotationMatrix))
    newImageWidth = int((imgHeight * cosofRotationMatrix) +
                        (imgWidth * sinofRotationMatrix))

    # After computing the new height & width of an image
    # we also need to update the values of rotation matrix
    rotationMatrix[0][2] += (newImageWidth/2) - centreX
    rotationMatrix[1][2] += (newImageHeight/2) - centreY

    # Now, we will perform actual image rotation
    rotatingimage = cv2.warpAffine(
        rotateImage, rotationMatrix, (newImageWidth, newImageHeight))

    return rotatingimage

# Driver Code
# Loading an Image from Disk
Image = cv2.imread("gfg.png", 1)

# Performing 40 degree rotation
ModifiedVersionRotation = ModifiedWay(Image, 40)

# Display image on Screen
cv2.imshow("Original Image", Image)

# Display rotated image on Screen
cv2.imshow("Modified Version Rotation", ModifiedVersionRotation)

# To hold the GUI screen and control until it is detected
# the input for closing it, Once it is closed
# control will be released
cv2.waitKey(0)

# To destroy and remove all created GUI windows from
#screen and memory
cv2.destroyAllWindows()
```

**输出:**

![](img/d707e378c542a27d60be67a384e7be64.png) ![](img/1b7f08a283ecf7b35e29375d1bb56cfe.png)