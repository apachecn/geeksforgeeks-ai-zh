# Python OpenCV–waitKeyEx()函数

> 原文:[https://www . geesforgeks . org/python-opencv-waitkeyex-function/](https://www.geeksforgeeks.org/python-opencv-waitkeyex-function/)

**Python OpenCv waitKeyEx()方法**与 waitKey()方法类似，但它也返回完整的密钥代码。返回的关键代码是特定于实现的，并且取决于所使用的后端:QT/GTK/Win32/等等。

> **语法:** cv2.waitKey(延迟)
> 
> **参数:**
> 
> *   **延迟:**窗口需要被破坏的时间，以毫秒为单位。如果给定 0，它将无限期等待，直到按下任何键来破坏窗口。
> 
> **返回:**该方法返回被按下按键的全键码。如果没有按键，返回-1。

### 例 1:

在下面的例子中，我们实现了 waitKeyEx()方法，我们制作了一个窗口，它有一个名为“gfg_logo.png”的图像，然后我们显示它，使用 waitKeyEx()方法，我们延迟关闭窗口，然后按键关闭它。我们将返回值存储在 full_key_code 变量中并打印出来。

## 计算机编程语言

```
# importing cv2 module
import cv2

# read the image
img = cv2.imread("gfg_logo.png")

# showing the image
cv2.imshow('gfg', img)

# waiting using waitKeyEX method and storing
# the returned value in full_key_code
full_key_code = cv2.waitKeyEx(0)

# printing the variable
print("The key code is:"+str(full_key_code))
```

**输出:**

```
The key code is:13
```

在输出中，full_key_code 的值将根据按下的键来打印。当我们按回车键时，打印的值如下。

### 例 2:

我们可以看到的另一个例子是，我们不按任何键，等待窗口在给定的延迟后自动销毁。我们将通过 5000 作为参数等待 5 秒钟，然后一个窗口将自动关闭，不需要按任何键。在这种情况下，由于没有按键，该功能将返回-1。

## 计算机编程语言

```
# importing cv2 module
import cv2

# read the image
img = cv2.imread("gfg_logo.png")

# showing the image
cv2.imshow('gfg', img)

# waiting using waitKeyEX method and
# storing the returned value in full_key_code
full_key_code = cv2.waitKeyEx(5000)

# printing the variable
print("The key code is:"+str(full_key_code))
```

**输出:**

```
The key code is:-1
```