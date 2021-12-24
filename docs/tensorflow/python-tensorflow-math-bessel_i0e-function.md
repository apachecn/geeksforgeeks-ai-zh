# Python–tensorflow . math . Bessel _ i0e()函数

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-Bessel _ i0e-function/](https://www.geeksforgeeks.org/python-tensorflow-math-bessel_i0e-function/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。**贝塞尔 _i0e()** 是张量流数学模块中存在的函数。该函数用于寻找元素态指数标度的修正 0 阶贝塞尔函数。

```
bessel_i0e(x) = exp(-abs(x)) bessel_i0(x)

bessel_i0e(x) is faster and numerically stabler than bessel_i0(x).

```

> **语法:**tensorflow . math . Bessel _ i0e(x，name)
> 
> **参数:**
> 
> *   **x:** 它是一个张量，这个张量允许的数据类型是 bfloat16，half，float32，float64。
> *   **名称:**是一个可选参数，用于给出操作名称。
>     
> 
> **返回:**它返回一个张量或稀疏张量，取决于与 x 相同数据类型的 x。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([1,2,3,4,5], dtype = tf.float64)

# printing the input 
print('a: ',a)

# evaluating the result
r = tf.math.bessel_i0e(a)

# printing the result
print("Result: ",r)
```

**输出:**

```
a:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5,), dtype=float64)
Result:  tf.Tensor([0.46575961 0.30850832 0.24300035 0.20700192 0.18354081], shape=(5,), dtype=float64)

```

**示例 2:** 可视化

## 蟒蛇 3

```
# importing the library
import tensorflow as tf
import matplotlib.pyplot as plt 

# initializing the input
a = tf.constant([1,2,3,4,5], dtype = tf.float64)

# evaluating the result
r = tf.math.bessel_i0e(a)

#plotting the graph
plt.plot(a, r, color = 'green', marker = "o")  
plt.title("tensorflow.math.bessel_i0e")  
plt.xlabel("Input")  
plt.ylabel("Result")  
plt.show() 
```

**输出:**

![](img/b2ec043fa50f7a59fecf173b176493e3.png)