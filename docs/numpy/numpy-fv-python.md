# Python 中的 numpy.fv()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-Fv-python/

**numpy.fv(rate，nper，pmt，pv，when = 'end') :** 该金融功能帮助用户计算未来价值。

**参数:**

> **利率:**【标量或(M，数组)】每期十进制(非百分比)利率
> **nper :** 【标量或(M，数组)】总复利期
> **pmt :** 【标量或(M，数组)】固定支付
> **pv :** 【标量或(M，数组)】现值
> **当:**开始时(当= {'begin '，1})或结束时默认值为{'end '，0}

**返回:**

```
value at the end of nper periods

```

**正在求解的方程:**

```
fv + pv*(1+rate)**nper +
pmt*(1 + rate*when)/rate*((1 + rate)**nper - 1) == 0
```

或者**当速率== 0 时**

```
fv + pv + pmt * nper == 0
```

**代码 1:工作**

```
# Python program explaining fv() function

import numpy as np
'''
Question : 

Future value after 10 years of saving $100 now, 
with an additional monthly savings of $100. 
Assume the interest rate is 5% (annually) 
compounded monthly ?
'''

#                 rate       np      pmt    pv
Solution = np.fv(0.05/12, 10*12, -100, -100)

print("Solution : ", Solution)
```

**输出:**

```
Solution :  15692.9288943

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . Fv . html # numpy . Fv](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.fv.html#numpy.fv)
。