# 使用 python 中的 NLTK 标记文本

> 原文:[https://www . geesforgeks . org/token ize-text-using-nltk-python/](https://www.geeksforgeeks.org/tokenize-text-using-nltk-python/)

要运行下面的 python 程序，必须在您的系统中安装(NLTK)自然语言工具包。
NLTK 模块是一个庞大的工具包，旨在帮助您掌握整个自然语言处理(NLP)方法。
要安装 NLTK，请在您的终端中运行以下命令。

*   sudo pip 安装 nltk
*   然后，只需在终端中输入 **python** 即可进入 python shell
*   键入**导入 nltk**
*   **nltk.download('all')**

由于需要下载大量的标记器、分块器、其他算法和所有的语料库，上述安装将花费相当长的时间。

*   **语料库**–正文，单数。语料库是这个的复数。*   **词汇**–单词及其含义。*   **Token** – Each “entity” that is a part of whatever was split up based on rules. For examples, each word is a token when a sentence is “tokenized” into words. Each sentence can also be a token, if you tokenized the sentences out of a paragraph.

    **所以基本上标记化包括从正文中拆分句子和单词。**

    ```
    # import the existing word and sentence tokenizing 
    # libraries
    from nltk.tokenize import sent_tokenize, word_tokenize

    text = "Natural language processing (NLP) is a field " + \
           "of computer science, artificial intelligence " + \
           "and computational linguistics concerned with " + \
           "the interactions between computers and human " + \
           "(natural) languages, and, in particular, " + \
           "concerned with programming computers to " + \
           "fruitfully process large natural language " + \
           "corpora. Challenges in natural language " + \
           "processing frequently involve natural " + \
           "language understanding, natural language" + \
           "generation frequently from formal, machine" + \
           "-readable logical forms), connecting language " + \
           "and machine perception, managing human-" + \
           "computer dialog systems, or some combination " + \
           "thereof."

    print(sent_tokenize(text))
    print(word_tokenize(text))`
    ```

    **OUTPUT**
    *【‘自然语言处理(NLP)是计算机科学、人工智能和计算语言学的一个领域，关注计算机和人类(自然)语言之间的交互，特别是关注对计算机进行编程以有效处理大型自然语言语料库。’“‘自然语言处理中的挑战通常涉及自然语言理解、自然语言生成(通常来自正式的、机器可读的逻辑形式)、连接语言和机器感知、管理人机对话系统，或者它们的某种组合。”】
    【“自然的”、“语言的”、“处理的”、“(”、“‘NLP’、“)”、“是”、“一个”、“领域的”、“的”、“计算机的”、“科学的”、“的”、“人工的”、“智能的”、“和”、“计算的”、“语言学的”、“关注的”、“与”、“的”、“相互作用的”、“之间的”、“计算机的”、“与”、“人类的”、“人类的”、“(”、“‘自然的’、“)”、“‘语言的’、“”、“‘和’、“”、“‘特别是’、“”、“”、“‘关注的”、“与”、“编程的”、“计算机的”、“到”、“结果的”、“过程的”、“过程的”“，‘挑战’，‘在’，‘自然’，‘语言’，‘处理’，‘频繁地’，‘涉及’，‘自然’，‘理解’，‘语言’，‘生成’，“(”，‘频繁地’，‘从’，‘形式’，“，”，‘机器可读’，‘逻辑’，‘形式’，“)”，‘连接’，‘语言’，‘和’，‘机器’，‘感知’，‘管理’，‘人机’，‘对话’，‘系统’，’，‘或’，‘某些’，‘它们的组合’，”】*

    在那里，我们创建了标记，最初是句子，后来是单词。

    本文由 **Pratima Upadhyay** 供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

    如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。