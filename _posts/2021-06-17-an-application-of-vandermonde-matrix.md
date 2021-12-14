---
layout: page
title: "An application of Vandermonde matrix"
author: "Felix Chen"
categories: journal
tags: [documentation,linear algebra]
---

In this post, we shall prove the following theorem:

_Let $T$ be a linear operator on a finite-dimensional vector space $V$. If $T$
possesses $n$ distinct eigenvalues, where $n=dim\,V$, then $V$ itself is a $T-
\mbox{cyclic}$ subspace._

Before we write down the proof, let's give an introduction to Vandermonde matrices.
A Vandermonde matrix is of the form

$$ V = \begin{pmatrix}
				1 & v_1 & v_1^2 & \cdots & v_1^{n-1} \\
				1 & v_2 & v_2^2 & \cdots & v_2^{n-1} \\
				\vdots & \vdots & \vdots & \ddots & \vdots \\
				1 & v_n & v_n^2 & \cdots & v_n^{n-1}
		\end{pmatrix} \mbox{.} $$

Its determinant is given by

$$ \tag{*} det(V) = \Pi_{i<j}(v_j-v_i) \mbox{,} $$

which can be established easily by elementary row and column oprations and induction on
$n$.

Having stated the property required, we proceed to prove our theorem.

**PROOF** Choose eigenvectors $\xi_1,\xi_2,...,\xi_n$ of $T$ corresponding to different
eigenvales $\lambda_1,\lambda_2,...\lambda_n$ so that the vectors chosen forms an
ordered basis for $V$. Put $\xi=\sum_i \xi_i$. We claim that $\beta=\\{\xi, T(\xi),...,
T^{n-1}(\xi)\\}$ generates $V$. It suffices to show that $\beta$ is linearly independent;
for then $\beta$ is another basis and hence spans $V$. Consider the coordinate vectors
$\eta_i$ of $T^i(\xi)$ relative to $\\{\xi_1,...,\xi_n\\}$, $i=0,1,...,n-1$. Observe that

$$ \eta_i = \begin{pmatrix}
				\lambda_1^i \\
				\lambda_2^i \\
				\vdots \\
				\lambda_n^i
				\end{pmatrix} \mbox{,} $$

Thus $V=(\eta_0\ \eta_1\ \cdots\ \eta_{n-1})$ is a Vandermonde matrix. Since the
$\lambda$'s are all distinct, by (\*), $det(V)\not=0$, from which it at once follows that
the $\eta$'s are linearly independent; consequently, $\beta$ is also linearly indepently,
as the coordinate vectors are obtained by a isomorphism. This complete our proof.

Finally, we mention in passing that a proof without the use of determinant can be given
with the help of the following lemma:

_Let $W$ be a $T$-invariant subspace of $V$. If $\xi_1+\cdots+\xi_n \in W$, where $\xi_1,
...,\xi_n$ are eigenvectors of $T$ with distinct eigenvalues, then $\xi_i \in W$ for
$i=1,...,n$._
