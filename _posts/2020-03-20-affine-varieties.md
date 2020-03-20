---
layout: post
title: "OPPD - Day 2: Affine varieties"
categories: 
- Algebraic Geometry
tag: 
- varieties
- OPPD
---

Today is 20/03/2020 and I decided to learn some basics about 
affine varieties, following [Gathmann's note](https://www.mathematik.uni-kl.de/~gathmann/class/alggeom-2019/alggeom-2019.pdf). The current goal is learn enough 
algebraic geometry to learn about (linear) algebraic groups. 

## Affine varieties

By *affine $n$-space* over field $K$, we mean simply
the vector space $K^n$, which is usually denoted as 
$\mathbb{A}_K^n$ or just $\mathbb{A}^n$ (i.e. writing 
this means we ignore the addition and scalar multiplication 
that occur in $K^n$). Given subset $S\subset K[x_1,\ldots, x_n]$
of polynomials we call set of common solutions in $\mathbb{A}^n$ of 
$S$ the (affine) *zero locus* of $S$, denoted as $V(S)=\{x\in 
\mathbb{A}^n: f(x)=0 \; \forall x\in S\}$. 
An *affine variety* $X\subset \mathbb{A}^n$
is the zero locus $V(S)$ of collection 
$S\subset K[x_1,\ldots, x_n]$.