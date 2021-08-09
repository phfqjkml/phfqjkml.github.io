---
layout: page
title: "Baby Rudin Theorem 7.13"
author: "Felix Chen"
categories: journal
tags: [documentation,real analysis]
---

> Suppose $K$ is compact, and \
> (a) $\\{f_n\\}$ is a sequence of continuous functions on $K$, \
> (b) $\\{f_n\\}$ converges pointwise to a continuous functions $f$ on $K$, \
> (c) $f_n(x)\geq f_{n+1}(x)$ for all $x\in K$, $n=1,2,3,...$. \
> Then $f_n\rightarrow f$ uniformly on $K$.

**ALTERNATIVE PROOF** Clearly $f_n\geq f$ for all $n$. Let $\epsilon>0$. Since
$\lim f_n=f$ and $f_n-f$ is continuous, to each $x\in K$ there correspond an
integer $N(x)$ and a neighborhood $V(x)$ such that

$$ 0\leq f_{N(x)}(t)-f(t)<\epsilon $$

provided that $t\in V(x)$. By compactness of $K$, there are finitely many points
$x_1,...,x_m\in K$ such that

$$ K\subset V(x_1)\cup\cdots\cup V(x_m) \mbox{.} $$

Put $N=\max(N(x_1),...,N(x_m))$. It follows that

$$ 0\leq f_n(x)-f(x)<\epsilon\quad(x\in K) $$

for all $n\geq N$. This means exactly that $f_n\rightarrow f$ uniformly.