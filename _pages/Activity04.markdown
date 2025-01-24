---
layout: post
title:  "Activity 04: Linear Data Structures Review"
categories: Activity Sorting
---

## Learning Goals

You will work towards being able to...

1. Understand the time and space complexity properties of Arrays, Stacks, Queues, and Lists

## Instructions

1. The textbook does a good job reviewing high-level aspects of the linear data structures we'll be using, but it misses out on some salient details: Namely, the time complexities of basic operations using these data structures. Construct a table that lists the worst-case time complexity of each operation available from a generic Array, Stack, Queue, and List (i.e., consider insert, remove, or look up an element in these collections). Do this using big-$\Theta$s. You don't have to provide a proof for each (but if you worry you couldn't construct one, it might be worth attempting!). 

2. Now let's practice reasoning about algorithms that use these data structures. Consider the following pseudocode

```plaintext
    StackFunction(String s):
        Let st be a stack
        For i <- 1 to length(s):
            st.push(s[i])
        For i <- 1 to length(s):
            If s[i] != st.pop():
                return false
        return true
```
(one day I'll figure out a nicer way to format pseudocode here)

What does it do?

3. What is this algorithm's big-$\Theta$ time complexity? Can you prove it? You don't know the *exact* growth functions for the time complexity of the calls to push and pop, but does knowing their big-$\Theta$ let you reason about StackFunction's big-$Theta$?

4. **For credit**: Submit your table from part 1 and your reasoning for part 3.
