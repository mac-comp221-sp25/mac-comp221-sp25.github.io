---
layout: post
title: "Activity 12: More Divide & Conquer Design"
categories: Activity DivideAndConquer Design
---

## Learning Goals

You will work towards being able to...

1. Use divide and conquer design principles to write algorithms to solve problems

## Instructions
Work with your groups on the following problems:

1. (LeetCode 198) Suppose you plan to rob houses along a street. [^1]  However, for safety, you cannot rob adjacent houses, since a strange alarm system will immediately alert the authorities if such an event occurs. You have, however, cased the street well, and have an array $A$ that contains $N$ integers, where $A[i]$ represents the expected illicit earnings from robbing the $i$th house on the street. Write a Divide & Conquer algorithm to determine the maximum profits you can earn without tripping the alarm.

    > ###### Hint
    > Consider whether or not you rob from house $i$. How does this affect the other houses one can take from? Once that decision is made, do you see subproblems that can help you solve the whole thing?
    {: .block-tip}

2. (Skiena 5-5) Suppose you have a sorted array of *distinct integers* $A$. Find a $O(\log n)$ algorithm find whether there exists some index $i$ such that $A[i] = i$. 

    > ###### Hint 
    > Remember that the array is sorted and contains *integers*. This means that $A[i+1] \geq 1 + A[i]$ for any index $1 \leq i < N$!
    {: .block-tip}

#### Submission
Submit an artifact of your work for problem 1 or 2.

---
[^1]: For the record, COMP221 does not officially endorse any crimes.
