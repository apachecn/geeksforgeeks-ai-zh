# 不错的统计数字。JointRV()在 Python 中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/symy-stats-jointrv-in-python/

借助`**sympy.stats.JointRV()**`方法，我们可以得到代表冯米塞斯分布的连续联合随机变量。

> **语法:** `sympy.stats.JointRV(name, pdf)`
> **返回:**返回连续关节随机变量。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.stats.JointRV()`方法，我们能够使用该方法获得表示 JointRV 分布的连续联合随机变量。

```
# Import sympy and JointRV
from sympy.stats import JointRV, density
from sympy import Symbol, pprint

z = Symbol("z")
pdf = 2 * pi * z

# Using sympy.stats.JointRV() method
X = JointRV("x", pdf)
gfg = density(X)

pprint(gfg)
```

**输出:**

> jointdstributionhandmade(lambda(()，2*pi*z)，有限公司(())

**例 2 :**

```
# Import sympy and JointRV
from sympy.stats import JointRV, density
from sympy import Symbol, pprint

z = 3
pdf = 2 * pi * z

# Using sympy.stats.JointRV() method
X = JointRV("x", pdf)
gfg = density(X)

pprint(gfg)
```

**输出:**

> 6*pi