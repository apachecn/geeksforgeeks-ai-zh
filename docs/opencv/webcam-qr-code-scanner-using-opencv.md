# 使用 OpenCV 的网络摄像头二维码扫描仪

> 原文:[https://www . geesforgeks . org/网络摄像头-二维码-扫描仪-使用-opencv/](https://www.geeksforgeeks.org/webcam-qr-code-scanner-using-opencv/)

在本文中，我们将了解如何使用网络摄像头执行二维码扫描。

![](img/a1ec75da424d9d377d7d59381a9f0898.png)

网络摄像头 QR 码扫描仪

在开始之前，你需要知道这个过程将如何运作。首先你需要打开你的网络摄像头，你必须运行你的 python 程序，让它准备好扫描二维码。您可以在手机上拍摄 Qr 码图片，并在网络摄像头前显示该图片。它可以正确识别屏幕上显示的二维码。这个程序会将你重定向到隐藏在二维码中的链接。

**要求:**

```
pip install OpenCV
pip install webbrowser ( built in )
```

**步骤 1:** 要创建二维码扫描仪，您需要在命令提示符下安装 OpenCV 库。首先，需要导入 *cv2* 和浏览器*库。Cv2* 用于通过网络摄像头扫描二维码，网络浏览器用于将网址带入浏览器。

## 蟒蛇 3

```
import cv2
import webbrowser
```

**第二步:**接下来，我们需要启动摄像头捕捉二维码。为此，声明一个名为 cap 的变量，并在该变量中传递实例 *cv2。VideoCapture(0)* 。下一个过程是我们需要创建一个名为检测器的变量，并在这个变量中调用对象 *cv2。QRCodeDetector()* 。这个对象对于实时捕获二维码非常有帮助。

## 蟒蛇 3

```
cap = cv2.VideoCapture(0)
# initialize the cv2 QRCode detector
detector = cv2.QRCodeDetector()
```

**第三步:**这一步非常重要你需要创建一个*同时*循环，并在这个循环中创建一个名为 *img* 的变量，这个循环将持续读取你的网络摄像头屏幕，直到这个循环中断

## 蟒蛇 3

```
while True:
    _, img = cap.read()
```

第四步:

接下来，创建一个名为 data 的变量，这个变量用于解码二维码，如果二维码图像中存在任何数据，它将打破循环，并在您的浏览器中打开链接。这就是我在这里插入的条件。

## 蟒蛇 3

```
# detect and decode
   data, bbox, _ = detector.detectAndDecode(img)
   # check if there is a QRCode in the image
   if data:
       a=data
       break
```

第五步:

最后，调用对象 cv2.imshow 这将产生输出，您必须分配密钥来中断循环。这里我指定了一个键，叫做 q，当我们按下 q 时，它将停止视频流。

然后你必须创建变量，在这个变量中你需要调用对象 webbrowser.open(在这个对象中传递变量 a)

## 蟒蛇 3

```
cv2.imshow("QRCODEscanner", img)    
    if cv2.waitKey(1) == ord("q"):
        break

b=webbrowser.open(str(a))
cap.release()
cv2.destroyAllWindows()
```

输出:

<center>
![](img/6b65fef64dd766cfa6a3c72fd6cd9f9b.png)</center>