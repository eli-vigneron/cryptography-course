# Index Calculus summary

In this short note we will discuss the discrete logarithm problem and also look at an implementation of a few probabilistic algorithms for computing discrete logarithms. These algorithms are collectively classified as index calculus algorithms.

The problem of computing discrete logarithms can be summarized as follows. Letting $q$ be a prime power, the multiplicative subgroup $\mathbb{F}_q^* \leq \mathbb{F}_q$ is cyclic. Elements that generate this cyclic subgroup are called primitive. If we are given a primitive element $g \in \mathbb{F}_q$ as well as any $h \in  \mathbb{F}_q^*$, then the discrete logarithm of $h$ with respect to $g$ is the integer $x, 0 \leq x \leq q-1$ such that $g^x = h$. We will denote this by the usual $x = \log_g h \mod q$. The goal is to find this $x$ given $q, g$ and $h$. 

We will start by looking at some na\"ive implementations of index calculi and then refine our approaches in later sections.