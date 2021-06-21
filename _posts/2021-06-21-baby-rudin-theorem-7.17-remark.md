---
layout: page
title: "Baby Rudin Theorem 7.17 Remark"
author: "Felix Chen"
categories: journal
tags: [documentation,real analysis]
---

> Suppose $\\{f_n\\}$ is a sequence of functions, continuously differentiable on
> $[a,b]$ and such that $\\{f_n(x_0)\\}$ converges for some point $x_0$ on $[a,b]$.
> If $\\{f_n'\\}$ converges uniformly on $[a,b]$, then $\\{f_n\\}$ converges uniformly
> on $[a,b]$, to a function $f$, and
> 
> $$ \tag{$\star$} f'(x) = \lim\limits_{n\rightarrow\infty} f_n'(x) \qquad
> (a\leq x\leq b)\mbox{.} $$

**PROOF** Given $\epsilon>0$. Choose $N$ such that $n\geq N$, $m\geq N$ impliy

$$ \left| f_n(x_0)-f_m(x_0) \right| < \frac{\epsilon}{2} $$

and

$$ \left| f_n'(t)-f_m'(t) \right| < \frac{\epsilon}{2(b-a)} \qquad
(a\leq t\leq b)\mbox{.} $$

By continuity of the functions $f_n'$, they are integrable. Hence

$$ \begin{aligned}
\left| 	f_n(x)-f_m(x) \right|
&= \left| f_n(x)-f_n(x_0)+f_n(x_0)-f_m(x_0)+f_m(x_0)-f_m(x) \right|\\
&\leq \left| \int^x_{x_0} f_n'(t)-f_m'(t)\, dt \right| + \left|f_n(x_0)-f_m(x_0)\right|\\
&< \epsilon\mbox{,}
\end{aligned} $$

for any $a\leq x\leq b$, $n\geq N$, and $m\geq N$, so that $\\{f_n\\}$ converges uniformly.
Suppose $f_n'\rightarrow \phi$ uniformly, then $\phi$ is continuous. By theorem,

$$ \lim\limits_{n\rightarrow\infty}\int^x_a f_n'(x) = \int^x_a \phi(t)\, dt $$

or, equivalently,

$$ f(x)-f(a) = \int^x_a \phi(t)\, dt \mbox{;}$$

thus, by differentiating both sides of the above equation, we obtain ($\star$). Note that
$f(x)$ is a sum of a contant and a integral of a continuous function, hence it is
differentiable.