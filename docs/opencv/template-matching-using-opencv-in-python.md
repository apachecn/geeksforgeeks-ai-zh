# 使用 Python 中的 OpenCV 进行模板匹配

> 原文:[https://www . geesforgeks . org/template-matching-using-opencv-in-python/](https://www.geeksforgeeks.org/template-matching-using-opencv-in-python/)

**模板匹配**是一种寻找图像中与面片(模板)相似的区域的技术。
斑块是具有一定特征的小图像。模板匹配的目标是在图像中找到补丁/模板。
要找到它，用户必须给出两个输入图像:**源图像**–要在其中找到模板的图像和**模板图像(T)**–要在源图像中找到的图像。

*   它基本上是一种在较大图像中搜索和查找模板图像位置的方法。
*   这里的想法是找到与我们提供的模板匹配的图像的相同区域，给出一个阈值
    *   阈值取决于我们想要在源图像中检测模板的准确度。
    *   例如，如果我们正在应用人脸识别，并且我们想要检测一个人的眼睛，我们可以提供一个眼睛的随机图像作为模板，并搜索来源(一个人的脸)。
    *   在这种情况下，由于“眼睛”因人而异，即使我们将阈值设置为 50%(0.5)，眼睛也会被检测到。
    *   如果要搜索几乎相同的模板，阈值应该设置得很高。(t>=0.8)

**模板匹配是如何工作的？**

*   模板图像只是在输入图像上滑动(如 2D 卷积)
*   比较模板图像和模板图像下的输入图像块。
*   将获得的结果与阈值进行比较。
*   如果结果大于阈值，该部分将被标记为检测到。
*   在函数 cv2.matchTemplate(img_gray，Template，cv2)中。第一个参数是主图像，第二个参数是要匹配的模板，第三个参数是用于匹配的方法。

## 计算机编程语言

```py
# Python program to illustrate
# template matching
import cv2
import numpy as np

# Read the main image
img_rgb = cv2.imread('mainimage.jpg').

# Convert it to grayscale
img_gray = cv2.cvtColor(img_rgb, cv2.COLOR_BGR2GRAY)

# Read the template
template = cv2.imread('template',0)

# Store width and height of template in w and h
w, h = template.shape[::-1]

# Perform match operations.
res = cv2.matchTemplate(img_gray,template,cv2.TM_CCOEFF_NORMED)

# Specify a threshold
threshold = 0.8

# Store the coordinates of matched area in a numpy array
loc = np.where( res >= threshold)

# Draw a rectangle around the matched region.
for pt in zip(*loc[::-1]):
    cv2.rectangle(img_rgb, pt, (pt[0] + w, pt[1] + h), (0,255,255), 2)

# Show the final image with the matched area.
cv2.imshow('Detected',img_rgb)
```

**模板匹配的局限性:**

1.  图案引用必须保持参考图案图像(模板)的方向
2.  因此，它不适用于模板的旋转或缩放版本，如形状/大小/剪切等的变化。对象的 w.r.t .模板将给出错误的匹配。
3.  当计算中到大图像的模式相关图像时，该方法是低效的，因为该过程是耗时的。

为了避免模板和原始图像大小不同造成的问题，我们可以使用**多尺度**。在这种情况下，仅仅因为模板的尺寸与您想要匹配的图像区域的尺寸不匹配，并不意味着您不能应用模板匹配。

**模板匹配中的多尺度机制**

多重缩放的过程如下:

1.  以多种比例循环输入图像(即，使输入图像越来越小)。
2.  使用 cv2.matchTemplate 应用模板匹配，并跟踪相关系数最大的匹配(以及相关系数最大的区域的 x、y 坐标)。
3.  在所有尺度上循环之后，取相关系数最大的区域，并将其用作“匹配”区域。

## 计算机编程语言

```py
# Python program to illustrate
# multiscaling in template matching
import cv2
import numpy as np

# Read the main image
img_rgb = cv2.imread('mainimage.jpg')

# Convert to grayscale
img_gray = cv2.cvtColor(img_rgb, cv2.COLOR_BGR2GRAY)

# Read the template
template = cv2.imread('template',0)

# Store width and height of template in w and h
w, h = template.shape[::-1]
found = None

for scale in np.linspace(0.2, 1.0, 20)[::-1]:

    # resize the image according to the scale, and keep track
    # of the ratio of the resizing
    resized = imutils.resize(img_gray, width = int(img_gray.shape[1] * scale))
    r = img_gray.shape[1] / float(resized.shape[1])

    # if the resized image is smaller than the template, then break
    # from the loop
    # detect edges in the resized, grayscale image and apply template
    # matching to find the template in the image edged
    # = cv2.Canny(resized, 50, 200) result = cv2.matchTemplate(edged, template,
    # cv2.TM_CCOEFF) (_, maxVal, _, maxLoc) = cv2.minMaxLoc(result)
    # if we have found a new maximum correlation value, then update
    # the found variable if found is None or maxVal > found[0]:
    if resized.shape[0] < h or resized.shape[1] < w:
            break
    found = (maxVal, maxLoc, r)

# unpack the found variable and compute the (x, y) coordinates
# of the bounding box based on the resized ratio
(_, maxLoc, r) = found
(startX, startY) = (int(maxLoc[0] * r), int(maxLoc[1] * r))
(endX, endY) = (int((maxLoc[0] + tW) * r), int((maxLoc[1] + tH) * r))

# draw a bounding box around the detected result and display the image
cv2.rectangle(image, (startX, startY), (endX, endY), (0, 0, 255), 2)
cv2.imshow("Image", image)
cv2.waitKey(0)
```

**以上代码的分步说明:**

*   在将模板的宽度和高度存储在 w 和 r 中之后，我们初始化一个变量，该变量用于跟踪具有最佳匹配的图像的区域和比例。从那里，我们开始使用 np.linspace 函数循环图像的多个比例。此函数接受三个参数，即起始值、结束值和其间相等的区块片数。在本例中，我们将从图像原始大小的 100%开始，在 20 个大小相等的百分比块中，一直向下到原始大小的 20%。
*   然后，我们根据当前的比例调整图像的大小，并计算旧宽度与新宽度的比率——正如您稍后将看到的那样，跟踪该比率非常重要。我们进行检查以确保输入图像大于我们的模板匹配。如果模板比较大，那么我们的 cv2.matchTemplate 调用会抛出一个错误，所以如果是这种情况，我们就中断循环。
*   此时，我们可以将模板匹配应用到调整后的图像:
    *   cv2.minMaxLoc 函数接受我们的相关结果，并返回一个 4 元组，其中分别包括最小相关值、最大相关值、最小值的(x，y)坐标和最大值的(x，y)坐标。我们只对最大值和(x，y)-坐标感兴趣，所以我们保留最大值，丢弃最小值。
*   之后，我们检查图像中在每次缩放迭代中匹配的区域。从那里，我们更新我们找到的变量，以跟踪到目前为止找到的最大相关值，即最大值的(x，y)坐标，以及原始图像宽度与当前调整大小的图像宽度的比率。
*   在我们循环了图像的所有比例之后，我们解包我们找到的变量，然后计算我们的边界框的开始和结束(x，y)坐标。特别注意将边界框的坐标乘以比率，以确保坐标与输入图像的原始尺寸相匹配。
*   最后，我们绘制边界框，并将其显示在屏幕上。

本文由 **Pratima Upadhyay** 供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。