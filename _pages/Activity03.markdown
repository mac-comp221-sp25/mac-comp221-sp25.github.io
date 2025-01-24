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

1. Look back at the pseudocode you've written for Activities 1--2 (check your Moodle submissions)

2. Work with your group to prove the correctness of your algorithm. Try and apply the following process: Work through the algorithm to convince yourself that it's correct, Identify a loop invariant you can use to prove it's correctness, prove that your pseudocode starts with the invariant being true (the base case of recursion), and finally prove that your pseudocode maintains the loop invariant after every iteration. Note that the above only works for iterative algorithms: proving recursive algorithms correct is even more straightforward! Prove the base case returns the right answer, and show that the recursive step will return the right answer if all of it's recursive calls return the right answer (which should be true by our inductive assumption! In some cases you may need strong induction!).

3. If you're having trouble proving your algorithm is correct, try and see if you can identify a counterexample: maybe there's a case that your algorithm fails on! Try and correct it, if possible! Otherwise, prove *in*correctness by demonstrating that your pseudocode won't correctly sort your counterexample.

4. If you haven't completed any of the previous sorting activities, take this time to complete them. You should have collected (1) pseudocode for an intuitive sorting algorithm, (2) a big-Oh analysis of it's time complexity with a proof, and now (3) a proof of correctness!

6. **For credit**: Submit some artifact of your work to Moodle, including at least an attempt at a proof of correctness
