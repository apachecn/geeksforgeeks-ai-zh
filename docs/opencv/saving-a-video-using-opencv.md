# 使用 OpenCV 保存视频

> 原文:[https://www.geeksforgeeks.org/saving-a-video-using-opencv/](https://www.geeksforgeeks.org/saving-a-video-using-opencv/)

OpenCV 是一个开源的也是最受欢迎的计算机视觉库，包含多种计算机视觉算法。你可以使用 OpenCV 对图像和视频进行读取、显示、写入和许多其他操作。OpenCV 模块通常用于流行的编程语言，如 C++、Python、Java。要在 OpenCV 中保存视频，使用`cv.VideoWriter()`方法。

**注:**详见[OpenCV 简介。](https://www.geeksforgeeks.org/introduction-to-opencv/)

> **语法:** cv。视频写入器(文件名、fourcc、fps、帧大小)
> 
> **参数:**
> 
> **文件名:**输入视频文件
> **fourcc:** 用于压缩帧的编解码器的 4 字符代码
> **fps:** 视频流的帧率
> **帧大小:**帧的高度和宽度

**示例:**

```
# Python program to save a 
# video using OpenCV

import cv2

# Create an object to read 
# from camera
video = cv2.VideoCapture(0)

# We need to check if camera
# is opened previously or not
if (video.isOpened() == False): 
    print("Error reading video file")

# We need to set resolutions.
# so, convert them from float to integer.
frame_width = int(video.get(3))
frame_height = int(video.get(4))

size = (frame_width, frame_height)

# Below VideoWriter object will create
# a frame of above defined The output 
# is stored in 'filename.avi' file.
result = cv2.VideoWriter('filename.avi', 
                         cv2.VideoWriter_fourcc(*'MJPG'),
                         10, size)

while(True):
    ret, frame = video.read()

    if ret == True: 

        # Write the frame into the
        # file 'filename.avi'
        result.write(frame)

        # Display the frame
        # saved in the file
        cv2.imshow('Frame', frame)

        # Press S on keyboard 
        # to stop the process
        if cv2.waitKey(1) & 0xFF == ord('s'):
            break

    # Break the loop
    else:
        break

# When everything done, release 
# the video capture and video 
# write objects
video.release()
result.release()

# Closes all the frames
cv2.destroyAllWindows()

print("The video was successfully saved")
```

**输出:**

<video class="wp-video-shortcode" id="video-376705-1" width="640" height="480" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200227195610/opencv-video.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200227195610/opencv-video.mp4](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200227195610/opencv-video.mp4)</video>