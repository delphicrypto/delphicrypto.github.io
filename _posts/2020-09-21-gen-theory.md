---
title: Lecture Notes -- No Free Lunch and Occam's Generalization Bound 
date: 2020-09-21
categories:
- Deep Learning Theory
---

**Published:** 12.05.2020

**Paper Author:** Simon Lacoste Julien 

**Full Notes:** [webpage](http://www-labs.iro.umontreal.ca/~slacoste/teaching/ift6132/W20/lectures.html)

Estimate $$h_w : \mathcal{X} \rightarrow \mathcal{Y}$$. How do we evaluage $$h_w$$?

$w$ is the parameters.

Normally use the generalization error, $$L_{p(w)} = \mathbb{E}_{(x,y) \sim p} [l(x(, h_w(x))])] $$ where $$p$$ is the unknown distribution..

The idea is, what is the expected value on the test distribution $$p$$?

I look at how my prediction rule is doing on this test distribution.

Total goal is to find $$ w^* = argmin_{w \in W} L_p(w)$$ in the case of an oracle. But we don't usually know it.

In training, suppose we have $$(X^{(i)}, Y^{(i)})  \sim p $$ i.e. points from the same distribution as I test, we can use the empirical distribution as what we care for.

Then I get $$\hat{L}(w) = \frac{1}{n} \sum_{i=1}^n l(y, h_w(x)) $$ doing this is already difficult. For example when we train a neural network we use the cross entropy which is not the same as the 0-1 error which is harder to compute.

This is an empirical version of the test error.

We know that pointwise, the empirical error will converge to the true value of the test error for $$w$$, $$L_n{w} \rightarrow L_p(w)$$, true pointwise for a fixed $$w$$, as $$n \rightarrow \infty$$

This is weaker than saying $$sup_w \hat{L})n(w) - L_p(w) \rightarrow 0$$, this is a uniform convergence result but we don't usually have this.

If the way you pick your $$w$$ is by minimizing a regularized version of the empirical error $$\hat{L}$$, needs to be close to the test error.

As long as in the neighbourhood of the minimum, the empirical and the true are similar thats what we want.

## No Free Lunch

Say we have a learnign algorithm, $A$, we call the whole training set $$\mathcal{D}_n$$ with $$n$$ training samples.

$$A$$ is a function $$A: D_n \rightarrow \mathcal{H}$$, $$A(D_n) = h$$, the hypothesis is $$A$$ applied to the dataset.

When we do learning theory we want to analyze the properties of the algorithm when the distribution changes, when the function changes etc.

We want a probabilistic staetment about the learning algorithm depending on the training set.

The simplest analytic tools for an estimator or an algorithm is looking at how it does in average (frequentist risk) $$R^f_{p,n}(A) = \mathbb{E}_{D_n \sim p \odot n}[L_p(A(D_n)]$$,

$$D_n$$ is the random variable. This is looking at how well the algo does over all possible training sets on average.

### No Free Lunch Theorem

Say we're doing binary classification over a finite set of inputs, it's possible to find a learning algo which will do well uniformly over all possible data distributions.

Thm 1. For any learning algorithm $$A$$, then if you look at the worst distribution for frequentist risk, $$sup_{all dist} [R^{p} (A;n) - L_p(h^*_p)] \geq \frac{1}{2}$$ when the input space is finite.

This means that there always exists a distribution $$p$$ such that the learning algo is worse than random predictions (since this is binary classification).

I can always find a bad distribution for any learning algorithm.

NFL keeps in mind claims that if you claim something does well everywhere, there must be some assumptions.

## Occam's Generalization Error Bound

For binary classification with 0-1 loss, $$l(y,y') = \mathbb{1}_[y \neq y']$$.

We consider the parameter set $$W$$ to be infinite countable.

We define a prior over this set, we can think of it as a complexity measure, $$\pi(w)$$, i.e. $$\sum_{w \in W)} \pi (w) = 1, \pi (w) \geq 0 \forall w$$.

$$\vert w \vert_{\pi}$$ is a description length, and it will be $$\log_2 \frac{1}{\pi(w)}$$ if a parameter is more probable, use shorter code, and vice versa.

$$\sum_w 2^{-|w|_\pi}$$

Generalization error will be upper bounded by the training error.

There will be a complexity term, the number of examples I need will depend on the complexity I assigned to a specific parameter.

Example: if you use $$\pi (w) \sim \mathcal{N}$$, gaussian prior, we get that the description length will be $$\vert\vert w \vert \vert^2$$


Proof


1) Chernoff Bound (concentration inequality). When I make an empirical average, it's not so far from the true average and we characterize how far. In the case of an iid training set for binary classification: $$P(D_n : \hat{L_n(w)} \leq L(w) - \epsilon )$$


und is only useful if both the empirical error and the complexity is small.

It's easy to have generalization error bounds bigger than one.

Observation 1. Minimizing right hand side of bound gives you a learning algorithm, because RHS is something defined prior and doesn't depend on distribution. And the learning algo is always uniformly consistent.This means that when $n$ goes to infinity, the result of the learning algo with converge to the best test error in the class (but can converge very slow which is the no free lunch part) The algo will do well for distributions where the complexity of the optimal classifier is small, because the empirical error will be small and the complexity will be small, which gives a tight bound. For example, on a neural net, if just minimize empirical risk there is no free lunch. if add complexity term, will do well for the parameters which has small complexity. 


