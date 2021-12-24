# python | num py ndaarray。_ _ _ _ _ _ _ _()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-ndaarray-_ _ _ _ _ _ _ ilshift _/

借助`**Numpy ndarray.__ilshift__()**`方法，我们可以得到左移了`numpy.ndarray.__ilshift__()`方法中作为参数提供的值的元素。

> **语法:**n 数组。__ilshift__($self，value，/)
> 
> **返回:**自我<<=值

**注意:**请安装 python 的 numpy 模块执行以下任务。连接到互联网时，在命令提示符下运行以下命令。

```py
pip install numpy
```

**示例#1 :**
在这个示例中，我们可以看到每个元素都向左移动了在`ndarray.__ilshift__()`方法中作为参数传递的值。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3, 4, 5])

# applying ndarray.__ilshift__() method
print(gfg.__ilshift__(2))
```

**Output:**

```py
[ 4  8 12 16 20]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3, 4, 5],
                [6, 5, 4, 3, 2]])

# applying ndarray.__ilshift__() method
print(gfg.__ilshift__(1))
```

**Output:**

```py
[[ 2  4  6  8 10]
 [12 10  8  6  4]]

```