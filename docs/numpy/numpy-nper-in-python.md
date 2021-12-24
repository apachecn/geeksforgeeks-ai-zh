# python 中的 numpy.nper()

> 原文:[https://www.geeksforgeeks.org/numpy-nper-in-python/](https://www.geeksforgeeks.org/numpy-nper-in-python/)

**`numpy.pmt(rate, pmt, pv, fv, when = ‘end’)` :** 该金融功能帮助用户计算定期付款次数。

> **参数:**
> **利率:**【标量或(M，数组)】每期十进制(非百分比)利率
> **pmt :** 【标量或(M，数组)】支付值
> **fv :** 【标量或(M，数组)】未来值
> **pv :** 【标量或(M，数组)】现值
> **当:**期初(当默认值为{'end '，0}。
> 
> **退货:**定期付款次数。

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

how much time would it take to pay-off a loan of 
$10, 000 at 10 % annual rate of interest, if we had 
$100 to pay each month ? 
'''

# rate    pmt    pv 
Solution = np.nper(0.1 / 12, -100, 10000) 

# Here fv = 0 ; Also Default value of fv = 0 
print("Solution - No. of periods : % f months" %(Solution)) 
```

**输出:**

```py
Solution - No. of periods : 215.905777 months

```