# 如何使用 Scipy–Python 从混合信号中提取音频波？

> 原文:[https://www . geeksforgeeks . org/如何使用 scipy-python 从混合信号中提取音频波/](https://www.geeksforgeeks.org/how-to-extract-audio-wave-from-a-mixture-of-signal-using-scipy-python/)

**先决条件:** [Scipy](https://www.geeksforgeeks.org/data-analysis-with-scipy/)

频谱分析是指分析波的频谱/响应。如标题所示，本文涉及从混合信号中提取音频波，具体过程可以解释为:

假设我们有 3 个混合音频信号，频率分别为 50Hz、1023Hz 和 1735Hz。除了这些信号之外，我们还将事先对信号进行噪声处理。光谱分析将通过使用滤波器来完成，这样我们就可以分离出信号。根据需要，我们可以根据想要提取的信号频率来调整信号。

### 方法

*   导入模块
*   指定条件，如样本数量，采样频率，内部采样时间&创建我们的混合音频波
*   给音频信号添加噪声
*   滤波器窗口的估计和截止频率的计算
*   创建一个过滤器来过滤噪音
*   绘制噪声信号、滤波器的频率响应、提取的音频波、混合音频信号的频谱、我们提取的音频信号的频谱
*   显示图

**程序:**

## 蟒蛇 3

```py
# Original, high sample rate signal
# Let us imagine this is like our analog signal
from scipy import signal
from scipy.fft import fft
import numpy as np
import matplotlib.pyplot as plt

# Number of samples
N_sample = 512

# Sampling frequency
fs = 10000

# inter sample time = 0.001s = 1kHz sampling
dt = 1/fs

# time vector
t = np.arange(0, N_sample)*dt

# Create signal vector that is the sum of 50 Hz, 1023 Hz, and 1735 Hz
Signal = np.sin(2*np.pi*50*t) + np.sin(2*np.pi*1023*t)+np.sin(2*np.pi*1735*t)

# Add random noise to the signal
Signal = Signal+np.random.normal(0, .1, Signal.shape)

# Part A: Estimation of Length and Window
# Select design  Specification
# Lower stopband frequency in Hz
fstop_L = 500

# Lower passband frequency in HZ
fpass_L = 800

# Upper stopband frequency in Hz
fstop_U = 1500

# Upper passband frequency in HZ
fpass_U = 1200

# Calculations
# Normalized lower transition band w.r.t. fs
del_f1 = abs(fpass_L-fstop_L)/fs

# Normalized upper transition band w.r.t. fs
del_f2 = abs(fpass_U-fstop_U)/fs

# Filter length using selected window based
# on Normalized lower transition band
N1 = 3.3/del_f1

# Filter length using selected window based
# on Normalized upper transition band
N2 = 3.3/del_f2
print('Filter length based on lower transition band:', N1)
print('Filter length based on upper transition band:', N2)

# Select length as the maximum of the N1 and N2
# and if it is even, make it next higher integer
N = int(np.ceil(max(N1, N2)))
if(N % 2 == 0):
    N = N+1
print('Selected filter length :', N)

# Calculate lower and uper cut-off frequencies
# Lower cut-off frequency in Hz
fL = (fstop_L+fpass_L)/2

# Upper cut-off frequency in Hz
fU = (fstop_U+fpass_U)/2

# Normalized Lower cut-off frequency in (w/pi) rad
wL = 2*fL/fs

# Normalized upper cut-off frequency in (w/pi) rad
wU = 2*fU/fs

# Cutoff frequency array
cutoff = [wL, wU]

# Since the given specification of Stopband attenuation = 50 dB
# and Passband ripple = 0.05 dB, atleast satisfy with
# Hamming window, we have to choose it.

# Determine Filter coefficients
# Call filter design function using Hamming window
b_ham = signal.firwin(N, cutoff, window="hamming", pass_zero="bandpass")

# Determine Frequency response of the filters
# Calculate response h at specified frequency
# points w for Hamming window
w, h_ham = signal.freqz(b_ham, a=1)

# Calculate Magnitude in dB
# Calculate magnitude in decibels
h_dB_ham = 20*np.log10(abs(h_ham))

a = [1]

# Filter the noisy signal by designed filter
# using signal.filtfilt
filtOut = signal.filtfilt(b_ham, a, Signal)

# Plot filter magnitude and phase responses using
# subplot. Digital frequency w converted in analog
# frequency
fig = plt.figure(figsize=(12, 18))

# Original signal
sub1 = plt.subplot(5, 1, 1)
sub1.plot(t[0:200], Signal[0:200])
sub1.set_ylabel('Amplitude')
sub1.set_xlabel('Time')
sub1.set_title('Noisy signal', fontsize=20)

# Magnitude response Plot
sub2 = plt.subplot(5, 1, 2)
sub2.plot(w*fs/(2*np.pi), h_dB_ham, 'r', label='Bandpass filter',
          linewidth='2')  # Plot for magnitude response window

sub2.set_ylabel('Magnitude (db)')
sub2.set_xlabel('Frequency in Hz')
sub2.set_title('Frequency response of Bandpass Filter', fontsize=20)
sub2.axis = ([0,  fs/2,  -110,  5])
sub2.grid()

sub3 = plt.subplot(5, 1, 3)
sub3.plot(t[0:200], filtOut[0:200], 'g', label='Filtered signal',
          linewidth='2')  # Plot for magnitude response window
sub3.set_ylabel('Magnitude ')
sub3.set_xlabel('Time')
sub3.set_title('Filtered output of Band pass Filter', fontsize=20)

# Show spectrum of noisy input signal
Sigf = fft(Signal)  # Compute FFT of noisy signal
sub4 = plt.subplot(5, 1, 4)
xf = np.linspace(0.0, 1.0/(2.0*dt), (N_sample-1)//2)
sub4.plot(xf, 2.0/N_sample * np.abs(Sigf[0:(N_sample-1)//2]))
sub4.set_ylabel('Magnitude')
sub4.set_xlabel('Frequency in Hz')
sub4.set_title('Frequency Spectrum of Original Signal', fontsize=20)
sub4.grid()

# Show spectrum of filtered output signal
Outf = fft(filtOut)  # Compute FFT of filtered signal
sub5 = plt.subplot(5, 1, 5)
xf = np.linspace(0.0, 1.0/(2.0*dt), (N_sample-1)//2)
sub5.plot(xf, 2.0/N_sample * np.abs(Outf[0:(N_sample-1)//2]))
sub5.set_ylabel('Magnitude')
sub5.set_xlabel('Frequency in Hz')
sub5.set_title('Frequency Spectrum of Filtered Signal', fontsize=20)
sub5.grid()

fig.tight_layout()
plt.show()
```

**输出:**

![](img/655d57d261355b731bca9ba37bb87f8f.png)