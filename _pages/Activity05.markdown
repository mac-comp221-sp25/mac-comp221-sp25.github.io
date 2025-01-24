---
layout: post
title:  "Activity 05: Brute Force Algorithms"
categories: Activity Design
---

## Learning Goals

You will work towards being able to...

1. Design brute-force algorithms to solve problems.

2. Determine the tiem complexity growth function for pseudocode under the RAM model.

3. Compute big-$O$/$\Omega$/$\Theta$s from time complexity growth functions. 

4. Convert intuitive algorithmic ideas into pseudocode.



## Instructions
For each of the problem specifications below, try and design a brute-force solution to each. Write out pseudocode for your solution, find the worst-case time complexity (big-$\Theta$), and convince yourself of correctness. For practice, write out formal proofs (or at least convince yourself you could, if asked!). 

1. **Substring Match**: You're given Strings $s_1, s_2$ of lengths $n$, $m$ and must return an integer index $i$ such that $s_1[i\dots i+m-1] = s_2$. For example, with 1-indexing, $s_1$ = E X A M P L E, $s_2$ = A M P means that a algorithm should return $3$. 

2. **Primality Testing**: A prime number is a number $p$ such that $\forall 2 \leq k < p$, $p \mod k \neq 0$ (that is, no integer between $2$ and $p-1$ evenly divides $p$). A primality testing algorithm takes a natural number $k$ as input and returns true if $k$ is prime and false otherwise. For a example, $7$ is prime (and the algorithm should return true) because $2, 3, 4, 5, 6$ do not divide $7$ evenly, but $6$ is not (and the algorithm should return false) because $2$ and $3$ evenly divide into $6$.

3. **Tic-Tac-Toe**: Tic-tac-toe is a two player game where players take turns placing markers (x's or o's, depending on the player) on a 3x3 grid. A player wins when their marker appears in all squares in a row, column, or diagonal (i.e., 3-in-a-row on a 3x3 grid). If the board is filled and neither player accomplishes this, the game is a draw. Generalize the game to boards of size $k$x$k$, where a player wins when their marker appears $k$ times in a row, column, or diagonal. A tic-tac-toe solver is an algorithm that, given a current board state represented by a $k$x$k$ two-dimensional array and which player moves next, returns 1 if player 1 has a sequence of moves that is guaranteed to win, 2 if player two has such a sequence of moves, or 0 if neither player has such a sequence of moves (i.e., if both players play optimally, the game will end in a draw).

    > ##### *HINT 1* 
    > This may be a problem where you want to take greater advantage of the flexibility of pseudocode, as there are... well... uninteresting parts of this problem that require a substantial bit of clunky code to write out. Pseudocode will help you avoid this (but thinking about time-complexities won't let you avoid the complicated bits). For example, don't worry about how an x, o, or empty square is represented: Just assume you can ask whether a particular square is filled and, if so, which marker it's filled with!
    {: .block-tip}

    > ##### *HINT 2* 
    > Make sure you consider all of the various branching paths that result from the opposing player's moves. Can you frame this problem in terms of simpler subproblems of the same type? Maybe your solution should be recursive!
    {: .block-tip}

#### Submission
Submit pseudocode for your solution to at least 1 or 2, as well as a big-Oh time complexity (you should do at least one runtime analysis + sketch out the proof of correctness, but that won't be necessary by Wednesday). 
