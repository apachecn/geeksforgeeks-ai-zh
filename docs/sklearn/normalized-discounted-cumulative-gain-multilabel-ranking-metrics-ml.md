# 标准化贴现累计收益–多标签排名指标| ML

> 原文:[https://www . geesforgeks . org/normalized-贴现-累积-增益-multi label-ranking-metrics-ml/](https://www.geeksforgeeks.org/normalized-discounted-cumulative-gain-multilabel-ranking-metrics-ml/)

**贴现累计收益**
贴现累计收益(DCG)是衡量排名质量的指标。它主要用于信息检索问题，例如通过根据搜索关键词的相关性对其显示的文章进行排名来衡量搜索引擎算法的有效性。

让我们考虑一个输出 5 个文档的搜索引擎，命名为( *D <sub>1</sub> 、D <sub>2</sub> 、D <sub>3</sub> 、D <sub>4</sub> 、D <sub>5</sub>* )按此顺序输出。我们需要定义相关性等级(0-3)，其中:

*   **0 :** 不相关
*   **1-2 :** 有点相关
*   **3 :** 完全相关

假设这些文档具有相关性分数:

*   D <sub>1</sub> : 3
*   D <sub>2</sub> : 2
*   D <sub>3</sub> : 0
*   D <sub>4</sub> : 0
*   D <sub>5</sub> : 1

***累计增益*** 是这些相关性得分的总和，可以计算为:
![CG = \sum_{i=1}^{5}(rel)_{i} = 3+2+0+0+1 =6   ](img/8c4165f9aacf8ad69d71d2c10859a735.png "Rendered by QuickLaTeX.com")

贴现后的累计收益可以通过公式计算:
![DCG = \sum_{i=1}^{5} \dfrac{rel_i}{\log_2 (i+1)}   ](img/00d100a8e835b956caa5593081fef687.png "Rendered by QuickLaTeX.com")

因此上述例子的贴现累计收益为:
![DCG_5 = \dfrac{3}{log_2 (2) } + \dfrac{2}{log_2 (3) }+ \dfrac{0}{log_2 (4) } +\dfrac{0}{log_2 (5) } + \dfrac{1}{log_2 (6) }\\ DCG_5 = \dfrac{3}{log_2 (2) } + \dfrac{2}{log_2 (3) }+ \dfrac{0}{log_2 (4) } +\dfrac{0}{log_2 (5) } + \dfrac{1}{log_2 (6) } \\ DCG_5 = 3 + \dfrac{2}{1.585} + 0 + 0 + \dfrac{1}{2.585}\\ DCG_5 = 3 + 1.26 + 0.3868 \\ DCG_5 \simeq 4.67   ](img/de460adc4b6b114661d48abe307c6223.png "Rendered by QuickLaTeX.com")

现在我们需要按排名降序排列这些文章，并计算 DCG，以获得理想折扣累积收益(IDCG)排名。
![IDCG_5 = \dfrac{3}{log_2 (2) } + \dfrac{2}{log_2 (3) }+ \dfrac{1}{log_2 (4) } +\dfrac{0}{log_2 (5) } + \dfrac{0}{log_2 (6) } \\ IDCG_5 = 3 + \dfrac{2}{1.585} + \dfrac{1}{2}+ 0 + 0 \\ IDCG_5 = 3 + 1.26 + 0.5\\ IDCG_5 = 4.76   ](img/b6a3dfec8b0974f6d2ed1c814935b68b.png "Rendered by QuickLaTeX.com")
现在，我们使用以下公式计算我们的**归一化 DCG**:
![nDCG = \dfrac{DCG_5}{IDCG_5} \\ nDCG = \dfrac{4.67}{4.76} \\ nDCG \simeq 0.98\\   ](img/3665827ae0e0ac426055ae7731348732.png "Rendered by QuickLaTeX.com")

**代码:Python 程序为** ***归一化贴现累计收益***

## 蟒蛇 3

```
# import required package
from sklearn.metrics import ndcg_score, dcg_score
import numpy as np

# Relevance scores in Ideal order
true_relevance = np.asarray([[3, 2, 1, 0, 0]])

# Relevance scores in output order
relevance_score = np.asarray([[3, 2, 0, 0, 1]])

# DCG score
dcg = dcg_score(true_relevance, relevance_score)
print("DCG score : ", dcg)

# IDCG score
idcg = dcg_score(true_relevance, true_relevance)
print("IDCG score : ", idcg)

# Normalized DCG score
ndcg = dcg / idcg
print("nDCG score : ", ndcg)

# or we can use the scikit-learn ndcg_score package
print("nDCG score (from function) : ", ndcg_score(
    true_relevance, relevance_score))
```

**输出:**

```
DCG score :  4.670624189796882
IDCG score :  4.761859507142915
nDCG score :  0.980840401274087
nDCG score (from function) :  0.980840401274087
```

**归一化贴现累计收益的限制(NDCG):**

*   NDCG 度量不会处罚不良文档输出。例如:*【3】**【3，0，0】*有同一个 NDCG，但倒数第二有两个不相关的文件。
*   因为没有为输出文档的数量定义具体的标准。DCG 似乎没有处理输出中缺少任何相关文档的问题。例如，相似输入的两个输出*【3，3，3】*和*【3，3，3，3】*被认为是同样好的。对于输出-1，计算 DCG <sub>3</sub> ，但是对于输出-2，计算 DCG <sub>4</sub> 。

**参考文献:**

*   [DCG 维基百科文章](https://en.wikipedia.org/wiki/Discounted_cumulative_gain)
*   j . j . & Kekalainen(2002 年)。基于累积增益的红外技术评估。美国计算机学会信息系统学报(TOIS)，20(4)，422-446。