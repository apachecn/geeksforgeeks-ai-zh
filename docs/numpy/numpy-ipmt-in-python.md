# Python 中的 numpy.ipmt()

> 原文:[https://www.geeksforgeeks.org/numpy-ipmt-in-python/](https://www.geeksforgeeks.org/numpy-ipmt-in-python/)

**`numpy.ipmt(rate, nper, pv, fv, when = ‘end’)` :** 该金融功能帮助用户只根据利息计算支付价值。即返回利息部分。

> **参数:**
> **利率:**【标量或(M，数组)】每期十进制(非百分比)利率
> **nper :** 【标量或(M，数组)】总复合期
> **fv :** 【标量或(M，数组)】未来值
> **pv :** 【标量或(M，数组)】当前值
> **当:**开始时默认值为{'end '，0}
> 
> **返回:**支付值 ie。有趣的部分。

**正在求解的方程:**

> Fv+PV *(1 +费率)**nper + pmt*(1 +费率*当)/费率*(1+费率)* * nper–1)= 0
> 
> 或者**当速率== 0 时**T2【Fv+PV+PMT * nper = = 0

**代码:**

```
# Python program explaining 
# ipmt() function 

import numpy as np 
''' 
Question : 

monthly payment needed to pay off a $10, 000 loan
in 12 years at an annual interest rate of 60 %
'''

Solution = np.ipmt(0.6 / 12, 2 * 12, 1 * 12, 10000)

# Here fv = 0 ; Also Default value of fv = 0 
print("Solution - ipmt value : ", Solution) 
```

**输出:**

```
Solution - ipmt value :  801.4432933339593

```