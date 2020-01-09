## 题目链接
https://leetcode.com/problems/add-two-numbers/

## Description:
```
You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order and each of their nodes contain a single digit. Add the two numbers and return it as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

Example:

Input: (2 -> 4 -> 3) + (5 -> 6 -> 4)
Output: 7 -> 0 -> 8
Explanation: 342 + 465 = 807.

```
## 方法
设立一个表示进位的变量carried，建立一个新链表，
把输入的两个链表从头往后同时处理，每两个相加，将结果加上carried后的值作为一个新节点到新链表后面。

![2.addTwoNumbers](https://camo.githubusercontent.com/6bc31a7535730021d9ced7499adaa9d36312cad3/68747470733a2f2f626c6f672d313235373132363534392e636f732e61702d6775616e677a686f752e6d7971636c6f75642e636f6d2f626c6f672f667a3933332e676966)

(图片来自： https://github.com/MisterBooo/LeetCodeAnimation)


## Code

#! python3

# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def addTwoNumbers(self, l1: ListNode, l2: ListNode) -> ListNode:
        
