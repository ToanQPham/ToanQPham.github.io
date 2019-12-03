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
to $H$, $\text{Res}\_{H}$
is the representation 
given by the vector space $V$, and the action 
$\rho_{\text{Res}\_H^G V}=\rho_{V|H}$. This 
is indeed a representation since the map 
$H \hookrightarrow G \rightarrow \text{GL}(V)$ is
a group homomorphism. 

One may ask whether there is a *natural* way to construct 
representation $V$ of $G$ knowing a representation $W$ of 
subgroup $H$ of $G$. $V$ is then denoted as 
$\text{Ind}\_H^G W$.

# First explanation

I learn this from answer on 
[MathStackExchange](https://math.stackexchange.com/a/266687/58951). 
This explanation is good since it assumes no
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

A morphism $(V_1,f_1) \to (V_2,f_2)$ is a 
$G$-module homomorphism $\varphi:V_1\to V_2$ 
such that the following diagram commutes

(OK NEED TO FIGURE HOW TO DRAW DIAGRAM)

$$
\xymatrix {
U \ar@/_/[ddr]_y \ar@{.>}[dr]|{\langle x,y \rangle} \ar@/^/[drr]^x \\
 & X \times_Z Y \ar[d]^q \ar[r]_p & X \ar[d]_f \\
 & Y \ar[r]^g & Z
}
$$



The induced representation 
$((\rho, \text{Ind}\_H^G W),j)$
with $j:W\to \text{Ind}\_H^G W$
is an *initial object* in this category:
it is an object such that 
for all representation $V$ of $G$ and 
$G$-module homomorphism $f:W\to V$, 
there exists a *unique* $G$-module
homomorphism $\varphi:\text{Ind}\_H^G W \to V$
such that the diagram 

(DIAGRAM)

commutes. This universal property defines
$\text{Ind}\_H^G W$ up to isomorphism, 
if it exists. In fact, one can check 
with the induced representation defined
in the first explanation that it safisties
the above universal property. 

## Short explanation

Left-induced representations as left-adjoint
to restricted representation. 

TODO.

See more at [nLab](https://ncatlab.org/nlab/show/induced+representation). 

# Module perspective

**Quick explanation.**
In fact $\text{Ind}_H^G W$ can be viewed as 
$k[G] \otimes_{k[H]} W$ where 
this is a left $k[G]$-module with $g$ acts on
$g'\otimes w$ as $gg'\otimes w$. Also, 
$gh\otimes w$ and $g\otimes (hw)$ are considered
the same for $h\in H$. 

**Detailed explanation.**
Here we need to know about tensor product
of modules over noncommutative ring. 
For this, see exercise 5.10.2 in Etingof's
Representation theory book, or 
this [blogspot](https://mathstrek.blog/2015/01/31/tensor-product-over-noncommutative-rings/).

TODO. 

# Different definition

TODO.

The induced representation $\text{Ind}_H^G W$
is the representation of $G$ with

$$\text{Ind}_H^GW=\{f:G\to W|f(hx)=hf(x)
\forall x\in G, \in H\}$$

and the action $g(f)(x)=f(xg)$ for all $g\in G$.

---

**TODO.** How does the last two 
definitions relate to the first definition?

**TODO.** Learn more about induced representation,
see [Wikipedia](https://en.wikipedia.org/wiki/Induced_representation).