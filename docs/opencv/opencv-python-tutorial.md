# OpenCV Python 教程

> 原文:[https://www.geeksforgeeks.org/opencv-python-tutorial/](https://www.geeksforgeeks.org/opencv-python-tutorial/)

**OpenCV** 是一个巨大的开源库，用于计算机视觉、机器学习和图像处理。OpenCV 支持多种编程语言，如 Python、C++、Java 等。它可以处理图像和视频来识别物体、人脸，甚至是人类的笔迹。当它与各种库集成时，比如`[Numpy](https://www.geeksforgeeks.org/python-numpy/)`这是一个高度优化的数值运算库，那么你的武器库中的武器数量就会增加，也就是说你在 Numpy 中可以做的任何运算都可以与 OpenCV 相结合。

这个 OpenCV 教程将帮助你学习从基础到高级的图像处理，就像使用大量 Opencv 程序和项目对图像、视频进行操作一样。
![OpenCV-tutorial-python](img/583f3c7232a41c9878d43a91580a0c3d.png)

> <font size="4">**目录:**</font>
> 
> *   [入门](#getting)
> *   [处理图像](#images)
>     *   [入门](#imagesstart)
>     *   [图像处理](#processing)
>     *   [特征检测和描述](#feature)
>     *   [绘图功能](#drawing)
> *   [处理视频](#videos)
>     *   [入门](#videostart)
>     *   [视频处理](#videoprocessing)
> *   [应用和项目](#applications)

<font size="3">[**OpenCV 上最近的文章！！**](https://www.geeksforgeeks.org/tag/opencv/)</font>

**Getting Started**

*   [OpenCV–概述](https://www.geeksforgeeks.org/opencv-overview/)
*   [OpenCV 简介](https://www.geeksforgeeks.org/introduction-to-opencv/)
*   [在 Windows 上安装 Python 的 OpenCV](https://www.geeksforgeeks.org/how-to-install-opencv-for-python-in-windows/)
*   [在 Linux 上安装 Python 的 OpenCV](https://www.geeksforgeeks.org/how-to-install-opencv-for-python-in-linux/)
*   [用蟒蛇环境设置 Opencv](https://www.geeksforgeeks.org/set-opencv-anaconda-environment/)

## 使用图像

**入门**

*   [使用 Python 在 OpenCV 中读取图像](https://www.geeksforgeeks.org/reading-image-opencv-using-python/)
*   [使用 Python 在 OpenCV 中显示图像](https://www.geeksforgeeks.org/python-opencv-cv2-imshow-method/)
*   [使用 Python 在 OpenCV 中写入图像](https://www.geeksforgeeks.org/python-opencv-cv2-imwrite-method/)
*   [OpenCV |保存图像](https://www.geeksforgeeks.org/opencv-saving-an-image/)
*   [颜色空间](https://www.geeksforgeeks.org/color-spaces-in-opencv-python/)
*   [图像上的算术运算](https://www.geeksforgeeks.org/arithmetic-operations-on-images-using-opencv-set-1-addition-and-subtraction/)
*   [二进制图像的逐位运算](https://www.geeksforgeeks.org/arithmetic-operations-on-images-using-opencv-set-2-bitwise-operations-on-binary-images/)

**图像处理**

*   [图像尺寸调整](https://www.geeksforgeeks.org/image-resizing-using-opencv-python/)
*   [腐蚀图像](https://www.geeksforgeeks.org/python-opencv-cv2-erode-method/)
*   [模糊图像](https://www.geeksforgeeks.org/python-image-blurring-using-opencv/)
*   [在图像周围创建边框](https://www.geeksforgeeks.org/python-opencv-cv2-copymakeborder-method/)
*   [图像的灰度缩放](https://www.geeksforgeeks.org/python-grayscaling-of-images-using-opencv/)
*   [缩放、旋转、移动和边缘检测](https://www.geeksforgeeks.org/image-processing-in-python-scaling-rotating-shifting-and-edge-detection/)
*   [图像的腐蚀和膨胀](https://www.geeksforgeeks.org/erosion-dilation-images-using-opencv-python/)
*   [使用直方图](https://www.geeksforgeeks.org/opencv-python-program-analyze-image-using-histogram/)分析图像
*   [直方图均衡化](https://www.geeksforgeeks.org/histograms-equalization-opencv/)
*   [简单阈值化](https://www.geeksforgeeks.org/python-thresholding-techniques-using-opencv-set-1-simple-thresholding/)
*   [自适应阈值化](https://www.geeksforgeeks.org/python-thresholding-techniques-using-opencv-set-2-adaptive-thresholding/)
*   [大津阈值](https://www.geeksforgeeks.org/python-thresholding-techniques-using-opencv-set-3-otsu-thresholding/)
*   [使用阈值分割](https://www.geeksforgeeks.org/opencv-segmentation-using-thresholding/)
*   [将图像从一个颜色空间转换到另一个颜色空间](https://www.geeksforgeeks.org/python-opencv-cv2-cvtcolor-method/)
*   [用 OpenCV 过滤颜色](https://www.geeksforgeeks.org/filter-color-with-opencv/)
*   [彩色图像去噪](https://www.geeksforgeeks.org/python-denoising-of-colored-images-using-opencv/)
*   [在不同颜色空间中可视化图像](https://www.geeksforgeeks.org/python-visualizing-image-in-different-color-spaces/)
*   [找到等高线的坐标](https://www.geeksforgeeks.org/find-co-ordinates-of-contours-using-opencv-python/)
*   [双边滤波](https://www.geeksforgeeks.org/python-bilateral-filtering/)
*   [使用 OpenCV 进行图像修复](https://www.geeksforgeeks.org/image-inpainting-using-opencv/)
*   [图像上的强度变换操作](https://www.geeksforgeeks.org/python-intensity-transformation-operations-on-images/)
*   [图像配准](https://www.geeksforgeeks.org/image-registration-using-opencv-python/)
*   [背景减法](https://www.geeksforgeeks.org/python-background-subtraction-using-opencv/)
*   [使用运行平均值的概念在图像中减去背景](https://www.geeksforgeeks.org/background-subtraction-in-an-image-using-concept-of-running-average/)
*   [使用 Grabcut 算法提取图像中的前景](https://www.geeksforgeeks.org/python-foreground-extraction-in-an-image-using-grabcut-algorithm/)
*   [图像处理中的形态运算(开)](https://www.geeksforgeeks.org/python-morphological-operations-in-image-processing-opening-set-1/)
*   [图像处理中的形态运算(关闭)](https://www.geeksforgeeks.org/python-morphological-operations-in-image-processing-closing-set-2/)
*   [图像处理中的形态学运算(梯度)](https://www.geeksforgeeks.org/python-morphological-operations-in-image-processing-gradient-set-3/)
*   [使用形态学操作的图像分割](https://www.geeksforgeeks.org/image-segmentation-using-morphological-operation/)
*   [图像翻译](https://www.geeksforgeeks.org/image-translation-using-opencv-python/)
*   [图像金字塔](https://www.geeksforgeeks.org/image-pyramid-using-opencv-python/)

**Feature Detection and Description**

*   [采用霍夫线法的直线检测](https://www.geeksforgeeks.org/line-detection-python-opencv-houghline-method/)
*   [圆检测](https://www.geeksforgeeks.org/circle-detection-using-opencv-python/)
*   [检测图像的角点](https://www.geeksforgeeks.org/python-detect-corner-of-an-image-using-opencv/)
*   [用施-托马西法进行角点检测](https://www.geeksforgeeks.org/python-corner-detection-with-shi-tomasi-corner-detection-method-using-opencv/)
*   [利用哈里斯角点检测进行角点检测](https://www.geeksforgeeks.org/python-corner-detection-with-harris-corner-detection-method-using-opencv/)
*   [在图像中寻找圆和椭圆](https://www.geeksforgeeks.org/find-circles-and-ellipses-in-an-image-using-opencv-python/)
*   [文档字段检测](https://www.geeksforgeeks.org/python-document-field-detection-using-template-matching/)
*   [微笑检测](https://www.geeksforgeeks.org/python-smile-detection-using-opencv/)

**绘图功能**

*   [画线](https://www.geeksforgeeks.org/python-opencv-cv2-line-method/)
*   [画箭头线段](https://www.geeksforgeeks.org/python-opencv-cv2-arrowedline-method/)
*   [画一个椭圆](https://www.geeksforgeeks.org/python-opencv-cv2-ellipse-method/)
*   [画圆](https://www.geeksforgeeks.org/python-opencv-cv2-circle-method/)
*   [画一个矩形](https://www.geeksforgeeks.org/python-opencv-cv2-rectangle-method/)
*   [绘制文本字符串](https://www.geeksforgeeks.org/python-opencv-cv2-puttext-method/)
*   [查找并绘制轮廓](https://www.geeksforgeeks.org/find-and-draw-contours-using-opencv-python/)
*   [画一个带质心的三角形](https://www.geeksforgeeks.org/draw-a-triangle-with-centroid-using-opencv/)

## 使用视频

**入门**

*   [使用 OpenCV](https://www.geeksforgeeks.org/python-play-a-video-using-opencv/) 播放视频

**视频处理**

*   [使用多个图像创建视频](https://www.geeksforgeeks.org/python-create-video-using-multiple-images-using-opencv/)
*   [从视频中提取图像](https://www.geeksforgeeks.org/extract-images-from-video-in-python/)

## 应用程序和项目

*   [使用 OpenCV](https://www.geeksforgeeks.org/python-program-extract-frames-using-opencv/) 提取帧
*   [使用 Python-OpenCV](https://www.geeksforgeeks.org/displaying-the-coordinates-of-the-points-clicked-on-the-image-using-python-opencv/) 显示图像上点击点的坐标
*   [黑白点检测](https://www.geeksforgeeks.org/white-and-black-dot-detection-using-opencv-python/)
*   [带有跟踪条的 OpenCV BGR 调色板](https://www.geeksforgeeks.org/python-opencv-bgr-color-palette-with-trackbars/)
*   [绘制矩形并提取对象](https://www.geeksforgeeks.org/python-draw-rectangular-shape-and-extract-objects-using-opencv/)
*   [使用 OpenCV 的隐形斗篷](https://www.geeksforgeeks.org/invisible-cloak-using-opencv-python-project/)
*   [无监督人脸聚类管道](https://www.geeksforgeeks.org/ml-unsupervised-face-clustering-pipeline/)
*   [从网络摄像头保存操作视频](https://www.geeksforgeeks.org/saving-operated-video-from-a-webcam-using-opencv/)
*   [使用 Python 和 OpenCV 结合网络摄像头进行人脸检测](https://www.geeksforgeeks.org/face-detection-using-python-and-opencv-with-webcam/)
*   [打开多个颜色窗口](https://www.geeksforgeeks.org/opening-multiple-color-windows-to-capture-using-opencv-in-python/)
*   [以倒车模式播放视频](https://www.geeksforgeeks.org/python-play-video-reverse-mode-using-opencv/)
*   [使用 Python 中的 OpenCV 进行模板匹配](https://www.geeksforgeeks.org/template-matching-using-opencv-in-python/)
*   [使用 OpenCV–Python 绘制图像](https://www.geeksforgeeks.org/cartooning-an-image-using-opencv-python/)
*   [使用 Python-OpenCV 在视频帧中检测车辆](https://www.geeksforgeeks.org/opencv-python-program-vehicle-detection-video-frame/)
*   [使用 Python–OpenCV](https://www.geeksforgeeks.org/count-number-of-faces-using-python-opencv/)统计人脸数量
*   [使用 OpenCV 的实时网络摄像头绘图](https://www.geeksforgeeks.org/live-webcam-drawing-using-opencv/)
*   [从视频中实时检测识别汽车牌照](https://www.geeksforgeeks.org/detect-and-recognize-car-license-plate-from-a-video-in-real-time/)