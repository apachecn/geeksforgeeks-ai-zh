# 使用 NumPy 数组

将摄氏度值列表转换为华氏度

> 原文:[https://www . geeksforgeeks . org/convert-list-of-Celtics-values-to-华氏-using-numpy-array/](https://www.geeksforgeeks.org/convert-list-of-celsius-values-into-fahrenheit-using-numpy-array/)

让我们看看如何通过将摄氏温度列表转换成华氏温度来将其转换成 NumPy 数组。
将 Celcius 转换为 Farenhiet 的公式为:

```
feh = (9 * cel / 5 + 32)

```

**方法 1 :** 使用`**numpy.array()**`方法。

```
# importing the module
import numpy as np

# taking the celsius  input
inp = [0, 12, 45.21, 34, 99.91]

# storing the input
# in numpy array
cel = np.array(inp)

print(f"Celsius {cel}")

# using formulae
feh = (9 * cel / 5 + 32)

# printing results
print(f"Fahrenheit {feh}")
```

**输出:**

```
Celsius [ 0\.   12\.   45.21 34\.   99.91]
Fahrenheit [ 32\.     53.6   113.378  93.2   211.838]

```

**方法 2 :** 使用`**numpy.asarray()**`方法。

```
# importing the module
import numpy as np

# taking the celsius  input
inp = [0, 12, 45.21, 34, 99.91]

# storing the input
# in numpy array
cel = np.asarray(inp)

print(f"Celsius {cel}")

# using formulae
feh = (9 * cel / 5 + 32)

# printing results
print(f"Fahrenheit {feh}")
```

**输出:**

```
Celsius [ 0\.   12\.   45.21 34\.   99.91]
Fahrenheit [ 32\.     53.6   113.378  93.2   211.838]

```

**方法三:**使用`**numpy.arange()**`。

```
# importing the module
import numpy as np

# taking thecelsius  input
inp = [0, 12, 45.21, 34, 99.91]

# arange will not directly
# convert into numpy array
cel = np.arange(5)

# the above code
# will give o/p as
# cel = [0, 1, 2, 3, 4]
cel = [i for i in inp]
# thus the input(inp)
# is stored in cel
# using list comprehension

print(f"Celsius {cel}")

# applying formulae
# using list comprehension
feh = [(9 * i / 5 + 32) for i in cel]

# printing results
print(f"Fahrenheit {feh}")
```

**输出:**

```
Celsius [ 0\.   12\.   45.21 34\.   99.91]
Fahrenheit [ 32\.     53.6   113.378  93.2   211.838]

```