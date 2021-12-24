# 从熊猫的约会中获得一天

> 原文:[https://www . geeksforgeeks . org/get-day-from-a-date-in-pandas/](https://www.geeksforgeeks.org/get-the-day-from-a-date-in-pandas/)

给定一个特定的日期，有可能获得该日期所在的星期几。这是在熊猫库和熊猫中的 to_datetime()方法的帮助下实现的。
在大多数数据集中， **Date** 列似乎是数据类型 **String** ，用该列执行任何计算肯定都不舒服，例如两个日期之间的月差、时间差或找到星期几。因此，Pandas 提供了一个名为 to_datetime()的方法来将字符串转换为 Timestamp 对象。
**例:**

```py
We'll use the date format 'dd/mm/yyyy'

Input :  '24/07/2020' 
Output : 'Friday' 

Input : '01/01/2001'
Output : 'Monday' 
```

一旦我们将字符串格式的日期转换为日期时间对象，就很容易在创建的时间戳对象上使用 day_name()方法获取一周中的某一天。
**示例 1 :** 在本例中，我们将一个类型为“str”且格式为“dd/mm/yyyy”的随机日期传递给 to_datetime()方法。结果我们得到一个**时间戳**熊猫对象。然后，我们通过 Timestamp 类的 day_name()方法检索一周中的某一天。

## 蟒蛇 3

```py
# importing the module
import pandas as pd

# the date in "dd/mm/yyyy" format
date = "19/02/2022"
print("Initially the type is : ", type(date))

# converting string to DateTime
date = pd.to_datetime(date, format = "%d/%m/%Y")
print("After conversion, the type is : ", type(date))

# fetching the day
print("The day is : " + date.day_name())
```