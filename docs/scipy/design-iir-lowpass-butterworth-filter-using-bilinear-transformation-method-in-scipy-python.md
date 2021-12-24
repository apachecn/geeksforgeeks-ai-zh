# 使用 Scipy- Python 中的双线性变换方法设计 IIR 低通巴特沃斯滤波器

> 原文:[https://www . geeksforgeeks . org/design-IIR-low-butterworth-filter-use-双线性变换-scipy-python 中的方法/](https://www.geeksforgeeks.org/design-iir-lowpass-butterworth-filter-using-bilinear-transformation-method-in-scipy-python/)

IIR 代表无限脉冲响应，它是许多线性时不变系统的显著特征之一，其特点是具有**脉冲响应 h(t)/h(n)** ，该脉冲响应在某一点后不变为零，而是无限延续。

## **什么是 IIR 低通巴特沃斯？**

它基本上就像一个普通的数字低通巴特沃兹滤波器，具有无限的脉冲响应。

**规格如下:**

*   8 千赫的采样率
*   过滤器 2 的顺序
*   截止频率 3400 赫兹

我们将绘制滤波器的幅度和相位响应。

**分步方法:**

**步骤 1:** 导入所有必要的库。

## 蟒 3

```py
# import required library
import numpy as np
import scipy.signal as signal
import matplotlib.pyplot as plt
```

**步骤 2:** 用给定的过滤器规格定义变量。

## 蟒 3

```py
# Given specification
N = 2  # Order of the filter
Fs = 8000  # Sampling frequency in Hz
fc = 3400  # Cut-off frequency in Hz

# Compute Design Sampling parameter
Td = 1/Fs
```

**第三步:**计算截止频率

## python 3

```py
# Compute cut-off frequency in radian/sec
wd = 2*np.pi*fc
print(wd)  # Cut-off frequency in radian/sec
```