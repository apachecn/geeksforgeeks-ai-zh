# Python–tensorflow . executing _ 翘首以盼()

> 原文:[https://www . geesforgeks . org/python-tensorflow-executing _ 翘首以盼/](https://www.geeksforgeeks.org/python-tensorflow-executing_eagerly/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**executing _ early()**用于检查当前线程中是否启用或禁用了紧急执行。默认情况下，启用了紧急执行，因此在大多数情况下，它将返回 true。在以下情况下，这将返回 false:

*   如果是在**tensorflow . function*****TF . init _ scope**或**TF . config . experial _ run _ functions _ 翘首(True)** 之前没有调用。*
*   *在 tensorflow.dataset 的转换函数中执行。*
*   *调用 tensorflow . compat . v1 . disable _ eage _ execution()。*

> ***语法:**tensorflow . executing _ 翘首以盼()*
> 
>  ***参数:**这个不接受任何参数。
> 
> **返回:**如果启用了紧急执行，则返回真，否则返回假。*

***例 1:***

## *蟒蛇 3*

```py
*# Importing the library
import tensorflow as tf

# Checking eager execution
res = tf.executing_eagerly()

# Printing the result
print('res: ', res)*
```

***输出:***

```py
*res:  True* 
```

***示例 2:** 本示例检查有和没有 init_scope 的 tensorflow.function 的紧急执行。*

## *蟒蛇 3*

```py
*# Importing the library
import tensorflow as tf

@tf.function
def gfg():
  with tf.init_scope():
    # Checking eager execution inside init_scope
    res = tf.executing_eagerly()
    print("res 1:", res)

  # Checking eager execution outside init_scope
  res = tf.executing_eagerly()
  print("res 2:", res)
gfg()*
```

***输出:***

```py
*res 1: True
res 2: False* 
```