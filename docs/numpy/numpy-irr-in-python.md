# Python 中的 numpy.irr()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-IRR-in-python/

**内部收益率(值):**该财务函数帮助用户计算内部收益率值，即**内部收益率**即。“平均”定期复合收益率。

![](img/816fbc5a1efcfd4d8110975446baf0d0.png)

> **参数:**
> **值:**【阵列式】输入每个时间段的现金流。净“存款”为负，净“取款”为正
> **收益:**周期输入值的内部收益率。

**代码:**

## 蟒蛇 3

```py
# Python program explaining
# irr() function

import numpy as np
'''
Question :

    Investment = 500
    Withdrawls at regular interval : 50, 31, 3, 11
'''

Solution = np.irr([-500, 50, 31, 3, 11])

print("Solution - Internal Rate of Return : ", Solution)
```

**输出:**

```py
Solution - Internal Rate of Return :  -0.5296447721512683 
```