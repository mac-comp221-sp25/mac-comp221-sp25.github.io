---
layout: post
title: "Graph Applications"
categories: Activity Graph 
---

## Learning Goals

You will work towards being able to...

1. Translate problem specifications into graph problems to be solved with standard algorithms.

## Instructions
Work with your groups on the following problems. You may work on them in any order:

#### Problem 1: Two-Tabled Wedding (Skiena 7-15): 
You are organizing seating for a wedding where all guests in a list $V$ must be organized into two tables. You also have a list $E$ of pairs of people who hate each other. Discuss how you might, if possible, construct a table assignment that avoids any enemies being at the same table. What kind of a graph problem is this?

#### Problem 2: Covering for a Friend (Skiena 7-18)
A *Vertex Cover* for a graph $G = (V, E)$ is a set $V' \subset V$ (a subset of $V$ such that ever edge is *incident* to some $v \in V'$ (formally, $\forall (v_1, v_2) \in E$, either $v_1 \in V'$ or $v_2 \in V'$). Informally, this just means for every edge, at least one vertex on the end of that edge is in $V'$.

Suppose you have $\lvert V \rvert$ people working on $\lvert E \rvert$ projects in teams of 2. You want to organize a meeting where at least one person on each project is present to talk about progress on that project. This is a vertex cover problem --- identify the vertices and edges of the implicit graph and convince yourself the solution is a vertex cover!

Skiena 7-18 suggests one algorithm for finding a vertex cover is building a DFS tree and pruning the leaves. Prove, given what you know about edges in a DFS tree, that this is always a vertex cover. Note that by Skiena's definition, we disallow self-edges in our graphs!

#### Problem 3: A Stop Along the Way (Skiena 8-19)

Suppose you have a set of cities and edges representing roads connecting them. Edges are weighted with the travel time between the relevant cities. Determine an algorithm to find the shortest path between city $s$ and city $t$ that makes a stop at city $v$ along the way!

#### Problem 4: Height Limited Shortest Paths (Skiena 8-22)

Suppose you have a set of cities and of roads connecting pairs of cities. For each road, you are told the maximum allowable height of a vehicle navigating that road. Construct an algorithm to find the maximum height of a vehicle that could successfully transit from city $s$ to city $t$.

### Submission
Submit an artifact of your work for one of the two problems.

