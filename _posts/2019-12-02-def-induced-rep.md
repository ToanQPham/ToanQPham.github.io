---
layout: post
title: "Definition of induced representation"
categories: 
- Representation Theory
tag: 
- induced representation
- draft
---

My unfinished notes for some ways to define induced
representation. My main goal here is to motivate such 
definitions. This is unfinished project 
with some unanswered questions. I will
update this when I have time and motivation to do so. 

First, we define restricted representation: Given 
a finite-dimensional representation $V$ of a 
finite group $G$ and a subgroup 
$H\subset G$, there is a *natural* way to construct 
a representation of $H$. The **restriction** of $V$
to $H$, $\text{Res}_H^GV$ is the representation 
given by the vector space $V$, and the action 
$\rho_{\text{Res}_H^GV}=\rho_{V|H}$. This 
is indeed a representation since the map 
$H \hookrightarrow G \rightarrow \text{GL}(V)$ is
a group homomorphism. 

One may ask whether there is a *natural* way to construct 
representation $V$ of $G$ knowing a representation $W$ of 
subgroup $H$ of $G$. $V$ is then denoted as 
$\text{Ind}_H^GW$

# First explanation

I learn this from answer on 
[MathStackExchange](https://math.stackexchange.com/a/266687/58951). This explanation is good since it assumes no
other knowledge. 

First question is how to describe 
$V$ in terms of $W$. Like how one generates free group
from a set or polynomial ring $R[x]$ from ring $R$
by concatenation, one would guess that $V$ is 
the vector space $\bigoplus_{s\in G}sW$ where $sW$
contains every symbol $sw$ for $v\in W$. However, 
note that we want to construct $V$ *from* representation 
$W$ of $H$ so it is natural to let $sW=tW$ if 
$s,t$ from the same left coset of $H$ (i.e. 
$s=ah,t=ah'$ so setting $sW=tW$ makes sense as 
$hW=h'W$). This suggests $V=\bigoplus_{s\in G/H}sW$.
The second question is how does $G$ acts on this $V$. 
Natually, it should be $s(tw)=(st)w$ for $s,t\in G$. 

## Spell this out

Follow the [wikipedia](https://en.wikipedia.org/wiki/Induced_representation#Algebraic), 
let $g_1,\ldots, g_n$ be the representatives in $G$
of the left cosets in $G/H$ and so
$V=\bigoplus_{i=1}^n g_iW$. For each $g\in G$,
there exists permutation $j$ of $[n]=\{1,\ldots, n\}$
so that $gg_i=g_{j(i)}h_i$ for some $h_i\in H$.
Hence, $g$ acts on $V$ as follow

$$g \sum_{i=1}^n g_iv_i= \sum_{i=1}^n g_{j(i)}(h_iv_i)$$

# Universal property

Universal property is a way to explain naturality
of objects. I learn this idea from the book Algebra:
Chapter 0 by Paulo Aluffi. This is another way
to phrase the first explanation while keeping 
it universal, i.e. this method can be mimicked 
to define other objects (in fact, free groups
can be also motivated this way).

Given representation $(\theta,W)$ of $H$. Consider 
category $\mathcal{C}$ whose objects are pairs 
$((\rho,V),f)$ where $(\rho,V)$ a representation
of $V$ and $f:W\to V$ a linear map satisfying 
$f(\theta(h)w)=\rho(h)f(w)$ for $h\in H$. 

A morphism $(V_1,f_1) \to (V_2,f_2)$ is a linear 
map $\varphi:V_1\to V_2$ such that the following 
diagram commutes

$$\xymatrix{ y \ar[r]_ g \ar[d]_ f &  z \ar[d]^ q \\  x \ar[r]^ p &  x\amalg _ y z }$$