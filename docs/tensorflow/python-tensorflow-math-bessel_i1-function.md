# Python–tensorflow . math . Bessel _ i1()函数

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-Bessel _ i1-function/](https://www.geeksforgeeks.org/python-tensorflow-math-bessel_i1-function/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。**贝塞尔 _i1()** 是张量流数学模块中存在的函数。该函数用于求单元式一阶修正贝塞尔函数。

> **语法:** tensorflow.math.bessel_i1( x，name)
> 
> **参数:**
> 
> *   **x:** 它是一个张量，这个张量允许的数据类型是 bfloat16，half，float32，float64。
> *   **名称:**是一个可选参数，用于给出操作名称。
> 
> **返回:**它返回一个张量或稀疏张量，取决于与 x 相同数据类型的 x。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([1,2,3,4,5], dtype = tf.float64)

# printing the input 
print('a: ',a)

# evaluating the result
r = tf.math.bessel_i1(a)

# printing the result
print("Result: ",r)
```

**输出:**

```py
a:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5,), dtype=float64)
Result:  tf.Tensor([ 0.5651591   1.59063685  3.95337022  9.75946515 24.33564214], shape=(5,), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt 

# initializing the input
a = tf.constant([1,2,3,4,5], dtype = tf.float64)

# evaluating the result
r = tf.math.bessel_i1(a)

#plotting the graph
plt.plot(a, r, color = 'green', marker = "o")  
plt.title("tensorflow.math.bessel_i1")  
plt.xlabel("Input")  
plt.ylabel("Result")  
plt.show() 
```

**输出:**

![](img/fabcf667f8d7086adf4c6970e264122f.png)