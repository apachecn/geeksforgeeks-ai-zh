# 将嵌套 JSON 结构转换为熊猫数据帧

> 原文:[https://www . geesforgeks . org/converting-nested-JSON-structures-to-pandas-data frames/](https://www.geeksforgeeks.org/converting-nested-json-structures-to-pandas-dataframes/)

在本文中，我们将看到如何将嵌套的 JSON 结构转换成熊猫数据帧。

## **多级 JSON】**

在这种情况下，嵌套的 JSON 数据包含另一个 JSON 对象作为其某些属性的值。这使得数据是多层次的，我们需要根据项目要求将其展平，以获得更好的可读性，如下所述。

## 蟒 3

```py
# importing the libraries used
import pandas as pd

# initializing the data
data = {
    'company': 'XYZ pvt ltd',
    'location': 'London',
    'info': {
        'president': 'Rakesh Kapoor',
        'contacts': {
            'email': 'contact@xyz.com',
            'tel': '9876543210'
        }
    }
}
```