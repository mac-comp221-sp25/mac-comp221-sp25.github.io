---
layout: post
title:  "Skiena Problem 2-5"
categories: Activity Sorting
---

Let this be a reminder for me to pick less tricky problems. Given the number of mistakes I've made prepping and solving this live, here is my authoritative analysis of the time complexity of this algorithm. 
## Lower bound

I didn't present this in class (maybe hinted at it in one of the sections?), but I'll demonstrate how you can derive a lower bound!

We showed in class that the print statement runs approximately (up to rounding errors) $\sum_{k=1}^n (\log(n/k))$ times.

Here's a trick: Since $\log(x) \geq 0$ for $x \geq 1$, we know each term in this sum is positive. So by removing some of the terms, we only make the sum smaller! Let's get rid of half of the terms, so

$$ \sum_{k=1}^n \log(n/k) \geq \sum_{k=1}^{n/2} \log(n/k) $$

Note that I'm assuming that $n$ is even and thus $n/2$ is an integer. You can convince yourself this won't matter in the end! 

Now we should observe that the logarithm is an increasing function, which means that 

$$ \sum_{k=1}^{n/2} \log(n/k) \geq \sum_{k=1}^{n/2} \log(n/(n/2)) $$

I.e., we replace each of the terms in the sum with the smallest term to get a lower bound! But, that simplifies!

$$ \sum_{k=1}^{n/2} \log(n/(n/2)) = \sum_{k=1}^{n/2} \log(2) = \log(2)n/2 $$

So, summing it all up (ha!), we find that our growth function is bounded from below by $(\log(2)/2) n$, so with $c = \log(2)/2$ and $n_0 > 1$, we have that our function is $\Omega(n)$. 


## Upper bounds
I'll present 2 upper bounds. A looser upper bound that I showed in class, and a stricter upper bound that requires a trick I won't expect you to know off the top of your head.

In class, I demonstrated that the algorithm is $O(n\log(n))$.

We showed in class that the print statement runs approximately (up to rounding errors) $\sum_{k=1}^n \log(n) - \sum_{k=1}^n \log(k)$ times (we showed this is equivalent to what I claimed in the lower bound section in class!)

Since $\log(k) > 0$ for $k > 1$, and the index k counts up from 1, we know that $\sum_{k=1}^n \log(k)$ is positive! That lets us bound the runtime from above by the first term. That is

$$ \sum_{k=1}^n \log(n) - \sum_{k=1}^n \log(k) \leq \sum_{k=1}^n \log(n) $$

and since the $\log(n)$ in the last term doesn't care about the index $k$ of the summation, $\sum_{k=1}^n \log(n)$ is simply $n\log(n)$.

This is (silliness aside), the upper bound I showed in class, and the one I'll expect you to be able to pull out at a moment's notice. However, it turns out we can do better! 

Above, we had a really weak bound on $\sum_{k=1}^n \log(k)$ --- just that it's positive! But it turns out there's a very *fancy* approximation of this value. [Stirling's Approximation](https://en.wikipedia.org/wiki/Stirling%27s_approximation) tells us that $\log(n!) = n\log(n) - n\log(e) + O(\log(n))$, with that last term just indicated something of order $\log(n)$. This may not seem like it applies, but...

$$ \sum_{k=1}^n \log(k) = \log(\prod_k^n k) = \log(n!) $$

Remember sums of logs are logs of products! So, we can reduce as follows:

$$\begin{aligned} \sum_{k=1}^n \log(n) - \sum_{k=1}^n \log(k) &= n\log(n) - \log(n!) \\
 &= n\log(n) - n\log(n) + \log(e)n - O(log(n)) \\
 &= \log(e)n - O(\log(n)) \end{aligned}$$

Which should clearly look $O(n)$ (note that n dominates anything $O(\log(n)$, so picking $c\geq log(e)$ will allow you to find some $n_0$ to satisfy the definition of $O(n)).

## The Theta

Since we saw that the algorithm is both $O(n)$ and $\Omega(n)$, it is $\Theta(n)$ (by my definition! If you haven't already, convince yourself that this is the same as the book's big-$\Theta$ analysis.

## In Summary
 I messed this up (my prep was lacking!), and so if Stirling's Approximation ever comes up, I'll be sure to give it to you. And I'll try not to pick questions tricky enough to trick me. My bad, hope making you read more math helps!
