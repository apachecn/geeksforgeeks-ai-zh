# 使用 OpenCV–Python 进行实时距离估计

> 原文:[https://www . geesforgeks . org/real-distance-estimation-use-opencv-python/](https://www.geeksforgeeks.org/realtime-distance-estimation-using-opencv-python/)

**先决条件:**[OpenCV 简介](https://www.geeksforgeeks.org/introduction-to-opencv/)

在本文中，我们将看到如何使用 Python 中的 OpenCV 通过网络摄像头计算距离。通过使用它，人们可以处理图像和视频来识别物体、人脸，甚至是人类的笔迹。本文着重于检测对象。

在本文中，我们将使用哈尔级联来进行物体检测。

### 瀑布式头发

哈尔级联分类器是一种有效的目标检测方法。哈尔级联是一种基于机器学习的方法，其中使用大量的正图像和负图像来训练分类器。

文件可以从这里下载:[for ontalface](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml)。

**距离估算步骤:**

*   Take a reference image: measure the distance from the object (face) to the camera, take a reference image and record the measured distance.
*   Measure the width of the object (face) to ensure that the reference image and the width of the object (face) keep the measurement unit. Mine [reference image](https://github.com/Asadullah-Dal17/Distance_measurement_using_single_camera/blob/main/Ref_image.png)

### **人脸检测:**

该函数将检测人脸并返回人脸宽度的像素值。这个面部数据函数只需要一个参数，即图像，返回以像素为单位的面部宽度，这是焦距探测器和距离探测器功能的要求。

## 蟒 3

```
def face_data(image):

    face_width = 0  # making face width to zero

    # converting color image to gray scale image
    gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

    # detecting face in the image
    faces = face_detector.detectMultiScale(gray_image, 1.3, 5)

    # looping through the faces detect in the
    # image getting coordinates x, y ,
    # width and height
    for (x, y, h, w) in faces:

        # draw the rectangle on the face
        cv2.rectangle(image, (x, y), (x+w, y+h), GREEN, 2)

        # getting face width in the pixels
        face_width = w

    # return the face width in pixel
    return face_width
```

### **焦距探测器:**

焦距探测器功能处理三个参数:

1.  **Measured _ distance:** It is the distance between the camera and the object when shooting the reference image, **Known _ distance = 72.2 # cm**
2.  **real _ width:** It measures the width of objects in the real world, and here we measure the width of faces around **, which is known as _ width = 14.3 # cm**
3.  **宽度 _ 英寸 _ 射频 _ 英寸**

该函数将返回焦距，用于查找距离。

## 蟒 3

```
# focal length finder function
def FocalLength(measured_distance, real_width, width_in_rf_image):
    focal_length = (width_in_rf_image* measured_distance)/ real_width
    return focal_length
```