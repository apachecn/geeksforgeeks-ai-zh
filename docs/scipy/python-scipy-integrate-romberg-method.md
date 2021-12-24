# Python | Scipy integrate . romberg()方法

> 原文:[https://www . geesforgeks . org/python-scipy-integrate-romberg-method/](https://www.geeksforgeeks.org/python-scipy-integrate-romberg-method/)

借助`**scipy.integrate.romberg()**`方法，我们可以用`scipy.integrate.romberg()`方法得到一个可调用函数从极限 a 到极限 b 的龙贝格积分。

> **语法:** `scipy.integrate.romberg(func, a, b)`
> **返回:**返回一个可调用函数的龙贝格积分值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`scipy.integrate.romberg()`方法，我们能够通过使用`scipy.integrate.romberg()`方法获得可调用函数从极限 a 到极限 b 的龙贝格积分。

```
# import numpy and scipy.integrate
import numpy as np
from scipy import integrate
gfg = lambda x: np.exp(-x**2)

# using scipy.integrate.romberg()
geek = integrate.romberg(gfg, 0, 3, show = True)

print(geek)
```

**输出:**

> ```
> Romberg integration of <function vectorize1..vfunc at 0x00000209C3641EA0> from [0, 3]
> 
>  Steps  StepSize   Results
>      1  3.000000  1.500185
>      2  1.500000  0.908191  0.710860
>      4  0.750000  0.886180  0.878843  0.890042
>      8  0.375000  0.886199  0.886206  0.886696  0.886643
>     16  0.187500  0.886205  0.886207  0.886207  0.886200  0.886198
>     32  0.093750  0.886207  0.886207  0.886207  0.886207  0.886207  0.886207
>     64  0.046875  0.886207  0.886207  0.886207  0.886207  0.886207  0.886207  0.886207
>    128  0.023438  0.886207  0.886207  0.886207  0.886207  0.886207  0.886207  0.886207  0.886207
> 
> The final result is 0.8862073482595311 after 129 function evaluations.
> 
> ```

**例 2 :**

```
# import numpy and scipy.integrate
import numpy as np
from scipy import integrate
gfg = lambda x: np.exp(-x**2) + 1 / np.sqrt(np.pi)

# using scipy.integrate.romberg()
geek = integrate.romberg(gfg, 1, 2, show = True)

print(geek)
```

**输出:**

> ```
> Romberg integration of <function vectorize1..vfunc at 0x00000209E1605400> from [1, 2]
> 
>  Steps  StepSize   Results
>      1  1.000000  0.757287
>      2  0.500000  0.713438  0.698822
>      4  0.250000  0.702909  0.699400  0.699438
>      8  0.125000  0.700310  0.699444  0.699447  0.699447
>     16  0.062500  0.699663  0.699447  0.699447  0.699447  0.699447
>     32  0.031250  0.699501  0.699447  0.699447  0.699447  0.699447  0.699447
> 
> The final result is 0.6994468414978009 after 33 function evaluations.
> 
> ```