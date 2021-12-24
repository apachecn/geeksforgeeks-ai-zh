# 使用 OpenCV-Python 检查摄像头是否打开

> 原文:[https://www . geeksforgeeks . org/check-如果打开或未使用摄像头-opencv-python/](https://www.geeksforgeeks.org/check-if-the-camera-is-opened-or-not-using-opencv-python/)

**OpenCV** (开源计算机视觉)是一个计算机视觉库，包含对图像或视频进行操作的各种功能。OpenCV 库可以用来对视频进行多种操作。

在使用 OpenCV 用 Python 编写代码时，我们可能不确定在远端摄像头是否打开并正常工作。摄像机在安全和视频监控系统等领域发挥着至关重要的作用。在实时视频监控系统中，为了确保摄像头打开并且正常工作，我们有 OpenCV 的`isOpened()`。文章背后的想法是检查摄像头是否连接，如果发现摄像头断开连接，则会向管理员或相关人员发送邮件。

**1。检查相机是否打开/连接。**

**进场:**

*   导入必要的库(NumPy 和 OpenCV)
*   启动摄像头。这里，在`VideoCapture()-0`中表示内置网络摄像头，而 1 表示使用外部网络摄像头。
*   如果打开摄像机，我们将在帧上循环，而在另一种情况下，会出现一条消息“警报！摄像头断开”将打印在终端窗口上。

下面是实现。

```
# Python program to check
# whether the camera is opened 
# or not

import numpy as np
import cv2

cap = cv2.VideoCapture(0)
while(cap.isOpened()):

    while True:

        ret, img = cap.read()
        cv2.imshow('img', img)
        if cv2.waitKey(30) & 0xff == ord('q'):
            break

    cap.release()
    cv2.destroyAllWindows()
else:
    print("Alert ! Camera disconnected")
```

**2。如果发现摄像头断开连接/未打开，则发送邮件。**

**进场:**

*   导入必要的库(smtplib 是发送邮件的 python 库)。
*   与服务器建立连接并登录到该帐户。
*   指定收件人的电子邮件地址和要发送的消息(“提醒！摄像头断开！”在这种情况下)。
*   邮件发送后，请关闭连接或退出会话。

下面是实现。

```
# Python program to send 
# the mail

import smtplib

conn = smtplib.SMTP('smtp.gmail.com', 587)

conn.ehlo()
conn.starttls()

# Enter the sender's details
conn.login('Enter sender \'s gmail address', 
           'Enter sender\'s password')

conn.sendmail('Enter sender\'s gmail address', 
              'Enter Receiver\'s gmail address', 
              'Enter message to be sent')

conn.quit()
```