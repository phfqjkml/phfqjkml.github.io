---
layout: page
title: "Baby Rudin Exercise 7.12"
author: "Felix Chen"
categories: journal
tags: [documentation,real analysis]
---

> Suppose $g$ and $f_n$ ($n=1,2,3,...$) are defined on $(0,\infty)$, are Riemann-
> integrable on $[t,T]$ whenever $0<t<T<\infty$, $\left|f_n\right|\leq g$,
> $f_n\rightarrow f$ uniformly on every compact subset of $(0,\infty)$, and
>
> $$\int^\infty_0 g(x)\,dx<\infty\mbox{.}$$
>
> Prove that
>
> $$\lim\limits_{n\rightarrow\infty}\int^\infty_0 f_n(x)\,dx=\int^\infty_0f(x)\,dx\mbox{.}$$

**PROOF** Since $f_n\rightarrow f$ uniformly and $f_n\in\mathscr{R}$ on $[t,T]$,
$f\in\mathscr{R}$ on $[t,T]$ for any $0<t<T<\infty$.\
Since $\left|f_n\right|\leq g$, $\left|f\right|\leq g$.\
Given $\epsilon>0$. By the Cauchy criterion, there exist real numbers $m,M$ with $m<M$ such
that

$$\tag{$\dagger$}\left|\int^q_p\phi\right|\leq\int^q_pg<\epsilon$$

if $q\geq p\geq M$, or if $p\leq q\leq m$, where $\phi=f$ or $\phi=f_n$ for some $n$;
hence $\int^\infty_0\phi$ converges for $\phi=f$ or $f_n$. Observe that ($\dagger)$ also
implies that

$$\left|\int^\infty_M\phi\right|\leq\epsilon\mbox{.}$$

Fix a number $t$ between $m$ and $M$ and then choose an integer $N$ such that

$$\left|\int^M_t(f_n-f)\right|<\epsilon$$

provided that $n>N$.

It follows that for $n>N$,

$$\begin{aligned}
\left|\int^\infty_t f_n-\int^\infty_t f\right|&\leq\left|\int^\infty_t f_n-\int^M_t f_n\right|+\left|\int^M_t f_n-\int^M_t f\right|+\left|\int^M_t f-\int^\infty_t f\right|\\
&<3\epsilon\mbox{;}\end{aligned}$$

thus

$$\int^\infty_t f_n\rightarrow\int^\infty_t f\mbox{.}$$

Similarly,

$$\int^t_0 f_n\rightarrow\int^t_0 f\mbox{.}$$

Consequently

$$\int^\infty_0 f_n\rightarrow\int^\infty_0 f\mbox{.}$$


