# 把数组排成最小的数

**题目描述：**

输入一个正整数数组，把数组里所有数字拼接起来排成一个数，打印能拼接出的所有数字中最小的一个。例如输入数组{3，32，321}，则打印出这三个数字能排成的最小数字为321323。

**分析：**

贪心策略。根据函数的返回值，应首先把所有数字转成字符串。若 `o1+o2>o2+o1` ，则 o2 应在序列中排在 o1 之前；反之若 `o1+o2<o2+o1` o1 应在序列中排在 o2 之前。代码中使用了 lambda 表达式。