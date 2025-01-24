---
layout: post
title: "Activity 16: Max-Flow and Ford-Fulkerson"
categories: Activity max flow min cut ford-fulkerson
---

## Learning Goals

You will work towards being able to...

1. Familiarize youself with canonical algorithms (Ford-Fulkerson/Edmonds-Karp)

2. Prove the (in)correctness of algorithmic techniques.

## Activity
### Part 1
Today, Let's walk through the development of a max-flow algorithm using the Ford-Fulkerson method!

1. First, we'll note that the pseudocode provided in class for Ford-Fulkerson is *underspecified*: **write out the steps of the pseudocode in a more concrete manner**. Arrive at consensus with your tablemates about how you might find an augmenting path (the tricky part of the implementation)! Note that we'll also know when $s$ and $t$ are disconnected when this path finding algorithm fails to find a path, which will allow us to set our termination condition for our while loop! 

    > ###### HINT
    > Observe that an edge $e$ is only in the residual graph $G_r$ iff the remaining capacity $c(e) - f(e) > 0$. 
    > Note that we should be able to do this in (graph) linear time ($O(\lvert V \rvert + \lvert E \rvert)$).
    {: .block-tip}

2. Now we need to figure out that a Ford-Fulkerson implementation is *correct*. In order to do that, we need to first determine that the flows that we compute are *real* flows. That is, they satisfy the four properties of flows: that the flow through an edge respects the capacity of the edge ($f(e) \leq c(e)$ for all $e \in E$), that flow values are symmetric $f((v_1, v_2)) = -f((v_2, v_2))$, that the in-flow and out-flow at each vertex are equal ($\sum_{(v, w) \in E} f((v,w)) = \sum_{(w, v) \in E} f((w,v))$ for all non-source or target vertices), and that the flow out of $s$ matches the flow into $t$ ($\sum_{(s, v) \in E} f((s,v)) = \sum{(v, t) \in E} f((v,t))$). For each of these, briefly convince yourself that these properties are (1) true before the while loop begins and (2) are maintained for every iteration (i.e., are loop invariants!). Convince yourselves that you could prove this, if asked!

3. To finish a proof of correctness, we need to prove that flow if *minimal*. Of course, we need to compute the flow value in the first place! I left that out! How would you compute the max-flow given the structure of the algorithm (i.e., what do you return?)? Once you have that, how would you argue for this value being the cost of the minimum cut between $s$ and $t$? Since we have a result that tells us that the maximum-flow **is** the minimum cut, this is what's left to show!

4. Now let's think about the time complexity of this algorithm: What is the time complexity of everything *inside* the while-loop? Now suppose all of our costs are integers ($c:E \to \mathbb{Z}$) and our max flow is some value $F$. How many iterations can the while loop run? Given that, what's the runtime of this algorithm?[^1]

    > ###### HINT
    > Every time we find an augmenting path, what is the minimum amount the flow we compute must increase?  
    {: .block-tip}

#### Submission
Submit an artifact of your work on Moodle. 

---
[^1]: If you use a particular algorithm to find augmenting paths, you can prove that this algorithm runs in $\Theta(\lvert V \rvert \lvert E \rvert^2)$ time even for real-valued capacities. This particular implementation is called the *Edmonds-Karp* algorithm.
