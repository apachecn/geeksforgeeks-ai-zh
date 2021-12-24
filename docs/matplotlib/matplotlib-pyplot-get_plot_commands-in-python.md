# Python 中的 matplotlib . pyplot . get _ plot _ commands()

> 原文:[https://www . geeksforgeeks . org/matplotlib-pyplot-get _ plot _ commands-in-python/](https://www.geeksforgeeks.org/matplotlib-pyplot-get_plot_commands-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。 **[Pyplot](https://www.geeksforgeeks.org/pyplot-in-matplotlib/)** 是一个基于状态的 Matplotlib 模块接口，它提供了一个类似 MATLAB 的接口。Pyplot 中可以使用的各种图有线图、等高线图、直方图、散点图、三维图等。

## matplotlib . pyplot . get _ plot _ commands()方法

matplotlib 库 pyplot 模块中的 **get_plot_commands()方法**用于获取所有绘图命令的排序列表。

> **语法:**matplotlib . pyplot . get _ plot _ commands()
> 
> **参数:**此方法不接受任何参数。
> 
> **返回:**该方法返回所有绘图命令的排序列表。

下面的例子说明了 matplotlib.pyplot . get _ plot _ commands()函数在 matplotlib . py plot 中的作用:

**示例:**

```
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt

w = plt.get_plot_commands()

print("List of all of the plotting commands : ")
for i in w:
    print(i)
```

**输出:**

```
List of all of the plotting commands : 
acorr
angle_spectrum
annotate
arrow
autoscale
axes
axhline
axhspan
axis
axvline
axvspan
bar
barbs
barh
box
boxplot
broken_barh
cla
clabel
clf
clim
close
cohere
colorbar
contour
contourf
csd
delaxes
draw
errorbar
eventplot
figimage
figlegend
fignum_exists
figtext
figure
fill
fill_between
fill_betweenx
findobj
gca
gcf
gci
get_figlabels
get_fignums
grid
hexbin
hist
hist2d
hlines
imread
imsave
imshow
install_repl_displayhook
ioff
ion
isinteractive
legend
locator_params
loglog
magnitude_spectrum
margins
matshow
minorticks_off
minorticks_on
pause
pcolor
pcolormesh
phase_spectrum
pie
plot
plot_date
plotfile
polar
psd
quiver
quiverkey
rc
rc_context
rcdefaults
rgrids
savefig
sca
scatter
sci
semilogx
semilogy
set_cmap
setp
show
specgram
spy
stackplot
stem
step
streamplot
subplot
subplot2grid
subplot_tool
subplots
subplots_adjust
suptitle
switch_backend
table
text
thetagrids
tick_params
ticklabel_format
tight_layout
title
tricontour
tricontourf
tripcolor
triplot
twinx
twiny
uninstall_repl_displayhook
violinplot
vlines
xcorr
xkcd
xlabel
xlim
xscale
xticks
ylabel
ylim
yscale
yticks
```