# OpenCV Python 程序模糊图像

> 原文:[https://www . geesforgeks . org/opencv-python-program-to-blur-an-image/](https://www.geeksforgeeks.org/opencv-python-program-to-blur-an-image/)

*注意:本文包含无法使用在线编译器运行的代码。请确保您已经安装了 Python 2.7 和 cv2 模块，然后再尝试在您的系统上运行该程序。*

大家好！我读了一篇**Aditya Prakash**–<u>[OpenCV c++程序模糊一个图像](https://www.geeksforgeeks.org/opencv-c-program-to-blur-an-image/)</u> 的精彩作品，所以我决定想出类似的东西，但这次是用 Python。这是一个非常简单的程序，结果基本相同。

```py
# Python Program to blur image

# Importing cv2 module
import cv2 

# bat.jpg is the batman image.
img = cv2.imread('bat.jpg') 

# make sure that you have saved it in the same folder
# You can change the kernel size as you want
blurImg = cv2.blur(img,(10,10)) 
cv2.imshow('blurred image',blurImg)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

输出:
![](img/c9369aaa6e6f750bc96f7b716eb69631.png)

现在，上面的这个程序正在使用一种叫做**平均的图像模糊技术。**还有一些其他选项可用–**高斯模糊、中值模糊、双边滤波。**让我们在程序中添加一些内容，并比较结果。

```py
# importing opencv CV2 module
import cv2 

# bat.jpg is the batman image.
img = cv2.imread('gfg.png')

# make sure that you have saved it in the same folder
# Averaging
# You can change the kernel size as you want
avging = cv2.blur(img,(10,10))

cv2.imshow('Averaging',avging)
cv2.waitKey(0)

# Gaussian Blurring
# Again, you can change the kernel size
gausBlur = cv2.GaussianBlur(img, (5,5),0) 
cv2.imshow('Gaussian Blurring', gausBlur)
cv2.waitKey(0)

# Median blurring
medBlur = cv2.medianBlur(img,5)
cv2.imshow('Media Blurring', medBlur)
cv2.waitKey(0)

# Bilateral Filtering
bilFilter = cv2.bilateralFilter(img,9,75,75)
cv2.imshow('Bilateral Filtering', bilFilter)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

原图:
![](img/4c232a4b5d3f7b4ecdc61aed07d4fff9.png)
求平均值:
![](img/61b7762e46a6cda5efcb314f0ec50161.png)

高斯模糊:
![](img/5dca493581e43c2a79c1d43642f910a3.png)

媒体模糊:
![](img/8447c0e2502ce86bc671d8a45f1dc1e2.png)

双边过滤:
![](img/3566b2859cd53e81a3e36b764112733d.png)

希望你喜欢这个帖子！再见！

**关于作者:**

**维斯韦什·施里马里**是 BITS Pilani 的机械工程本科生。他满足了所有没有在他的分支机构教过的要求——白帽黑客、网络安全操作员和前竞争性程序员。作为 Python 力量的坚定信仰者，他的大部分作品都是同一种语言。每当他除了编程、上课、看 CSI Cyber 之外有时间的时候，他都会去散步，默默地弹吉他。他的人生格言是——“享受你的生活，因为它值得享受！”

**如果你也想在这里展示你的博客，请查看[博客](http://geeksquiz.com/gblog/)在极客博客上的客座博文。**