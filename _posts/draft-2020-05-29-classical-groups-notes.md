---
layout: post
title: "Symmetry, Representations and Invariants notes"
categories: 
- Representation Theory
tag: 
---

## Lie algebra of a Lie subgroup $G$ of $\text{GL}(n,\mathbb{C})$
Defined as matrices $X\in M_n(\mathbb{C})$ such that 
$\exp(tX)\in G$ for all $t\ge 0$. This is an 
easy-to-compute definition but it seems it 
is not generalisable for linear algebraic groups
or other Lie groups that are not subgroups of 
$\text{GL}(n,\mathbb{C})$.

Secondly, we view elements of $\mathfrak{g}$
as left-invariant vector fields on $G$

## Linear algebraic groups over $\mathbb{C}$

Subgroup $G$ of $\text{GL}(n,\mathbb{C})$ is 
*linear algebraic group* if there is set 
$\mathcal{A}$ of polynomial functions on 
$M_n(\mathbb{C})$ such that $f(g)=0$ 
for all $f\in \mathcal{A}, g\in G$. 
Here polynomial functions mean is is polynomials 
of matrix entry functions $x_{i,j}$ on $M_n(\mathbb{C}$.
On then can define linear algebraic group as subgroup 
$G\subset \text{GL}(V)$ for some finite-dimensional complex
vector space via the isomorphism
$\text{GL}(V)\to\text{GL}(n,\mathbb{C})$.

There are two ways to define *regular functions* on 
$\text{GL}(V)$ to $\mathbb{C}$:
- The algebra $\mathcal{O}[\text{GL}(n,\mathbb{C})]$ 
of regular functions on 
$\text{GL}(n,\mathbb{C})$ as $\mathbb{C}[x_{i,j},\det(x)^{-1}]$. One then can define regular functions for $\text{GL}(V)$.
- For $B\in \text{End}(V)$, define $f_B\in \text{End}(V)$
by $f_B(Y)=\text{tr}_V(YB), Y\in \text{End}(V)$.
Then $\mathcal{O}[\text{GL}(V)]$ is generated
by $\{f_B:B\in \text{End}(V)\}$ and $(\det)^{-1}$. 

The second definition is a basis-free definition. 
When $V=\mathbb{C}^n, \text{End}(V)=M_n(\mathbb{C})$
and $B=e_{i,j}$ then $f_{e_{i,j}}(Y)=x_{i,j}(Y)$
so we obtain the first definition from the second 
one. 

For $G\subset \text{GL}(V)$ then regular functions 
on $G$ is restriction of regular functions on 
$\text{GL}(V)$. In particular, $\mathcal{O}[G]$
is quotient of $\mathcal{O}[\text{GL}(V)]$ by 
some ideal.

For linear algebraic groups $G,H$ then 
map $\varphi:G\to H$ is *regular map* when 
it induces algebra map
$\varphi^*: \mathcal{O}[G]\to \mathcal{O}[H]$.

For algebraic groups $G\subset \text{GL}(m,\mathbb{C})$
and $H\subset \text{GL}(n,\mathbb{C})$ then the 
direct product $K=G\times H$ is also algebraic 
group by block diagonal embedding 
$K\subset \text{GL}(m+n,\mathbb{C})$. Also, 
$\mathcal{O}[G]\otimes \mathcal{O}[H] \cong \mathcal{O}[K]$
via algebra homomorphism $f\otimes f' \mapsto ((g,h)\mapsto f(g)f'(h))$. 

We can show that multiplication $G\times G\to G$, inversion 
$G\to G$, left-multiplication $L_g:G\to G$,
right-multiplication $R_g:G\to G$ are regular maps.

## Lie algebra of an Algebraic Group 

See \S 1.4.3. Lie algebra of $G$ is derivations 
of $\mathcal{O}[G]$ that commutes with left-translation.

TODO

## Rational representations

