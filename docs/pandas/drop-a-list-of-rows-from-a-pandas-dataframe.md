# 从熊猫数据框中删除行列表

> 原文:[https://www . geesforgeks . org/drop-a-list-from-a-pandas-data frame/](https://www.geeksforgeeks.org/drop-a-list-of-rows-from-a-pandas-dataframe/)

让我们看看如何删除熊猫数据框中的行列表。我们可以使用 **drop()** 功能来实现。我们还将传递 inplace = True，因为它确保我们在实例中所做的更改存储在该实例中，而无需执行任何赋值
下面是如何从表中删除行列表的代码实现:

**例 1 :**

## 蟒蛇 3

```py
# import the module
import pandas as pd

# creating a DataFrame
dictionary = {'Names':['Simon', 'Josh', 'Amen', 'Habby',
                       'Jonathan', 'Nick'],
              'Countries':['AUSTRIA', 'BELGIUM', 'BRAZIL',
                           'FRANCE', 'INDIA', 'GERMANY']}
table = pd.DataFrame(dictionary, columns = ['Names', 'Countries'],
                     index = ['a', 'b', 'c', 'd', 'e', 'f'])

display(table)

# gives the table with the dropped rows
display("Table with the dropped rows")
display(table.drop(['a', 'd']))

# gives the table with the dropped rows
# shows the reduced table for the given command only
display("Reduced table for the given command only")
display(table.drop(table.index[[1, 3]]))

# it gives none but it makes changes in the table
display(table.drop(['a', 'd'], inplace = True))

# final table
print("Final Table")
display(table)

# table after removing range of rows from 0 to 2(not included)
table.drop(table.index[:2], inplace = True)

display(table)
```