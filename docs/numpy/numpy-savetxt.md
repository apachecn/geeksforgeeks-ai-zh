# num py . save txt()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-save txt/

**`numpy.savetxt(fname, X, fmt='%.18e', delimiter=' ', newline='\n', header='', footer='', comments='# ', encoding=None)`** :这个方法是把数组保存到一个文本文件中。

> ***参数:**
> **fname :** 如果文件名以`.gz`结尾，文件会自动以压缩 gzip 格式保存。loadtxt 透明地理解 gzipped 文件。
> **X**:【1D 或 2D 数组 _like】要保存到文本文件的数据。
> **fmt** :单一格式(%10.5f)、格式序列或多格式字符串，例如“迭代% d –% 10.5 f”，在这种情况下分隔符被忽略。
> **分隔符**:分隔列的字符串或字符。
> **换行符**:分隔行的字符串或字符。
> **头文件**:将写在文件开头的字符串。
> **页脚**:将写在文件末尾的字符串。
> **注释**:将被添加到页眉和页脚字符串前的字符串，以将其标记为注释。默认值:' # '，如 numpy.loadtxt.
> **编码**所预期的:用于编码输出文件的编码。不适用于输出流。如果编码不是“字节”或“拉丁 1”，您将无法在 NumPy 版本< 1.14 中加载文件。默认值为“latin1”。*

**代码#1:**

```
# Python program explaining  
# savetxt() function
import numpy as geek

x = geek.arange(0, 10, 1)
print("x is:")
print(x)

# X is an array
c = geek.savetxt('geekfile.txt', x, delimiter =', ')   
a = open("geekfile.txt", 'r')# open file in read mode

print("the file contains:")
print(a.read())
```

**输出:**

```
x is:
[0 1 2 3 4 5 6 7 8 9]
the file contains:
0.000000000000000000e+00
1.000000000000000000e+00
2.000000000000000000e+00
3.000000000000000000e+00
4.000000000000000000e+00
5.000000000000000000e+00
6.000000000000000000e+00
7.000000000000000000e+00
8.000000000000000000e+00
9.000000000000000000e+00

```

**代码#2:**

```
# Python program explaining  
# savetxt() function

import numpy as geek

x = geek.arange(0, 10, 1)
y = geek.arange(10, 20, 1)
z = geek.arange(20, 30, 1)
print("x is:")
print(x)

print("y is:")
print(y)

print("z is:")
print(z)

# x, y, z are 3 numpy arrays with same dimension 
c = geek.savetxt('geekfile.txt', (x, y, z)) 
a = open("geekfile.txt", 'r')# open file in read mode

print("the file contains:")
print(a.read())
```

**输出:**

> x 为:
> 【0 1 2 3 4 5 6 7 8 9】
> y 为:
> 【10 11 12 13 14 15 16 17 18 19】
> z 为:
> 【20 21 22 23 24 25 26 27 28 29】
> 
> 该文件包含:
> 0.00000000000000000 e+00 1.0000000000000000 e+00 2.00000000000000000000003.000000000000000000000000004.0000000000000000000000000000000000000000000000000000000000000005

**代码#3:** 类型错误

```
# Python program explaining  
# savetxt() function

import numpy as geek

x = geek.arange(0, 10, 1)
y = geek.arange(0, 20, 1)
z = geek.arange(0, 30, 1)
print("x is:")
print(x)

print("y is:")
print(y)

print("z is:")
print(z)

# x, y, z are 3 numpy arrays without having same dimension 
c = geek.savetxt('geekfile.txt', (x, y, z)) 
```

**输出:**

> FH . write(as bytes(format % tuple(row)+newline))
> type error:只有 length-1 数组可以转换为 Python 标量
> 
> 在处理上述异常的过程中，发生了另一个异常:
> 
> %(字符串(X.dtype)，格式))
> 类型错误:数组 dtype ('object ')和格式说明符(' %.18e ')不匹配

请注意，如果 numpy 数组的维数不等，则会出现错误。