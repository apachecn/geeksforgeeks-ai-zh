# 从 OpenCV 2 过渡到 OpenCV 3.x

> 原文:[https://www . geesforgeks . org/transition-from-opencv-2-to-opencv-3-x/](https://www.geeksforgeeks.org/transition-from-opencv-2-to-opencv-3-x/)

OpenCV 是最受欢迎和使用最多的计算机视觉库之一。它包含执行图像和视频处理的工具。

当 OpenCV 3..4.1 是 OpenCV 2.4 的改进版本，因为它引入了新的算法和功能。虽然一些现有的模块被重写并转移到子模块。在本文中，我将重点介绍在 OpenCV 2.4 的现有模块中所做的更改，以及如何在 OpenCV 3.4.1 中实现这些更改。

### 特征检测

一些特征检测算法(FREAK、BRIEF、SIFT 和 SURF)已被移至 o *pencv_contrib 资源库*和 *xfeatures2d* 模块。SIFT 和 SURF 算法由它们的创作者申请专利，并且是非免费的。虽然它们可以用于教育和研究目的。

**SIFT :** 创建 SIFT 特征检测器对象。

```
# OpenCV 2.4
sift = cv2.SIFT()

# OpenCV 3.4.1
sift = cv2.xfeatures2d.SIFT_create()
```

****SURF:****创建 SURF 特征检测器对象

```
# OpenCV 2.4
surf = cv2.SURF()

# OpenCV 3.4.1
surf = cv2.xfeatures2d.SURF_create()
```

**T21】FAST:**创建 FAST 检测器对象

```
# OpenCV 2.4
fast = cv2.FastFeatureDetector()

# OpenCV 3.4.1
fast = cv2.FastFeatureDetector_create()
```

****ORB**:**创建 ORB 检测器对象

```
# OpenCV 2.4
orb = cv2.ORB()

# OpenCV 3.4.1
orb = cv2.ORB_create()
```

**简单斑点检测器**

```
# OpenCV 2.4
detector = cv2.SimpleBlobDetector()

# OpenCV 3.4.1
detector = cv2.SimpleBlobDetector_create()
```

T35】CIRCLE DETECTION

OpenCV 使用

```
# OpenCV 3.4.1
circles = cv2.HoughCircles(img, cv2.HOUGH_GRADIENT, 4, 10)
```

方法名称由 2.4 版的`CV_HOUGH_GRADIENT`改为 3.4 版的`HOUGH_GRADIENT`。

### CONTOURS

最初`findContours()`函数在 OpenCV 2.4 中只返回了两个参数。在 OpenCV 3.2 之后，该函数被修改以返回三个参数，即修改后的图像、轮廓和层次。

```
# OpenCV 2.4
contours, hierarchy = cv2.findContours(img, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_NONE)

# OpenCV 3.4.1
im, contours, hierarchy = cv2.findContours(img, cv2.RETR_EXTERNAL, 
                                           cv2.CHAIN_APPROX_NONE)
```

这些是在将代码从 OpenCV 2 .4 迁移到 OpenCV 3.x 时可能有用的一些重要更改。