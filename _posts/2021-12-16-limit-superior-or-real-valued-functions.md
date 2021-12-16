---
layout: page
title: "Limit Superior of Real-valued Functions"
author: Felix Chen
categories: journal
tags: [documentation,real analysis]
---

**DEFINITION**\
Suppose $X$ is a metric space, $E\subset X$, $f$ maps $E$ into $\mathbb{R}^1$,
and $p$ is a limit point of $E$.\
Define a set $L$ of extended real numbers as follows: If $\{p_n\}$ is a sequence
in $E$ converging to $p$ with $p_n\not=p$, and if $f(p_{n_k})\rightarrow l$
for some subsequence $\{p_{n_k}\}$, then $l\in L$.\
Put

$$\limsup_{x\rightarrow p}f(x)=\sup L$$

and

$$\liminf_{x\rightarrow p}f(x)=\inf L\mbox{.}$$

**THEOREM 1**\
(a) If $y>\limsup_{x\rightarrow p}f(x)$, then there exists $\delta>0$ such that
$f(x)<y$ whenever $0<d(x,p)<\delta$, $x\in E$. \
(b) If $y<\lim\sup_{x\rightarrow p}f(x)$, then for every $\delta>0$, there exists
$x\in E$ with $0<d(x,p)<\delta$, such that $f(x)>y\mbox{.}$\
A similar result is valid for $\liminf$.

**PROOF**\
(a) Suppose to every $\delta>0$ corresponds $x\in E$ such that $0<d(x,p)<\delta$
and $f(x)\geq y$. Take $\delta=\frac{1}{n}$, $n=1,2,3...$. We then obtain a sequence
$x_n\rightarrow p$, $x_n\not=p$ such that

$$f(x_n)\geq y\mbox{.}$$

Letting $n\rightarrow\infty$, we get

$$\limsup_{x\rightarrow p}f(x)\geq \limsup_{n\rightarrow\infty}f(x_n)\geq y\mbox{.}$$

This proves (a).\
(b) Since $y<\sup L$, $l>y$ for some $l\in L$, which means that there exists a sequence
$x_n\rightarrow p$, $x_n\not=p$ such that $f(x_n)\rightarrow l$. Since $l>y$, $f(x_n)>y$
for all $n$ from some definite index $N$ onwards. For any $\delta>0$, there exists $n>N$
such that $0<d(p,x_n)<\delta$, since $x_n\rightarrow p$. Evidently, $f(x_n)>y$. $\square$

**THEOREM 2**\
If $\liminf_{x\rightarrow p}f(x)=\limsup_{x\rightarrow p}f(x)=l$, then $f(x)\rightarrow l$
as $x\rightarrow p$.

**PROOF**\
This follows immediately from Theorem 1(a).

**THEOREM 3**\
If $g$ is another mapping of $E$ into $\mathbb{R}^1$, and if there exists $\delta>0$ such
that $0<d(p,x)<\delta$, $x\in E$ imply that

$$\tag{1}f(x)\leq g(x)\mbox{,}$$

then

$$\tag{2}\liminf f(x)\leq\liminf g(x)\mbox{,}$$

$$\tag{3}\limsup f(x)\leq\limsup g(x)\mbox{,}$$

as $x\rightarrow p$.

**PROOF**\
We show (3). If $\limsup f(x)>y>\limsup g(x)$, then, by Theorem 1, there exist $\delta>\delta'>0$
such that

$$\tag{4}g(x)<y\quad(x\in E,0<d(x,p)<\delta')\mbox{;}$$

also, there exists $\xi\in E$ with $0<d(\xi,p)<\delta'$ such that

$$\tag{5}f(\xi)>y\mbox{.}$$

(4) and (5) contradict (1).