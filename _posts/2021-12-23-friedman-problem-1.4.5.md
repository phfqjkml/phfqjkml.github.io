---
layout: page
title: "Friedman Problem 1.4.5"
author: Felix Chen
categories: journal
tags: [documentation,real analysis]
---

> 1.4.5. If $\mathscr{K}$ is a $\sigma$-algebra and $\lambda$ is a measure
> on $\mathscr{K}$, then every set in $\mathscr{K}$ is $\mu^*$-measurable.

Let $E\in\mathscr{K}$ and $A$ be a set. Given $\epsilon>0$. There exists
$\{E_n\}\in\mathscr{K}$ such that

$$A\subset\bigcup E_n\mbox{,}$$

$$\tag{1}\mu^*(A)+\epsilon>\sum\lambda(E_n)\mbox{.}$$

Put $G=E\cap\bigcup E_n$. Since $\mathscr{K}$ is a $\sigma$-algebra,
$G\in\mathscr{K}$. Observe that

$$\tag{2}A\cap E\subset G\mbox{,}$$

$$\tag{3}A\setminus E\subset\bigcup E_n\setminus E=\bigcup E_n\setminus G\mbox{.}$$

By (1), (2), and (3), since $\lambda$ is a measure and $\sum\lambda(E_n)<\infty$,

$$\mu^*(A)+\epsilon>\lambda(G)+\left(\sum\lambda(E_n)-\lambda(G)\right)\geq\mu^*(A\cap E)+\mu^*(A\setminus E)\mbox{.}$$

Since $\epsilon$ is arbitrary, we obtain, for any set $A$,

$$\mu^*(A)\geq\mu^*(A\cap E)+\mu^*(A\setminus E)\mbox{,}$$

from which we conclude that $E$ is measurable.
