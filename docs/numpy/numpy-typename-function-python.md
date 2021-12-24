# numpy.typename()函数–python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-typename-function-python/

**`numpy.typename()`** 函数返回给定数据类型代码的描述。

> **语法:** numpy.typename(char)
> 
> **参数:**
> **字符:**【str】数据类型代码。
> **返回:**【str】输入数据类型代码的描述。

**代码#1 :**

```
# Python program explaining
# numpy.typename() function

# importing numpy as geek 
import numpy as geek 

typechars = ['?', 'O', 'b', 'd', 'g', 'f', 'i', 'h', 'l', 'q'] 

for typechar in typechars:
    print(typechar, ' : ', geek.typename(typechar))
```

**输出:**

```
?  :  bool
O  :  object
b  :  signed char
d  :  double precision
g  :  long precision
f  :  single precision
i  :  integer
h  :  short
l  :  long integer
q  :  long long integer

```

**代码#2 :**

```
# Python program explaining
# numpy.typename() function

# importing numpy as geek 
import numpy as geek 

typechars = ['S1', 'B', 'D', 'G', 'F', 'I', 'H', 'L', 'Q', 'S', 'U', 'V'] 

for typechar in typechars:
    print(typechar, ' : ', geek.typename(typechar))
```

**输出:**

```
S1  :  character
B  :  unsigned char
D  :  complex double precision
G  :  complex long double precision
F  :  complex single precision
I  :  unsigned integer
H  :  unsigned short
L  :  unsigned long integer
Q  :  unsigned long long integer
S  :  string
U  :  unicode
V  :  void

```