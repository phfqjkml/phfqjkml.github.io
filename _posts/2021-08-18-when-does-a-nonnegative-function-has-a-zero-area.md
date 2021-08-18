---
layout: page
title: "When does a Nonnegative Function has a Zero Area?"
author: "Felix Chen"
categories: journal
tags: [documentation,real analysis]
---

It is clear that if $f$ is a nonnegative Riemann-integrable function on $[a,b]$
and its zero set is dense in $[a,b]$, then $$\int f=0$$. The converse is also
true!

**Lemma** If $f>0$ and $f\in\mathscr{R}$ on $[a,b]$, then $\int^b_af>0$.

**Proof** Clearly, $\int f\geq 0$. Suppose $\int^b_a f=0$. There then exists a
partition $P=\\{x_0,...,x_p\\}$ of $[a,b]$ such that

$$U(P,f)<b-a\text{;}$$

whence

$$\sup_{x_{j-1}\leq x\leq x_j}f(x)<1$$

for some $j$. Let $I_1=[x_{j-1},x_j]$. Simiarly, since $\int^{x_j}_{x\_{j-1}}f=0$,
there exists a partition $Q=\\{y_0,...,y_q\\}$ of $I_1$ such that

$$U(Q,f)<\frac{x_j-x_{j-1}}{2}\text{.}$$

Hence

$$\sup_{y_{k-1}\leq x\leq y_k}f(x)<\frac{1}{2}$$

for some $k$. Let $I_2=[y_{k-1},y_k]$. Continuing in this fashion, we then obtain
a sequence $\\{I_n\\}$ of intervals such that\
(a) $I_1\supset I_2\supset I_3\supset\cdots$;\
(b) $f(x)<\frac{1}{n}$ if $x\in I_n$, for each $n$.\
By (a), there exists $\xi\in\cap I_n$. By (b), $f(\xi)<\frac{1}{n}$ for all $n$.
Therefore, $f(\xi)=0$, a contradiction. Thus, $\int f>0$.

**Theorem** Suppose $f\geq0$ on $[a,b]$, $f\in\mathscr{R}$ on $[a,b]$, and $\int f=0$.
Then the zero set $Z$ of $f$ is dense in $[a,b]$.

**Proof** Assume to the contrary that $Z$ is not dense in $[a,b]$, and assume $f(x)\not=0$.
We can find $r>0$ such that

$$f(t)>0$$

whenever $\left\|t-x\right\| <r$, $t\in [a,b]$. Hence by the lemma,

$$ \int^b_a\geq \int_{t\in [a,b]\cap[x-\frac{r}{2},x+\frac{r}{2}]} f>0 \text{,} $$

which is asurd.
