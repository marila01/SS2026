---
aliases:
  - "Definition: Norm"
---
# Definition: Norm

A mapping $\lVert\cdot\rVert : X \to \mathbb{R}$ on a vector space $X$ over $\mathbb{K} \in \{\mathbb{R}, \mathbb{C}\}$ is a **norm**, if the following three conditions hold:

1. $\forall x \in X : \bigl(\lVert x\rVert = 0 \Rightarrow x = 0\bigr)$  
   $\lVert\cdot\rVert$ is **definite**.
2. $\forall x \in X\; \forall \lambda \in \mathbb{K}: \; \lVert \lambda x\rVert = |\lambda|\,\lVert x\rVert$  
   $\lVert\cdot\rVert$ is **homogeneous**.
3. $\forall x,y \in X : \; \lVert x+y\rVert \le \lVert x\rVert + \lVert y\rVert$  
   $\lVert\cdot\rVert$ satisfies the **triangle inequality**.
