# 跳台阶

**题目描述：**

一只青蛙一次可以跳上1级台阶，也可以跳上2级。求该青蛙跳上一个n级的台阶总共有多少种跳法（先后次序不同算不同的结果）。

**分析：**

跳上第 *n* 级之前，可以是从第 *n-1* 级跳一级上来的，也可以是从第 *n-2* 跳两级上来的，所以 *f(n)=f(n-1)+f(n-2)* ，所以就是在求斐波那契数列。

