# Python OpenCv:在视频上写文字

> 原文:[https://www . geesforgeks . org/python-opencv-write-text-on-video/](https://www.geeksforgeeks.org/python-opencv-write-text-on-video/)

OpenCV 是用于计算机视觉、机器学习和图像处理的巨大开源库，现在它在实时操作中发挥着重要作用，这在当今的系统中非常重要。通过使用它，人们可以处理图像和视频来识别物体、人脸，甚至是人类的笔迹。

`cv2.putText()`方法在用户指定的期望位置的视频帧上插入文本。我们可以设计字体的类型以及颜色和粗细。

> **语法** : cv2.putText(框架、文本、组织、字体、颜色、粗细)
> 
> **参数** :
> **帧:**视频当前运行帧。
> **文本:**要插入的文本字符串。
> **org:** 文本字符串的左下角
> **字体:**要使用的字体类型。
> **颜色:**字体的颜色。
> **粗细:**字体的粗细

**示例:**

```
# Python program to write
# text on video

import cv2

cap = cv2.VideoCapture('sample_vid.mp4')

while(True):

    # Capture frames in the video
    ret, frame = cap.read()

    # describe the type of font
    # to be used.
    font = cv2.FONT_HERSHEY_SIMPLEX

    # Use putText() method for
    # inserting text on video
    cv2.putText(frame, 
                'TEXT ON VIDEO', 
                (50, 50), 
                font, 1, 
                (0, 255, 255), 
                2, 
                cv2.LINE_4)

    # Display the resulting frame
    cv2.imshow('video', frame)

    # creating 'q' as the quit 
    # button for the video
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# release the cap object
cap.release()
# close all windows
cv2.destroyAllWindows()
```

**输出:**

![python-write-to-video-opencv](img/72dafbb1947b61000f0b3d0463975434.png)