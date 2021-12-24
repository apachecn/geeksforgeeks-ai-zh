# python | numpy num py . ndaarray . _ _ _ isb _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-ndaarray-_ _ _ _ _ _/t1]

借助`**numpy.ndarray.__isub__()**`方法，我们可以减去在`ndarray.__isub__()`方法中作为参数提供的特定值。数值将从 numpy 数组的每个元素中减去**。**

> ****语法:**n 数组。__isub__($self，value，/)**
> 
> ****返回:**自=值**

****示例#1 :**
在这个示例中，我们可以看到数组中的每个元素都被**减去**，该值在方法`ndarray.__isub__()`中作为参数给出。请记住，此方法适用于所有类型的数值。**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1.2, 2.6, 3, 4.5, 5])

# applying ndarray.__isub__() method
print(gfg.__isub__(5))
```

****Output:**

```py
[-3.8 -2.4 -2\.  -0.5  0\. ]

```** 

****例 2 :****

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2.2, 3, 4, 5.01],
                [6.1, 5, 4.8, 3, 2]])

# applying ndarray.__isub__() method
print(gfg.__isub__(3))
```

****Output:**

```py
[[-2\.   -0.8   0\.    1\.    2.01]
 [ 3.1   2\.    1.8   0\.   -1\.  ]]

```**