# Python 中的 numpy.rate()

> 原文:[https://www.geeksforgeeks.org/numpy-rate-in-python/](https://www.geeksforgeeks.org/numpy-rate-in-python/)

**`numpy.pmt(rate, nper, pv, fv, when = ‘end’)` :** 该金融功能帮助用户计算每期利率。

> **参数:**
> **nper :** 【标量或(M，)数组】合计复合周期
> **pmt :** 【标量或(M，)数组】Payment
> **fv :** 【标量或(M，)数组】Future value
> **pv :** 【标量或(M，)数组】present value
> **when:**开头(when = {'begin '，1})或默认值为{'end '，0}
> 
> **收益率:**每期利率。

**正在求解的方程:**

> Fv+PV *(1 +费率)**nper + pmt*(1 +费率*当)/费率*(1+费率)* * nper–1)= 0
> 
> 或者**当速率== 0 时**T2【Fv+PV+PMT * nper = = 0

**代码:**

```py
# Python program explaining 
# rate() function 
import numpy as np 

#                 nper  pmt   pv   fv 
Solution = np.rate(6, 10000, 500, 200) 

print("Solution= rate ", Solution) 
```

**输出:**

```py
Solution= rate  -2.024705182882783
```