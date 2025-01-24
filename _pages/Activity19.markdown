---
layout: post
title: "Activity 19: Dynamic Programming Practice 2"
categories: Activity dynamic programming dp 
---

## Learning Goals

You will work towards being able to...

1. Design dynamic programming solutions to algorithmic problems

## Activity
For each of the following questions, design a recurrence relation, and then provide pseudocode for a dynamic programming algorithm to solve it. Consider the time and space complexity of your solutions. **It may be helpful to play around with the problem specification to build intution (i.e., work through an example!) before jumping to designing an algorithm**.

### Day 1

1. Write out pseudocode for the edit distance algorithm we discussed in lecture.  

### Day 2

1. Write out pseudocode for the CKY Parsing distance algorithm we discussed in lecture.  

### Days 1--3

1. (Skiena 10-6) Modify the edit distance algorithm we've discussed to allow for *transposition errors*, where at the cost of one operation, you can swap two adjacent characters. Convince yourself that your recurrence works, and run your pseudocode on the "steve"/"setve" pair Skiena gives you. 

2. (Skiena 10-7) Suppose you have 3 strings, $x, y, z$, where $\lvert z \rvert = \lvert x \rvert + \lvert y \rvert$. $z$ is a shuffle of $x$ and $y$ if it interleaves characters from $x$ and $y$ preserving their order. That is, you take $x$ and insert all characters of $y$ into the string such that the order of characters in $y$ are preserved. See Skiena 10-7a for examples --- confirm that they make sense! Then write a dynamic programming algorithm (based on the structure of edit distance!) that determines whether $z$ is a shuffle of $x$ and $y$. 

3. (Skiena 10-23) In some programming languages, the cost of spliting a string of length $n$ into two pieces is $\Theta(n)$. This happens in languages where strings are *immutable*, and thus must be copied for string operations like this! For simplicity, let's assume it actually takes exactly $n$ time steps. Suppose you want to make a sequence of splits such that the original string $s$ ends up split at positions $P = \{p_1, p_2, \dots, p_k\}$. That is, we want to conduct a series of splits such that we end up with $s[0\dots p_1], s[p_1+1, \dots p_2], \dots, s[p_k+1\dots n]$. What order of splits will get you those splits the fastest? Design an $\Theta(n^3)$ algorithm to find the minimum cost of splitting the strings in this way.

    For example, if $P = [3, 8, 10]$ and $n=20$, Splitting first at 3 takes 20 time steps, then at 8 takes 17, and finally at 10 takes 12, resulting in 49 time steps! Going in the reverse order, splitting at 10 takes 20, then at 8 takes 10, and finally at 3 takes 8, totalling 38.

    > ###### Hint
    > Think back to CKY Parsing!
    >
    {: .block-tip} 

#### Submission
Submit an artifact of your work on Moodle. 

---
