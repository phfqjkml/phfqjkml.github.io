---
layout: page
title: "Friedman Problems 1.6.3, 1.6.4"
author: Felix Chen
categories: journal
tags: [documentation,real analysis]
---

> 1.6.3. The outer Lebesgue measure of a closed bounded interval $[a,b]$ on the real line is equal to $b-a$.

**Lemma 1** If $[\alpha,\beta]\subset(a,b)$, then $\lambda(a,b)>\beta-\alpha$.

**Proof** Since $a<\alpha<\beta<b$, $\lambda(a,b)=b-a>\beta-\alpha$. $\blacksquare$

**Lemma 2** If $[a,b]\subset\bigcup^m_{n=1}(a_n,b_n)$, then there exists a partition $P=\\{x_0,x_1,...,x_p\\}$ of $[a,b]$ such that for each $i$,

$$\tag{1}[x_{i-1},x_i]\subset(a_j,b_j)$$

for some $j$.

**Proof** The proof is by induction on $m$. The case $m=1$ is trivial. Suppose, for some $m'\geq1$, the claim is valid when $m=m'$, and suppose that $m=m'+1$.

Choose $n_1$ so that $a\in(a_{n_1},b_{n_1})$. If $b_{n_1}>b$, then clearly $P=\\{a,b\\}$ is the partition we seek. If, on other hand, $b_{n_1}\leq b$, then we choose $n_2$ so that $b_{n_1}\in(a_{n_2},b_{n_2})$. By the openness of $(a_{n_2},b_{n_2})$, $[a',b_{n_1}]\subset(a_{n_2},b_{n_2})$ for some $b_{n_1}>a'>a$. Evidently,

$$[a,a']\subset(a_{n_1},b_{n_1}),\qquad[a',b]\subset\bigcup_{1\leq n\leq m;n\not=n_1}(a_n,b_n)\mbox{.}$$

By the inductive hypothesis, there exists a parition $P'$ of $[a',b]$ such that each subinterval of $P'$ satisfies (1). $P=\\{a,a'\\}\cup P'$ is the parition of $[a,b]$ we seek. This completes the induction. $\blacksquare$.

**Proof of 1.6.3.** Let $\\{I_n\\}$ be an open cover for $[a,b]$. By the compactness of $[a,b]$, there are finitely many indices $n_1,...,n_p$ such that

$$[a,b]\subset I_{n_1}\cup\cdots\cup I_{n_p}\mbox{.}$$

By the lemmata,

$$\sum_{n=1}^\infty\lambda(I_n)\geq\lambda(I_{n_1})+\cdots+\lambda(I_{n_p})>b-a\mbox{.}$$

Hence $\mu^*[a,b]\geq b-a$.

Let $\epsilon>0$. $[a,b]\subset(a-\epsilon,b+\epsilon)$, so that

$$\mu^*[a,b]\leq b-a+2\epsilon\mbox{.}$$

Since $\epsilon$ is arbitrary,

$$\mu^*[a,b]\leq b-a\mbox{.}$$

Therefore, $\mu^*[a,b]=b-a$. $\blacksquare$

> 1.6.4. The outer Lebesgue measure of each of the intervals $(a,b)$, $[a,b)$, $(a,b]$ is equal to $b-a$.

**Proof** Let $\epsilon>0$ be sufficiently small. Since

$$[a+\epsilon,b-\epsilon]\subset(a,b)\subset[a,b]\mbox{,}$$

by the monotonicity of $\mu^*$,

$$b-a-2\epsilon\leq\mu^*(a,b)\leq b-a\mbox{.}$$

Since $\epsilon$ is arbitrary,

$$\mu^*(a,b)=b-a\mbox{.}$$

Again by the monotonicity of $\mu^*$, 

$$\mu^*[a,b)=\mu^*[a,b)=b-a\mbox{. }$$

$\tag*{$\blacksquare$}$

