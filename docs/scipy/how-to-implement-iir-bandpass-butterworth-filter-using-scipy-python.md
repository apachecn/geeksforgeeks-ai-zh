# 如何用 Scipy–Python 实现 IIR 带通巴特沃斯滤波器？

> 原文:[https://www . geeksforgeeks . org/如何实现-IIR-带通-巴特沃斯-滤波器-使用-scipy-python/](https://www.geeksforgeeks.org/how-to-implement-iir-bandpass-butterworth-filter-using-scipy-python/)

IIR 代表无限脉冲响应，它是许多线性时不变系统的显著特征之一，其特点是具有**脉冲响应 h(t)/h(n)** ，该脉冲响应在某一点后不变为零，而是无限延续。

## **什么是 IIR 带通巴特沃斯？**

它基本上就像一个普通的数字带通巴特沃兹滤波器，具有无限的脉冲响应。

**规格如下:**

*   通带频率:1400-2100 赫兹
*   阻带频率:1050-24500 赫兹
*   通带纹波:0.4 分贝
*   阻带衰减:50 分贝
*   采样频率:7 千赫

我们将绘制滤波器的幅度、相位、脉冲和阶跃响应。

**分步方法:**

**步骤 1:** 导入所有必要的库。

## 蟒 3

```
# import required library
import numpy as np
import scipy.signal as signal
import matplotlib.pyplot as plt
```

**步骤 2:** 定义用户定义函数 ***mfreqz()和 impz()*** 。【mfreqz 是幅值和相位图的函数& impz 是脉冲和阶跃响应的函数】

## python 3

```
def mfreqz(b, a, Fs):

    # Compute frequency response of the filter
    # using signal.freqz function
    wz, hz = signal.freqz(b, a)

    # Calculate Magnitude from hz in dB
    Mag = 20*np.log10(abs(hz))

    # Calculate phase angle in degree from hz
    Phase = np.unwrap(np.arctan2(np.imag(hz), np.real(hz)))*(180/np.pi)

    # Calculate frequency in Hz from wz
    Freq = wz*Fs/(2*np.pi)

    # Plot filter magnitude and phase responses using subplot.
    fig = plt.figure(figsize=(10, 6))

    # Plot Magnitude response
    sub1 = plt.subplot(2, 1, 1)
    sub1.plot(Freq, Mag, 'r', linewidth=2)
    sub1.axis([1, Fs/2, -100, 5])
    sub1.set_title('Magnitude Response', fontsize=20)
    sub1.set_xlabel('Frequency [Hz]', fontsize=20)
    sub1.set_ylabel('Magnitude [dB]', fontsize=20)
    sub1.grid()

    # Plot phase angle
    sub2 = plt.subplot(2, 1, 2)
    sub2.plot(Freq, Phase, 'g', linewidth=2)
    sub2.set_ylabel('Phase (degree)', fontsize=20)
    sub2.set_xlabel(r'Frequency (Hz)', fontsize=20)
    sub2.set_title(r'Phase response', fontsize=20)
    sub2.grid()

    plt.subplots_adjust(hspace=0.5)
    fig.tight_layout()
    plt.show()

# Define impz(b,a) to calculate impulse response
# and step response of a system
# input: b= an array containing numerator coefficients,
# a= an array containing denominator coefficients
def impz(b, a):

    # Define the impulse sequence of length 60
    impulse = np.repeat(0., 60)
    impulse[0] = 1.
    x = np.arange(0, 60)

    # Compute the impulse response
    response = signal.lfilter(b, a, impulse)

    # Plot filter impulse and step response:
    fig = plt.figure(figsize=(10, 6))
    plt.subplot(211)
    plt.stem(x, response, 'm', use_line_collection=True)
    plt.ylabel('Amplitude', fontsize=15)
    plt.xlabel(r'n (samples)', fontsize=15)
    plt.title(r'Impulse response', fontsize=15)

    plt.subplot(212)
    step = np.cumsum(response)  # Compute step response of the system

    plt.stem(x, step, 'g', use_line_collection=True)
    plt.ylabel('Amplitude', fontsize=15)
    plt.xlabel(r'n (samples)', fontsize=15)
    plt.title(r'Step response', fontsize=15)
    plt.subplots_adjust(hspace=0.5)

    fig.tight_layout()
    plt.show()
```

**步骤 3:** 用给定的过滤器规格定义变量。

## 蟒 3

```
# Given specification
Fs = 7000  # Sampling frequency in Hz
fp = np.array([1400, 2100])  # Pass band frequency in Hz
fs = np.array([1050, 2450])  # Stop band frequency in Hz
Ap = 0.4  # Pass band ripple in dB
As = 50  # stop band attenuation in dB
```