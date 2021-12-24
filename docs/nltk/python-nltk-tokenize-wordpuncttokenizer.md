# Python NLTK | tokenize。wordpunctadizer()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-nltk-token ize-wordpuncttkenizer/

借助`**nltk.tokenize.WordPunctTokenizer()()**`方法，我们能够使用`tokenize.WordPunctTokenizer()()`方法从一串单词或句子中提取出**字母**和**非字母**字符形式的标记。

> **语法:** `tokenize.WordPunctTokenizer()()`
> **返回:** **从一串字母或非字母字符中返回标记。**

**示例#1 :**
在这个示例中，我们可以看到，通过使用`tokenize.WordPunctTokenizer()()`方法，我们能够从字母或非字母字符流中提取标记。

```py
# import WordPunctTokenizer() method from nltk
from nltk.tokenize import WordPunctTokenizer

# Create a reference variable for Class WordPunctTokenizer
tk = WordPunctTokenizer()

# Create a string input
gfg = "GeeksforGeeks...$&* \nis\t for geeks"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['GeeksforGeeks '，'…$&*，' is '，' for '，' geeks']

**例 2 :**

```py
# import WordPunctTokenizer() method from nltk
from nltk.tokenize import WordPunctTokenizer

# Create a reference variable for Class WordPunctTokenizer
tk = WordPunctTokenizer()

# Create a string input
gfg = "The price\t of burger \nin BurgerKing is Rs.36.\n"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['The '，' price '，' of '，' burger '，' in '，' BurgerKing '，' is '，' Rs '，', '36', '.']