---
layout: post
title: "Activity 14: Minimum Spanning Trees and Prim's Algorithm"
categories: Activity MST graph Prims greedy
---

## Learning Goals

You will work towards being able to...

1. Be familiar with canonical algorithms (Prim's, Kruskal's) 

2. Translate problems into graph problems and solve them with cannonical graph algorithms (MST Problems)

3. Design and prove correct/incorrect algorithms based on Greedy design principles. 

## Warm-Up
Recall from the reading that a *Spanning Tree* $T = (V', E')$ of a graph $G = (V, E)$ *spans* the graph $G$ (i.e., $V' = V$) and is a *tree* (T is acyclic and connected). 

Suppose you had a *spanning tree* and added a new edge $e \in E \setminus E'$, constructing $T' = (V, E' \cup \\{ e \\} )$. Does $T'$ contain a cycle? Convince your table-mates!

As a bonus: How many edges **must** be in an MST? How do these two results interact?

## Activity

1. (Skiena 8-2) Since a Minimum Spanning Tree is connected, that means for any vertices $s, t \in V$, there is a path in the minimum spanning tree between them (i.e., by our in-class definitions, a sequence of edges $(s, v_1), (v_1, v_2) \dots (v_{k-1}, t) \in E'$). Is this path the *shortest* path in $G$ between those vertices? Check intuitions between people at your table. Come to a consensus, and then either prove it true, or construct a graph that presents a counterexample!

2. (Skiena 8-8a) Suppose you construct an MST $T$ for a weighted graph $G$. Then you construct a graph $G'$ where the weight of each graph is increased by exactly $k$. Does the MST necessarily contain the same edges? Convince yourself and this table that this is true!

3. (Skiena 8-8b) Suppose you have a shortest path from $s \in V$ to $t \in V$ in $G$. Using the $G'$ construction from the previous problem, does the shortest path in $G'$ always contain the same edges as the shortest path in $G$?

#### Submission
Submit an artifact of your work for problem 1, or 2 & 3. As a hint, all 3 rely on the same essential intuition!

---
