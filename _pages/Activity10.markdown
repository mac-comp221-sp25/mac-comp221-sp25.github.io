---
layout: post
title:  "Activity 10: Binary Search Variants"
categories: Activity Sorting Design
---

## Learning Goals

You will work towards being able to...

1. Understanding the core idea of common algorithms (BinarySearch)    

2. Turn algorithmic ideas into pseudocode

3. Apply Divide-and-Conquer design techniques to novel problems

## Instructions
Work with your groups on the following problems:

1. **Approximately how wrong**: Let's suppose we want to find a the decimal expansion of a root of a polynomial $f(n)$ to a certain *precision*. While Skiena tells us that each iteration of binary search gets us closer and closer to the true root, how much closer does each iteration get us? Suppose we have some polynomial $f(x)$ that is guaranteed to have some root $x$ that is between a given $l$ and $r$ (i.e., $\exists r$, $l \leq x \leq r$ such that $f(x) = 0$). Suppose we also have some notion of the precision we desire, $\varepsilon > 0$, and we want to find some $x'$ such that $x - \varepsilon \leq x' \leq x + \varepsilon$. Given all this, how many iterations of the bisection method do we need to call before we can guarantee we can pick such a $x'$? I recommend you first step through the algorithm a few times to get a feel for it's behavior, and then sketch out a concrete solution for a particular set of choices. Then try and generalize. If you're confident with that, prove this to be true by constructing a loop invariant!

2. **With great power comes great responsibility (with computing resources)**: Suppose you are a statistician consulting for psychologist. They are worried about statistical power for their upcoming experiment (i.e., they're concerned that they won't collect enough data from enough participants to make valid statistical inference). They've determined that if they don't have a statistical power $>0.8$, it's not worth running the experiment. However, they don't want to run too many participants, since they have to pay each one, and money is tight. Luckily, you know how to do a power analysis, a computationally intense algorithm that can determine the statistical power given a particular number of subjects. Call the number of subjects $n$. Luckily, you know one helpful fact: the more participants you run, the higher the power you have! What strategy would you use to guarantee the experiment has $>.80$ power, minimize the cost of recruiting participants, and minimize the amount of computational power spent (i.e., minimize the number of power analyses run?).[^1]

#### Submission
Submit an artifact of your work from either 1 or 2.  

---

[^1]: As you might have guessed from the detailed framing and my research area, [I did this](https://doi.org/10.31234/osf.io/y4peh) in some work I did a few years ago, though I was playing both roles. 
