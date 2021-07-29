---
layout: page
title: "Baby Rudin Exercise 4.15"
author: "Felix Chen"
categories: journal
tags: [documentation,real analysis]
---

> Call a mapping of $X$ into $Y$ open if $f(V)$ is an open set in $Y$ whenever
> $V$ is an open set in $X$. \
> Prove that every continuous open mapping of $\mathbb{R}^1$ into $\mathbb{R}^1$
> is monotonic.

**PROOF** Suppose $f$ is a continuous open mapping of $\mathbb{R}^1$ into $\mathbb{R}^1$
that is not monotonic. Observe that for any real numbers $a$, $b$ and $c$,

$$ a \leq b \leq c \mbox{,} $$

$$ c \leq b \leq a \mbox{,} $$

$$ a \leq c < b \mbox{,} $$

$$ c \leq a < b \mbox{,} $$

$$ b < a \leq c \mbox{,} $$

or

$$ b < c \leq a \mbox{.} $$
	
Hence we can find $a,b,c$ with $a<b<c$ such that

$$\tag{$\dagger$} f(a)>f(b) \mbox{, } f(c)>f(b)$$

or

$$ f(a)<f(b) \mbox{, } f(c)<f(b) \mbox{.} $$

For brevity, assume ($\dagger$) holds. By continuity, there exist $p,q$ such that

$$ f(x) > f(b) $$

if $a<x<p$ or $q<x<b$. Also, by continuity, $f$ attains its minimum on $[p,q]$ at
some point $t\in[p,q]$. Evidently, $f(t)$ is the minimum of $f$ on $(a,b)$, hence
$f(t)$ cannot be an interior point of $f(a,b)$, which is absurd.
