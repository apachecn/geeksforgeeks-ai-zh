# 使用 Matplotlib

在 Python 中绘制相位谱

> 原文:[https://www . geeksforgeeks . org/plot-the-phase-spectrum-in-python-using-matplotlib/](https://www.geeksforgeeks.org/plot-the-phase-spectrum-in-python-using-matplotlib/)

一个**信号**是一个电磁场或者电流来传输数据。信号有各种成分，如频率、振幅、波长、相位、角频率和描述它的周期。
周期信号可以用下面的正弦函数表示:

```
y = A sin(w*t + Q)

```

其中`A`代表周期信号的振幅(单位:米)`w`代表频率(单位:赫兹)`t`代表时间周期(单位:秒)`Q`代表相位(单位:弧度)。

周期信号的两个主要成分频率和相位定义了该信号的**相位谱**。周期信号的频率分量绘制在水平轴上，周期信号的相位分量绘制在垂直轴上。

在 Python 中，Python `matplotlib`库的`pyplot`模块中的`phase_spectrum()`方法绘制了周期信号的相位谱。以下是一些演示使用`phase_spectrum()`方法可视化不同周期信号相位谱的程序。
**例 1:**

```
# importing modules
import numpy
from matplotlib import pyplot 

# assigning time values of the signal
# initial time period, final time period and phase angle
signalTime = numpy.arange(5, 10, 0.25);

# getting the amplitude of the signal
signalAmplitude = numpy.sin(signalTime)

# plotting the signal 
pyplot.plot(signalTime, signalAmplitude, color ='green')
pyplot.show()

pyplot.xlabel('Time')
pyplot.ylabel('Amplitude')
pyplot.title("Signal")

# plotting the phase spectrum of the signal 
pyplot.phase_spectrum(signalAmplitude, color ='green')

pyplot.title("Phase Spectrum of the Signal")
pyplot.show()
```

**输出:**
![](img/e81bca8a1a5d3464d8216f6ba1cb3877.png)
![](img/5ceed36b26a7a11e22b58f9cb423a68b.png)
第一张图表示振幅对时间分量中的信号，第二张图表示相位对频率图中的信号的相位谱，通过对具有从 5 到 10 秒的时间周期、0.25 弧度相位角的信号使用`phase_spectrum()`，从给定的时间周期计算信号的频率，并且使用`numpy`模块中的`sin()`功能计算信号的振幅。
**例 2:**

```
# importing modules
import numpy
from matplotlib import pyplot 

# assigning time values of the signal
# initial time period, final time period and phase angle
signalTime = numpy.arange(0, 1, 0.1)

# getting the amplitude of the signal
signalAmplitude = numpy.sin(signalTime)

# plotting the signal 
pyplot.plot(signalTime, signalAmplitude, color ='green')
pyplot.show()

pyplot.xlabel('Time')
pyplot.ylabel('Amplitude')
pyplot.title("Signal")

# plotting the phase spectrum of the signal 
pyplot.phase_spectrum(signalAmplitude, color ='green')

pyplot.title("Phase Spectrum of the Signal")
pyplot.show()
```

**输出:**
![](img/a72966d164fc7a37f73eeaa7994ed894.png)
![](img/f509a3b4eb3b1654be2362d70671f0df.png)
在上面的程序中，由于信号的振幅随时间增加，所以在第一个图形中没有形成正弦波。信号存在于 0 到 1 秒的时间周期内，相位角为 0.1 弧度，信号的相位谱用`phase_spectrum()`方法描绘。

**例 3:**

```
# importing modules
import numpy
from matplotlib import pyplot 

# assigning time values of the signal
# initial time period, final time period and phase angle 
signalTime = numpy.arange(1, 100, 0.5);

# getting the amplitude of the signal
signalAmplitude = numpy.sin(signalTime)

# plotting the signal 
pyplot.plot(signalTime, signalAmplitude, color ='green')
pyplot.show()

pyplot.xlabel('Time')
pyplot.ylabel('Amplitude')
pyplot.title("Signal")

# plotting the phase spectrum of the signal 
pyplot.phase_spectrum(signalAmplitude, color ='green')

pyplot.title("Phase Spectrum of the Signal")
pyplot.show()
```

**输出:**
![](img/3354db3d6267716a46e1550b7cc666ab.png)
![](img/2317b23ef1f3cf20f2db9781e8cefd48.png)
这里，信号用振幅对时间图表示，振幅对时间图形成正弦波，信号的相位谱用相位对频率图中的`phase_spectrum()`方法表示。信号的时间周期从 1 秒到 100 秒开始，相位角为 0.5 弧度。