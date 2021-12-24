# Matplotlib.pyplot.csd()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/matplot lib-pyplot-CSD-in-python/

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。 **[Pyplot](https://www.geeksforgeeks.org/pyplot-in-matplotlib/)** 是一个基于状态的接口到 **Matplotlib** 模块，它提供了一个类似于 MATLAB 的接口。

## matplotlib.pyplot.csd()函数

matplotlib 库 pyplot 模块中的 **csd()函数**用于绘制交叉光谱密度。

> **语法:** matplotlib.pyplot.csd(x，y，NFFT =无，Fs =无，Fc =无，detrend =无，window =无，noverlap =无，pad _ to =无，sides =无，scale _ by _ freq =无，return _ line =无，\*，data =无，*\*kwargs)
> 
> **参数:**该方法接受以下描述的参数:
> 
> *   **x，y:** 这些参数是数据的序列。
> *   **Fs :** 此参数为标量。它的默认值是 2。
> *   **窗口:**该参数以一个数据段为自变量，返回该段的窗口版本。其默认值为 *window_hanning()*
> *   **边:**此参数指定要返回光谱的哪些边。这可以有以下值:“默认值”、“单侧”和“双侧”。
> *   **pad_to :** 此参数包含数据段填充到的整数值。
> *   **NFFT :** 该参数包含用于快速傅立叶变换的每个块中的数据点数。
> *   **去趋势:**此参数包含在 fft 之前应用于每个分段的函数，旨在移除均值或线性趋势{ '无'，'均值'，'线性' }。
> *   **scale_by_freq :** 该参数允许对返回的频率值进行积分。
> *   **noverlap :** 此参数是块之间重叠的点数。
> *   **Fc :** 该参数为 x 的中心频率。
> *   **return_line :** 此参数包括在返回值中绘制的线对象。
> 
> **返回:**这将返回以下内容:
> 
> *   **Pxy:** 这将返回缩放前交叉光谱 P_{xy}的值。
> *   **频率:**返回 Pxy 中元素的频率。
> *   **行:**返回该函数创建的行。
> 
> 结果是 **(Pxy，freqs，line)**

下面的例子说明了 matplotlib.pyplot.csd()函数在 matplotlib.pyplot 中的作用:

**示例#1:**

```
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt

dt = 0.01
t = np.arange(0, 30, dt)
nse1 = np.random.randn(len(t))
nse2 = np.random.randn(len(t))

s1 = 1.5 * np.sin(2 * np.pi * 10 * t) + nse1
s2 = np.cos(np.pi * t) + nse2

plt.csd(s1, s2**2, 128, 1./dt)
plt.xlabel('Frequency')
plt.ylabel('CSD(db)')

plt.title('matplotlib.pyplot.csd() function Example',
          fontweight ="bold")

plt.show()
```

**输出:**
![](img/896842706a031cb72420d388a086a589.png)

**例 2:**

```
#Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt

dt = 0.01
t = np.arange(0, 30, dt)
nse1 = np.random.randn(len(t))
nse2 = np.random.randn(len(t))
r = np.exp(-t/0.05)

cnse1 = np.convolve(nse1, r, mode='same')*dt
cnse2 = np.convolve(nse2, r, mode='same')*dt

s1 = 1.5 * np.sin(2*np.pi*10*t) + cnse1
s2 = np.cos(np.pi*t) + cnse2 + np.sin(2*np.pi*10*t)

plt.plot(t, s1, t, s2)
plt.xlim(0, 5)
plt.ylabel('s1 and s2')
plt.grid(True)
plt.show()

plt.csd(s1, s2, 256, 1./dt)
plt.ylabel('CSD(db)')
plt.xlabel('Frequency')

plt.title('matplotlib.pyplot.csd() function Example'
             ,fontweight="bold")

plt.show()
```

**输出:**

![python-matplotlib-csd](img/f6994b4e9b7ddfabcf7ccc6a38e405bc.png)