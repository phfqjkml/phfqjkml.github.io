---
layout: page
title: "Baby rudin remark 4.31"
author: "Felix Chen"
categories: journal
tags: [documentation,real analysis]
---

> Given a countable subset $E$ of $(a,b)$. Let the points of $E$ be arranged in a
> sequence $\\{x_n\\}$, $n=1,2,3,...$. Let $\\{c_n\\}$ be a sequence of positive
> numbers such that $\sum c_n$ converges. Define
>
> $$ \tag{$\dagger$} f(x) = \sum_{x_n<x} c_n \qquad (a<x<b)\mbox{.} $$
>
> The summation is to be understood as follows: Sum over those indices $n$ for which
> $x_n<x$. If there are points $x_n$ to the left of $x$, we define it to be zero.
> Since ($\dagger$) converges absolutely, the order in which the terms are arranged
> is immaterial.\
> We leave the verification of the following properties of $f$ to the
> reader:\
> (a) $f$ is monotonically increasing on $(a,b)$;\
> (b) $f$ is discontinuous at every point of $E$; in fact,
>
> $$ f(x_n+)-f(x_n-)=c_n\mbox{.} $$
>
> (c) $f$ is continous at every other point of $(a,b)$.

**PROOF** For $x<y$,

$$ f(y)-f(x) = \sum_{x\leq x_n<y} c_n \geq 0 \mbox{,} $$

and (a) is thus established. \
Fix $x\in(a,b)$. Let $\Lambda$ be the set of all indices $n$ for which $x_n<x$.
If $\Lambda$ is finite, then plainly $f(x-)=f(x)$. Otherwise, we arranges $\Lambda$
in a sequence $\{\alpha_n\}$ and choose arbitrarily $\epsilon>0$. By definition,

$$ \left| f(x) - \sum_{i=1}^n c_{\alpha_i} \right| < \epsilon \mbox{,} $$

for all $n$ from some definite index $N$ onward. Hence, if $x>\xi>x\_{\alpha_i}$,
$i=1,...,N$,

$$ f(x)-\epsilon < f(\xi) \leq f(x) \mbox{.} $$

This means $f(x-)=f(x)$. Next, we show that

$$ f(x+) = \left\{ \begin{array}{ll}
						f(x) & \mbox{if }x\not\in E \\
						f(x) + c_m & \mbox{if }x = x_m
\end{array} \right. \mbox{.} $$

Since, for $\xi>x$,

$$ f(\xi)-f(x) = \left\{ \begin{array}{ll}
					\sum_{x<x_n<\xi} c_n & \mbox{if }x\not\in E \\
					\sum_{x<x_n<\xi} c_n + c_m & \mbox{if }x = x_m \\
\end{array} \right. \mbox{,} $$

it suffices to show that

$$ \tag{$\star$} \sum_{x<x_n<\xi} c_n $$

can be made arbitrarily if only
$\xi$ is close enough to $x$. By Cauchy criterion, there exists $M$ such that

$$ \sum_n^\infty c_n < \epsilon $$

provided that $n\geq M$; whence, if we pick a $\delta>0$ such that $x_n\not\in(x,x+\delta)$
for $n=1,2,...,M$, then for each $x<\xi<x+\delta$, $(\star)$ holds. $\tag*{$\blacksquare$}$