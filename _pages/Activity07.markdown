---
layout: post
title:  "Activity 07: Heap- & TreeSort"
categories: Activity DataStructures Sorting TreeSort HeapSort
---

## Learning Goals

You will work towards being able to...

1. Build and reason about algorithms that use data structure-based design principles

2. Understanding the core idea of, write pseudocode for, and analyze the runtime and correctness of common algorithms (HeapSort and TreeSort)

3. Understand sorting as a pre-processing step for solving common algorithmic problems. 

## Instructions
Work with your groups on the following problems


#### HeapSort Review
1. If you've completed the reading response, share and discuss your pseudocode for your heap insert and removemin operations. Hopefully you've converged on a $\log n$ time complexity for each, where $n$ is the size of the heap. 

2. Manually step through the operations of a HeapSort call with an array of size 5. You may choose any 5 Integers as the entries of the array. Create some artifact of your work (notes, pictures, etc.) that you can submit to Moodle!

#### Thinking about TreeSort's Design 
1. Write out pseudocode for TreeSort, which works by inserting each element of our array into a Binary Search Tree and filling in a new array by reading out the search tree's in-order traversal.

2. Skiena had us think about HeapSort as a variant of SelectionSort. While SelectionSort found the minimum unsorted element in our array with a linear search, the key idea (under this view) of HeapSort was that min-heaps provide a more efficient way of repeatedly finding the minimum remaining (unsorted) element. This is the core principle of Data Structure Design: We take a simple, intuitive algorithm and find a data structure (or sometimes construct a bespoke data structure!) to make some of the clunkier operations in the algorithm faster. This principle can also be used to think about TreeSort! 

Consider the behavior of your TreeSort pseudocode, but for our purposes here, let's ignore the fact that we need to transform the in-order traversal of nodes into an Array at the end. Simply treat the in-order traversal of the tree as the state of an array. Does this resemble another sorting algorithm you've seen? Can you describe TreeSort as a variant of one of those $\Theta(n^2)$ sorts where a (Self-Balancing) Binary Search Tree improves the efficiency of a part of that algorithm?

**Bonus:** Lets begin analyze TreeSort's correctness (and runtime, if we didn't discuss this in lecture!). You'll find (similar to HeapSort) that the correctness of this algorithm relies on a property of a binary search tree: That it's in-order traversal is sorted! Use the following definitions:

A sequence $a_1, \dots a_n$ is *sorted* iff $a_1 \leq a_2 \leq \dots \leq a_n$. A sequence $a_1, \dots, a_n$ is an *in-order traversal* of a binary tree $T$ iff each $a_i$, $1 \leq i \leq n$ uniquely maps to the value of a node in $T$ (something, something, a bijection exists for the math majors) and for any $a_i$ and it's corresponding node $N$, the value of each node in the left subtree of $N$, $a_j$  has index $j < i$ and every element in it's right subtree of $N$, $a_k$, has index $k > i$. A *binary search tree* is a tree $T$ such that for every node $N$ with value $m$ in the tree, every value $l$ in the left subtree of $N$ has $l \leq m$ and for every value $r$ in the right subtree of $N$ has $r \geq m$. Note that this slightly extends Skiena's definition, which assumes our trees do not contain duplicates. 

and write pseudocode for an in-order traversal (recalling it's recursive structure from 128). Try and show: (1) the pseudocode you wrote is correct, by the definition of an in-order traversal I have given you above, (2) that if this is run on a binary search tree, the in-order traversal must be sorted.

#### Submission
Submit an artifact of your work from the HeapSort portion of this assignment, as well as your TreeSort pseudocode. 
