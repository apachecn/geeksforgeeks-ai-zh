# Python 中的 numpy.pmt()

> 原文:[https://www.geeksforgeeks.org/numpy-pmt-in-python/](https://www.geeksforgeeks.org/numpy-pmt-in-python/)

**`numpy.pmt(rate, nper, pv, fv, when = ‘end’)` :** 该金融功能帮助用户按照本金和利息计算支付价值。

> **参数:**
> **利率:**【标量或(M，数组)】每期十进制(非百分比)利率
> **nper :** 【标量或(M，数组)】总复合期
> **fv :** 【标量或(M，数组)】未来值
> **pv :** 【标量或(M，数组)】当前值
> **当:**开始时默认值为{'end '，0}
> 
> **返回:**支付值

**正在求解的方程:**

> Fv+PV *(1 +费率)**nper + pmt*(1 +费率*当)/费率*(1+费率)* * nper–1)= 0
> 
> 或者**当速率== 0 时**T2【Fv+PV+PMT * nper = = 0

**代码:**

```py
# Python program explaining 
# pmt() function 

import numpy as np 

''' 
Question : 

monthly payment needed to pay off a $10, 000 loan
in 12 years at an annual interest rate of 10 %
'''

# rate np  pv 
Solution = np.pmt(0.10 / 12, 12 * 12,  10, 000) 

# Here fv = 0 ; Also Default value of fv = 0 
print("Solution : ", Solution) 
```

**输出:**

```py
Solution :  -0.1195078262827336
```