# python 中的 numpy.pv()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-PV-python/

**numpy.fv(rate，nper，pmt，fv，when = 'end') :** 该金融功能帮助用户计算未来价值。

**参数:**

> **利率:**【array _ like】每期十进制(非百分比)利率
> **nper:**【array _ like】总复利期
> **PMT:**【array _ like】定期付款
> **Fv:**【array _ like，可选】未来值。默认值= 0.0
> **当:**在每个周期的开始(当= {'begin '，1})或结束(当= {'end '，0})时。默认值为{'end '，0}

**返回:**

```
present value as per given parameters.

```

**正在求解的方程:**

```
fv + pv*(1 + rate)**nper +
pmt*(1 + rate*when)/rate*((1 + rate)**nper - 1) = 0
```

或者**当速率== 0 时**

```
fv + pv + pmt * nper = 0
```

**代码 1:工作**

```
## Python program explaining pv() function

import numpy as np
'''
Question : 

What is the present value (e.g., the initial investment)
of an investment that needs to total $15692.93 after 10
years of saving $100 every month? 
Assume the interest rate is 5% (annually) compounded monthly.
'''

#                 rate        np       pmt   fv
Solution = np.pv(0.05/12, 10*12, -100, 15692.93)

print("present value (fv) : ", Solution)
```

**输出:**

```
present value (fv) :  -100.000671316

```

参考:
https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . PV . html