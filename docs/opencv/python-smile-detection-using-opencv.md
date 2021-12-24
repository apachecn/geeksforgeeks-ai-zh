# Python |使用 OpenCV 进行微笑检测

> 原文:[https://www . geesforgeks . org/python-微笑-检测-使用-opencv/](https://www.geeksforgeeks.org/python-smile-detection-using-opencv/)

情感检测器用于许多行业，其中一个是媒体行业，在这个行业中，公司确定公众对其产品的反应非常重要。在本文中，我们将使用 OpenCV 构建一个微笑检测器，该检测器从网络摄像头获取实时反馈。我们将要实现的微笑/幸福检测器将是一个原始的，有很多更好的方法来实现它。
**第一步:**首先，我们需要导入 OpenCV 库。

```py
import cv2
```

**步骤#2:** 包括所需的哈尔级联。
哈尔级联是一种分类器，用于通过在人脸片段上叠加预定义的模式来检测(在这种情况下是人脸的)特征，并用作 XML 文件。在我们的模型中，我们将使用脸，眼睛和微笑哈尔-喀斯喀斯，下载后需要放在工作目录中。
所有需要的哈尔-喀斯喀特可以在这里[找到](https://github.com/opencv/opencv/tree/master/data/haarcascades)。

## 蟒蛇 3

```py
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades +'haarcascade_frontalface_default.xml')
eye_cascade = cv2.CascadeClassifier(cv2.data.haarcascades +'haarcascade_eye.xml')
smile_cascade = cv2.CascadeClassifier(cv2.data.haarcascades +'haarcascade_smile.xml')
```