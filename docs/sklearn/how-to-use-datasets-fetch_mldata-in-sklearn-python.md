# 如何在 sklearn–Python 中使用 datasets.fetch_mldata()？

> 原文:[https://www . geeksforgeeks . org/如何使用-数据集-fetch _ mldata-in-sklearn-python/](https://www.geeksforgeeks.org/how-to-use-datasets-fetch_mldata-in-sklearn-python/)

**mldata.org 没有强制的惯例来存储数据或命名数据集中的列。该函数的默认行为适用于下面提到的大多数常见情况:**

***   The data value stored in the column is Data, and the target value stored in the column is Label.*   The first list stores targets and the second column stores data.*   The array data is stored as features and samples, which need to be transposed to match the *sklearn standard.***

**获取一个机器学习数据集，如果文件不存在，它会自动从 mldata.org 下载。**

**sklearn.datasets 包使用函数直接加载数据集:***sklearn . datasets . fetch _ mldata(**)***

> ****语法:**sklearn . datasets . fetch _ mldata(dataname，target_name='label '，data_name='data '，transpose_data=True，data_home=None)**
> 
> ****参数:****
> 
> *   ****日期名称:****(<***【str】>**)**是阿云*mld data . org****-什么，云娥***:【iris】【mnist】"绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿绿“”-什么。***
> *   ****target _ name: (** *optional, default: [label]* **)** accept the name or index of the column containing the target value, and need to pass the default value of the label.**
> *   ****data _ name:** **(** *optional, default: [data]* **)** Accept the name or index of the column containing data, and need to pass the default value of data.**
> ***   **Transfer _ data:** **(** *optional, default value: True* **)** The transferred default value is *true* . If it is true, the loaded data will be transferred.*   **data _ home:** **(** *optional, default: none* **)** Load the cache folder for the data set. By default, all sklearn data is stored in the subfolder " *~/scikit _ learn _ data* ".T61】**
> 
> ****返回:**数据、 **(** *Bunch* **)** 有趣的属性有:【数据】、要学习的数据、【目标】、分类标签、【DESCR】、数据集描述、数据集列的原始名称“COL_NAMES”。**

**让我们看看例子:**

****示例 1:** 从 mldata 中加载需要转置的‘虹膜’数据集。**

 **## 蟒 3

```
# import fetch_mldata function
from sklearn.datasets.mldata import fetch_mldata

# load data and transpose data
iris = fetch_mldata('iris',
                    transpose_data = False)

# iris data is very large
# so print the dataset shape
# print(iris)
print(iris.data.shape)
```** 

****输出:****

```
(4,150)
```

****示例 2:** 从 mldata 加载 MNIST 数字识别数据集。**

 **## 蟒 3

```
# import fetch_mldata function
from sklearn.datasets.mldata import fetch_mldata

# load data 
mnist = fetch_mldata('MNIST original')

# mnist data is very large
# so  print the shape of data
print(mnist.data.shape)
```** 

****输出:****

```
 (70000, 784)
```

****注:**此帖根据 Scikit-learn(0.19 版)发布。**