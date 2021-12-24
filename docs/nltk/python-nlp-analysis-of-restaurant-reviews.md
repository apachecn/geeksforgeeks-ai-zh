# Python | NLP 分析餐厅点评

> 原文:[https://www . geesforgeks . org/python-NLP-分析-餐厅-评论/](https://www.geeksforgeeks.org/python-nlp-analysis-of-restaurant-reviews/)

**自然语言处理(NLP)** 是计算机科学和人工智能的一个领域，关注计算机和人类(自然)语言之间的交互，特别是如何对计算机进行编程以处理和分析大量自然语言数据。它是机器学习的一个分支，是关于分析任何文本和处理预测分析。
[**Scikit-learn**](https://www.geeksforgeeks.org/learning-model-building-scikit-learn-python-machine-learning-library/) 是一个针对 Python 编程语言的免费软件机器学习库。Scikit-learn 大部分是用 Python 编写的，一些核心算法是用 Cython 编写的，以实现性能。Cython 是 Python 编程语言的超集，旨在用主要用 Python 编写的代码提供类似 C 的性能。
我们来了解一下文本处理涉及的各个步骤以及 NLP 的流程。
这种算法可以很容易地应用到任何其他类型的文本中，比如将一本书分为《浪漫》、《摩擦》，但现在，让我们使用一个[餐厅评论](https://media.geeksforgeeks.org/wp-content/uploads/Restaurant_Reviews.tsv)数据集来评论负面或正面反馈。

#### 涉及的步骤:

**第 1 步:**导入数据集，设置分隔符为' \t '，因为列之间用制表符分隔。评论和它们的类别(0 或 1)没有被任何其他符号分开，但是有标签空间，因为大多数其他符号是评论(像$的价格，…！，等等)，算法可能会将它们用作分隔符，这将导致输出中出现奇怪的行为(如错误、怪异的输出)。

## 蟒蛇 3

```py
# Importing Libraries
import numpy as np 
import pandas as pd

# Import dataset
dataset = pd.read_csv('Restaurant_Reviews.tsv', delimiter = '\t')
```