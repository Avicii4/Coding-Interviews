# 正则表达式匹配

**题目描述：**

请实现一个函数用来匹配包括 '.' 和 '\*' 的正则表达式。模式中的字符 '.' 表示任意一个字符，而 '\*' 表示它前面的字符可以出现任意次（包含0次）。在本题中，匹配是指字符串的所有字符匹配整个模式。例如，字符串 "aaa" 与模式 "a.a" 和 "ab\*ac\*a" 匹配，但是与 "aa.a" 和 "ab\*a" 均不匹配。

**分析：**

1 当模式中第二个字符不是 \* 时，

1.1 若字符串和模式的第一个字符相同时，字符串和模式都后移一位再匹配。

1.2 若不同，直接返回 false。

2 当模式中第二个字符是 \* 时，

2.1 若字符串和模式的第一个字符相同时，

2.1.1 模式后移两位，继续匹配，表明直接忽略这两位。

2.1.2 字符串后移一位，继续匹配，因为 \* 可匹配多个字符。

2.2  若字符串和模式的第一个字符不同时，模式直接后移两位再匹配。

