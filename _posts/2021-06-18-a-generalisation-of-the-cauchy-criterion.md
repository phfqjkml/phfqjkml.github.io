---
layout: page
title: "A generalisation of the Cauchy criterion"
author: "Felix Chen"
categories: journal
tags: [documentation,real analysis]
---

In this post, we shall prove a criterion for determining whether a function has a limit
at a limit points of its domain.

**THEOREM** _Suppose $(X, d)$ is a metric space, $E$ a subset of $X$, $(Y,d')$
a complete metric space, $\xi$ a limit point of $E$, and $f$ a mapping of $E$ into
$Y$. Then $f$ possesses a limit at $\xi$ if and only if for any $\epsilon>0$ there
exists $\delta>0$ such that_

$$ \tag{*} d'(f(x),f(y))<\epsilon $$

_provided that $x,y\in E$, $d(x,\xi)<\delta$, and $d(y,\xi)<\delta$._

The following definition is sometimes useful.\
**DEFINITION** _Sequences $\\{x_n\\}, \\{y_n\\}$ in a metric space $(X,d)$ are
said to be equivalent if $d(x_n,y_n)$ can be made arbitrarily small provided
only that $n$ is large enough._\
One can see at once that two sequences converge to the same point if and only
if they are equivalent.

**PROOF** Suppose $\lim\limits\_{x\rightarrow\xi}f(x)=\eta$ for some $\eta\in Y$.
Then for any $\epsilon>0$, there exists $\delta>0$ such that $d'(f(x),\eta)<
\frac{\epsilon}{2}$ whenever $d(x,\xi)<\delta$. From this it follows that if
$d(x,\xi)<\delta$ and $d(y,\xi)<\delta$ then

$$ d'(f(x),f(y))\leq d'(f(x),\eta)+d'(\eta,f(y))<\epsilon\mbox{.}
\mbox{,} $$

which proves (\*). \
Conversely, suppose (\*) holds. Let $x_n\rightarrow\xi$. By (\*), $\\{f(x_n)\\}$ is a 
Cauchy sequence, whence $f(x_n)\rightarrow\eta$ for some $\eta\in Y$. Now let
$y_n\rightarrow\xi$ be arbitrary. Again, by (\*), $\\{f(x_n)\\}$ and $\\{f(y_n)\\}$
are equivalent, therefore, $f(y_n)\rightarrow\eta$. Since $\\{y_n\\}$ was arbitrary,
$\lim\limits_{x\rightarrow\xi}f(x)=\eta$ as was to be proved.

Observe that the theorem is still valid if $X=\mathbb{R}$, $\xi=-\infty$ or $+\infty$.
Consequently, it is indeed a generalisation of the Cauchy criterion.

We show that $\int_0^\infty \frac{\sin x}{x}\, dx$ converges by the this criterion.

$$ \begin{aligned}
\left|\int_p^q \frac{\sin x}{x}\, dx\right|
&= \left|\left.\frac{-\cos x}{x}\right|_p^q - \int_p^q \frac{\cos x}{x^2}\, dx\right| \\
&\leq \left|\frac{\cos q}{q}\right| + \left|\frac{\cos p}{p}\right| + \int_p^q\left|\frac{\cos x}{x^2}\right|\, dx \\
&\leq \frac{1}{q} + \frac{1}{p} + \int_p^q \frac{1}{x^2} \\
&= \frac{1}{q} + \frac{1}{p} + \frac{1}{p} - \frac{1}{q} \\
&= \frac{2}{p} \rightarrow 0 \mbox{,}
\end{aligned} $$

as $p\rightarrow+\infty$.
