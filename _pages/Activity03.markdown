---
layout: post
title:  "Activity 03: Sorting 3"
categories: Activity Sorting
---

## Learning Goals

You will work towards being able to...

1. Formalize algorithmic ideas into pseudocode
2. Prove the correctness of algorithms through induction.
3. Know common algorithms to solve cannonical problems (sorting)

## Instructions

1. Consider the following sorting algorithm, called Bubblesort!

```plaintext
function BubbleSort(Array A):
    For i <- 1 to N:
        For j <- 1 to N-1:
            If (A[j] > A[j+1]:
                Swap(A[j], A[j+1])
            EndIf
        EndFor
    EndFor 
```
This may look similar to the sorting algorithm that you saw 

2. Work with your group to prove the correctness of this algorithm. Try and apply the following process: 

    1. Work through the algorithm on an example to convince yourself that it's correct, 
    2. Identify a loop invariant you can use to prove it's correctness, 
    3. Prove that your pseudocode starts with the invariant being true (the base case of recursion)
    4. Begin proving that your pseudocode maintains the loop invariant after every iteration (the inductive step)
    5. Much like with InsertionSort, BubbleSort has a nested for-loop structure, so to prove the inductive step, you will likely need to prove something about the behavior of the inner loop. Make a claim about what the inner loop does, and prove that via loop invariant! 
    6. Use the proof in (e) to finish your inductive step, and thus your proof by induction for your loop invariant for the outer loop.
    7. Conclude by showing that your loop invariant demonstrates the correctness of BubbleSort. 

3. If you have additional time (or on your own to review the material!), consider the following *recursive* algorithm to solve the search problem:

```plaintext
function LinearSearch(Array A, element e):
    if (length(A) == 0):
        return NULL
    if (A[1] == e):
        return 1
    else:
        return 1 + LinearSearch(A[2...N], e)
``` 

4. Work with your group to prove the correctness of this algorithm directly using induction. 
    a. Identify a base case where correctness is easy to prove.
    b. Determine what you are doing induction over (typically the size of your input), and whether strong or weak induction is needed.
    c. Make sure you consider all possible cases, using the definition of the search problem you saw in lecture.

4. **For credit**: Submit some artifact of your work to Moodle, including at least an attempt at a proof of correctness
