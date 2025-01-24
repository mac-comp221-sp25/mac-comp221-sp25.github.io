---
layout: post
title: "Activity 20: Complexity Theory and Hardness Reductions"
categories: Activity complexity theory hardnesss reduction
---

## Learning Goals

You will work towards being able to...

1. Design reductions to prove the hardness of problems

## Activity
Work with your groups to work through the following problems. For these in particular, discuss at your tables to make sure everyone comes to agreement!

### Day 1

1. Suppose a problem $X$ is tractable, and you have an algorithm that runs in polynomial time that turns a solution from problem $X$ into a solution for problem $Y$. Can you tell if Problem $Y$ is tractable? If so, is it?

2. Suppose a problem $X$ is intractable, and you have an algorithm that runs in polynomial time that turns a solution from problem $X$ into a solution for problem $Y$. Can you tell if Problem $Y$ is tractable? If so, is it?

3. Suppose a problem $Y$ is intractable, and you have an algorithm that runs in polynomial time that turns a solution from problem $X$ into a solution for problem $Y$. Can you tell if Problem $X$ is tractable? If so, is it?

4. Suppose a problem $Y$ is tractable, and you have an algorithm that runs in polynomial time that turns a solution from problem $X$ into a solution for problem $Y$. Can you tell if Problem $X$ is tractable? If so, is it?

5. Raise your hand and check your answers to each of these questions!

### Day 2

1. (Skiena 11-4) *Stingy SAT* is a problem that that asks, given a set of clauses (that is, disjunctions of literals) and $k \in \mathbb{Z}_{\geq 0}$, determine whether there is an assignment of boolean values to variables such that each clause evaluates to true *and* at most $k$ of the variables are assigned to true. Prove that this is NP-hard!

    > ###### Hint
    > Reduce this from an instance of the SAT problem![^1]
    {: .block-tip}

2. (Skiena 11-10) The *(Minimum) Set Cover* problem provides you a set $X$, a set of subsets of $X$ called $F$, and asks you to find the smallest subset of $F' \subseteq F$ such that $X \subseteq \bigcup_{S \in F'} S$. That is, select the fewest number of subsets from $F$ such that the union of those subsets contains every element in $X$. A Set-Cover *decision* problem asks, for $F$, $X$, and $k \in \mathbb{Z}_{\geq 0}$ if there exists $F' \subseteq F$ that is a set cover w.r.t. $X$ and $\lvert F' \rvert \leq k$. Working with the decision problems, Assuming Vertex Cover is NP-Hard, prove Set Cover is NP-Hard via a reduction. 

3. Provide a *verification* algorithm for Set Cover. That is, given a potential solution to the set cover problem, provide an algorithm to verify it. Show that this verification can be done in polynomial time (i.e., Set Cover is NP-Complete). 

### Day 3

3. Recall that a *clique* in a graph $G=(V, E)$ is a set of vertices $C \subseteq V$ such that every $v, w \in C$ are connected (i.e., $(v,w) \in E$). The clique decision problem asks, given a graph $G = (V, E)$ and $k \in \mathbb{Z}_{\geq 0}$, if a clique of size $\geq k$ exists in $G$. Suppose you consider a simplified version of the problem where you're guaranteed that $G$ only contains vertices with degree $\leq k$. Prove that this problem is tractable (i.e., find a polynomial-time solution). 

#### Submission
Submit an artifact of your work on Moodle. 

---
[^1]: The reductions we've looked at thus far are called *Turing* (or sometimes *Cook*) reductions. A more restricted class or reductions that require that you can translate the *inputs* of Problem Y into inputs of Problem X such that the solution to that problem instance for problem X is also the solution to the original instance of Problem Y is called a *Karp* or *Many-One* reduction. That is, you can find a function that maps inputs for Problem Y into inputs for Problem X that have the same solution. Given how restricted Karp reductions are, they are more powerful than Turing reductions, and are the standard kind of reduction in complexity theory. 
