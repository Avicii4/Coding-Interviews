# 链表中环的入口结点

**题目描述：**

给一个链表，若其中包含环，请找出该链表的环的入口结点，否则，输出null。

**分析：**

首先用快慢指针测出链表是否有环。若有环，快指针回到链表头部，然后快慢指针一起，每次只走一步，两指针相遇之处就是链表环的入口结点。数学证明请看我的文章：https://avicii4.github.io/2019/05/04/crossed-linkedlist/#more 。

