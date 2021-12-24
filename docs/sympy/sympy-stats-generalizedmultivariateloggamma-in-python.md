# 症状统计。Python 中的概化多变量图形符号()

> 原文:[https://www . geesforgeks . org/sympy-stats-generated multi variatelogamma-in-python/](https://www.geeksforgeeks.org/sympy-stats-generalizedmultivariateloggamma-in-python/)

借助`**sympy.stats.GeneralizedMultivariateLogGamma()**`方法，我们可以得到代表广义多元对数伽玛分布的连续联合随机变量。

> **语法:** `GeneralizedMultivariateLogGamma(syms, delta, v, lamda, mu)`
> **参数:**
> 1)Syms–符号列表
> 2)Delta–范围[0，1]
> 3)V–正实数列表
> 4)Lambda–正实数列表
> 5)mu–正实数列表。
> **返回:**返回连续关节随机变量。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.stats.GeneralizedMultivariateLogGamma()`方法，我们能够使用该方法获得表示广义多元对数伽马分布的连续联合随机变量。

```
# Import sympy and GeneralizedMultivariateLogGamma
from sympy.stats import density
from sympy.stats.joint_rv_types import GeneralizedMultivariateLogGamma
from sympy.stats.joint_rv import marginal_distribution
from sympy import symbols, S

v = 1
l, mu = [1, 1, 1], [1, 1, 1]
d = S.Half
y = symbols('y_1:4', positive = True)

# Using sympy.stats.GeneralizedMultivariateLogGamma() method
Gd = GeneralizedMultivariateLogGamma('G', d, v, l, mu)
gfg = density(Gd)(y[0], y[1], y[2])

pprint(gfg)
```

**输出:**

```
  oo                                                      
_____                                                     
\    `                                                    
 \                                       y_1    y_2    y_3
  \     -n  (n + 1)*(y_1 + y_2 + y_3) - e    - e    - e   
   \   2  *e                                              
   /   ---------------------------------------------------
  /                            3                          
 /                        Gamma (n + 1)                   
/____,                                                    
n = 0                                                     
----------------------------------------------------------
                            2                             

```

**例 2 :**

```
# Import sympy and GeneralizedMultivariateLogGamma
from sympy.stats import density
from sympy.stats.joint_rv_types import GeneralizedMultivariateLogGamma
from sympy.stats.joint_rv import marginal_distribution
from sympy import symbols, S

v = 1
l, mu = [1, 2, 3], [2, 5, 1]
d = S.One
y = symbols('y_1:4', positive = True)

# Using sympy.stats.GeneralizedMultivariateLogGamma() method
Gd = GeneralizedMultivariateLogGamma('G', d, v, l, mu)
gfg = density(Gd)(y[0], y[1], y[2])

pprint(gfg)
```

**输出:**

```
   oo                                                                        
______                                                                       
\     `                                                                      
 \                                                               5*y_2    y_3
  \                                                     2*y_1   e        e   
   \                   (n + 1)*(2*y_1 + 5*y_2 + y_3) - e      - ------ - ----
    \       n  -n - 1                                             2       3  
    /   10*0 *6      *e                                                      
   /    ---------------------------------------------------------------------
  /                                      3                                   
 /                                  Gamma (n + 1)                            
/_____,                                                                      
 n = 0                                        

```