# Index Calculus

In this short note we will discuss the discrete logarithm problem and also look at an implementation of a few probabilistic algorithms for computing discrete logarithms. These algorithms are collectively classified as index calculus algorithms.

The problem of computing discrete logarithms can be summarized as follows. 
Letting <img src="https://render.githubusercontent.com/render/math?math=q"> be a prime power, the multiplicative subgroup <img src="https://render.githubusercontent.com/render/math?math=\mathbb{F}_q^* \leq \mathbb{F}_q"> is cyclic. Elements that generate this cyclic subgroup are called primitive. If we are given a primitive element <img src="https://render.githubusercontent.com/render/math?math=g \in \mathbb{F}_q"> as well as any <img src="https://render.githubusercontent.com/render/math?math=h\in\mathbb{F}_q^*">, then the discrete logarithm of $h$ with respect to $g$ is the integer <img src="https://render.githubusercontent.com/render/math?math=x, 0 \leq x \leq q-1"> such that $g^x = h$. We will denote this by the usual <img src="https://render.githubusercontent.com/render/math?math=x = \log_g h\mod q">. The goal is to find this $x$ given $q, g$ and $h$. 

We will start by looking at some naive implementations of index calculi and then refine our approaches in later sections.
