# Python | Numpy np.gumbel()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-gum bel-method/](https://www.geeksforgeeks.org/python-numpy-np-gumbel-method/)

借助`**np.gumbel()**`方法，我们可以用`np.gumbel()`方法得到一个数组形式的 gumbel 分布。

> **语法:** `np.gumbel(value, scale, size)`
> 
> **返回:**返回甘贝尔分布的数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.gumbel()`方法，我们能够使用该方法获得 gumbel 分布的数组。

```
# import numpy
import numpy as np

# using np.gumbel() method
gfg = np.random.gumbel(12, 0.7, 20)

print(gfg)
```

**输出:**

> array([12.64947204，12.37405666，13.58474571，14.91257252，12.52167875，
> 12.4480617，14.95250558，11.70944994，12.8072181，11.6026466，【11.602264666

**例 2 :**

```
# import numpy
import numpy as np

# using np.gumbel() method
gfg = np.random.gumbel(0, 1.7, 10)

print(gfg)
```

**输出:**

> [5.34883666-0.98597658 2.35585763 1.45700115-2.62043708-0.61983442
> 1.8046374-1.73997392 4.29301495 1.82840768]