# numpy.defchararray.decode()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-defchararray-decode-in-python/

**`numpy.core.defchararray.decode(arr, encoding)` :** 这个 numpy 函数根据指定的编解码器解码字符串(对象)。

> **参数:**
> **arr :** 阵状或弦状。
> **编码:**【str】正在遵循的编解码器名称。
> **错误:**指定如何处理错误。
> 
> **返回:**解码字符串

**代码:**

```
# Python Program illustrating 
# numpy.char.decode() method 
import numpy as np 

arr1 = ['eAAAa', 'ttttds', 'AAtAAt']
arr2 = ['11sf', 'sdsf2', '1111f2']

print ("\narr1 : ", arr1)
print ("\narr2 : ", arr2)

# Using np.char.encode()
encode_arr1 = np.char.encode(arr1, encoding ='cp037')
print ("\nEncoded arr1 : \n", encode_arr1)

encode_arr2 = np.char.encode(arr2, encoding ='utf8')
print ("\nEncoded arr2 : \n", encode_arr2)

# Using np.char.decode()
decode_arr1 = np.char.decode(encode_arr1, encoding ='cp037')
print ("\nDecoded arr1 : \n", decode_arr1)

decode_arr2 = np.char.decode(encode_arr2, encoding ='cp037')
print ("\nDecoded arr1 : \n", decode_arr2)

decode_arr2 = np.char.decode(encode_arr2, encoding ='utf8')
print ("\nDecoded arr1 : \n", decode_arr2)
```

**输出:**

```
arr1 :  ['eAAAa', 'ttttds', 'AAtAAt']
arr2 :  ['11sf', 'sdsf2', '1111f2']

Encoded arr1 : 
 [b'\x85\xc1\xc1\xc1\x81' b'\xa3\xa3\xa3\xa3\x84\xa2'
 b'\xc1\xc1\xa3\xc1\xc1\xa3']

Encoded arr2 : 
 [b'11sf' b'sdsf2' b'1111f2']

Decoded arr1 : 
 ['eAAAa' 'ttttds' 'AAtAAt']

Decoded arr2 : 
 ['\x91\x91ËÃ' 'ËÀËÃ\x16' '\x91\x91\x91\x91Ã\x16']

Decoded arr2 : 
 ['11sf' 'sdsf2' '1111f2']

```