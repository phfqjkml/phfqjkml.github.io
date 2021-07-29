---
layout: page
title: "Limit Superior of Real-valued Functions"
author:
categories: journal
tags: [documentation,real analysis]
---

**DEFINITION**\
Suppose $X$ is a metric space, $E\subset X$, $f$ maps
$E$ into $\mathbb{R}^1$, and $p\in E$. For any $\delta>0$, let $V(\delta)$ denote
the set of $f(x)$ for all $x\in E$ for which $0<d(p,x)<\delta$. Define

$$ \limsup\limits_{x\rightarrow p} f(x)=\lim\limits_{\delta\rightarrow0}\sup V(\delta)\mbox{.}$$

Observe that the limit is a number in the extended real number system and equals

$$ \inf\sup V(\delta) $$

where the inf is taken over all $\delta>0$.

**THEOREM** \
Put

$$L=\limsup\limits_{x\rightarrow p} f(x)\mbox{.}$$

(a) If $s>L$, then there exists $\delta>0$ such that $f(x)<s$ for all $x\in E$ for
which $0<d(p,x)<\delta$. \
(b) If $t<L$, then for any $\delta>0$ there exists some $x\in E$ such that $0<d(p,x)<\delta$
and $f(x)>t$.

**PROOF** If $s>L$, then, by definition, $\sup V(\delta)<s$ for some $\delta>0$, hence
$f(x)\leq \sup V(\delta)<s$ for all $x$ with $0<d(p,x)<\delta$. This proves (a). \
If $t<L$, then, by definition, there exists $\omega>0$ such that $\sup V(\delta_1)>t$
whenever $0<\delta_1<\omega$. By definition of sup, if $0<\delta_1<\omega$, there
exists $x$ with $d(p,x)<\delta_1$ such that $f(x)>t$, which proves (b).

**THEOREM** \
Suppose $g$ is another real-valued function defined on $E$, and

$$ f(x) \leq g(x) $$

for all $x$ in some neighborhood of $p$. Then

$$ \limsup f(x)\leq \lim\sup g(x) $$

as $x\rightarrow p$.

**PROOF** If $\limsup f(x)>\limsup g(x)$, choose a number $q$ between them. By the theorem
we just proved, $f(x)>q>g(x)$ for some $x$ close enough to $p$, which contradicts the
hypothesis.