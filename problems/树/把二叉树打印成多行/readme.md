# 把二叉树打印成多行

**题目描述：**

从上到下按层打印二叉树，同一层结点从左至右输出。每一层输出一行。

**分析：**

递归，使用先序遍历，根据层数创建 多个 ArrayList，遍历到某一层时再向对应的 ArrayList 中添加元素。