A representation $\rho:G\to \text{GL}(V)$ is *regular* 
if $\text{dim }(V) <\infty$ and the functions on 
$G$: $g\mapsto \langle v^*, \rho(g)v\rangle$, 
which we called *matrix coefficients* of 
$\rho$, are regular for all $v\in V$ and 
$v^*\in V^*$. In particular, if we fix a basis 
for $V$ and then write $\rho(g)\in \text{GL}(V)$
as $\rho(g)=(\rho_{i,j}(g))_{1\le i,j\le n}$
then $\rho_{i,j}$ are regular functions on $G$.
Also, as $\det(\rho(g))^{-1}=\det \rho(g^{-1})$
so $\rho$ is a regular homomorphism from $G$ to 
$\text{GL}(V)$. Regular representation is often called 
*rational* representation because each $\rho_{i,j}(g)$
is a rational function of matrix entries of $g$
with denominator as powers of $\det g$. 

The definition of regularity can be phrased as follows:
On $\text{End}(V)$, we have symmetric bilinear form 
$A,B\mapsto \text{tr}_V(AB)$. This form is nondegenerate,
so if $\lambda\in \text{End}(V)^*$, there exists 
$A_{\lambda}\in \text{End}(V)$ such that 
$\lambda(X)=\text{tr}_V(A_{\lambda}X)$. For 
$B\in \text{End}(V)$, define function $f_B^{\rho}$
on $G$ by $f_B^{\rho}(g)=\text{tr}_V(\rho(g)B)$. 
When $B$ has rank $1$, we obtain the matrix-coefficient-formulation in previous definition. 
Then $(\rho,V)$ is regular iff $f_B^{\rho}$ regular 
functions on $G$, for all $B\in \text{End}(V)$. We set 

$$
E^{\rho}=\{f_B^{\rho}:B\in \text{End}(V)\}.
$$

This is the linear subspace of $\mathcal{O}[G]$
spanned by the functions in the matrix for $\rho$. 
It is finite-dimensional and invariant under 
left and right-translations by $G$. We call it space 
of *representative functions* associated with $\rho$. 

Supopse $\rho$ representation of $G$ on infinite-dim 
vector space $V$. We say $\rho$ is *locally regular* 
if every finite-dimensional subspace $E\subset V$
is contained in finite-dimensional $G$-invariant 
subspace $F$ such that the restriction of $\rho$
to $F$ is a regular representation. 

Representations $L,R$ of $G$ on infinite-dimensional 
vector space $\mathcal{O}[G]$ given by *left* and 
*right translations*:

$$L(x)f(y) =f(x^{-1}y), R(x)f(y)=f(yx), f\in \mathcal{O}[G]$$
Then $(L, \mathcal{O}[G])$ and $(R,\mathcal{O}[G])$
are locally regular. 
There are also locally regular representation on $G\times G$
and conjugacy representation. ...

## Differential of a Rational representation

For now, just to know that given rational representation 
$(\pi,V)$ of $G\subset \text{GL}(n,\mathbb{C})$. One 
can obtain a complex Lie algebra hom 
$d\pi: \mathfrak{g} \to \mathfrak{gl}(V)$.

## Adjoint representation 

For $G\subset \text{GL}(n,\mathbb{C})$ be algebraic 
group with Lie algebra $\mathfrak{g}$. The representation 
of $\text{GL}(n,\mathbb{C})$ by similarity $A\mapsto gAg^{-1}$
is regular. We can show that restriction of this 
representation to $G$ is a regular representation of $G$.

To show that, note that for $A\in \mathfrak{g}$ and $g\in G$
then $gAg^{-1}\in \mathfrak{g}$. If we then define 
$\text{Ad}(g)=gAg^{-1}$ for $g\in G, A\in \mathfrak{g}$
then we can show $\text{Ad}(g):\mathfrak{g}\to\mathfrak{g}$ so 
$\text{Ad}:G\to \text{End}(\mathfrak{g})$ is the 
*adjoint representation* of $G$. Furthermore, $\text{Ad}(g):\mathfrak{g}\to\mathfrak{g}$ is Lie algebra automorphism 
and $\text{Ad}$ is group automorphism. 

The differiential of the adjoint representation 
is the representation $\mathfrak{g}\to\text{End}(\mathfrak{g})$
given by $\text{ad}(A)(B)=[A,B]$ for $A,B\in \mathfrak{g}$.

# Structure of Classical Groups

## Semisimple elements

