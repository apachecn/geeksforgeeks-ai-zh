# 症状统计。python 中的 generated multi variatelogamomega()

> 原文:[https://www . geesforgeks . org/sympy-stats-generated multi variatelogamomega-in-python/](https://www.geeksforgeeks.org/sympy-stats-generalizedmultivariateloggammaomega-in-python/)

借助`**sympy.stats.GeneralizedMultivariateLogGammaOmega()**`方法，我们可以得到代表扩展的广义多元对数伽玛分布的连续联合随机变量。

> **语法:** `GeneralizedMultivariateLogGammaOmega(syms, omega, v, lamda, mu)`
> **参数:**
> 1)Syms–符号列表
> 2)Omega–正方形矩阵
> 3)V–正实数
> 4)Lambda–正实数列表
> 5)mu–正实数列表。
> **返回:**返回连续关节随机变量。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.stats.GeneralizedMultivariateLogGammaOmega()`方法，我们能够使用该方法获得表示扩展的广义多元对数伽马分布的连续联合随机变量。

```
# Import sympy and GeneralizedMultivariateLogGammaOmega
from sympy.stats import density
from sympy.stats.joint_rv_types import GeneralizedMultivariateLogGammaOmega
from sympy.stats.joint_rv import marginal_distribution
from sympy import symbols, S, Matrix

v = 1
l, mu = [1, 1, 1], [1, 1, 1]
d = S.One
y = symbols('y_1:4', positive = True)
omega = Matrix([[1, S.Half, S.Half], [S.Half, 1, S.Half], [S.Half, S.Half, 1]])

# Using sympy.stats.GeneralizedMultivariateLogGammaOmega() method
Gd = GeneralizedMultivariateLogGammaOmega('G', omega, v, l, mu)
gfg = density(Gd)(y[0], y[1], y[2])

pprint(gfg)
```

**输出:**

```
         oo                                                               
      ______                                                              
      \     `                                                             
       \                 n                                                
        \     /      ___\                                y_1    y_2    y_3
         \    |    \/ 2 |   (n + 1)*(y_1 + y_2 + y_3) - e    - e    - e   
  ___     \   |1 - -----| *e                                              
\/ 2 *    /   \      2  /                                                 
         /    ------------------------------------------------------------
        /                                 3                               
       /                             Gamma (n + 1)                        
      /_____,                                                             
       n = 0                                                              
--------------------------------------------------------------------------
                                    2                                     

```

**例 2 :**

```
# Import sympy and GeneralizedMultivariateLogGammaOmega
from sympy.stats import density
from sympy.stats.joint_rv_types import GeneralizedMultivariateLogGammaOmega
from sympy.stats.joint_rv import marginal_distribution
from sympy import symbols, S, Matrix

v = 1
l, mu = [1, 2], [2, 1]
d = S.One
y = symbols('y_1:3', positive = True)
omega = Matrix([[1, S.Half], [S.Half, 1]])

# Using sympy.stats.GeneralizedMultivariateLogGammaOmega() method
Gd = GeneralizedMultivariateLogGammaOmega('G', omega, v, l, mu)
gfg = density(Gd)(y[0], y[1])

pprint(gfg)
```

**输出:**

```
     oo                                                       
  ______                                                      
  \     `                                                     
   \                                                       y_2
    \                                             2*y_1   e   
     \                   (n + 1)*(2*y_1 + y_2) - e      - ----
      \      -n - 1  -n                                    2  
3*    /   2*2      *4  *e                                     
     /    ----------------------------------------------------
    /                             2                           
   /                         Gamma (n + 1)                    
  /_____,                                                     
   n = 0                                                      
--------------------------------------------------------------
                              4                               

```