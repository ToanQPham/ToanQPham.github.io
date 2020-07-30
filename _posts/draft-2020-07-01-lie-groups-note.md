---
layout: post
title: "Lie Groups Varadarajan"
categories: 
- Representation Theory
- Lie Groups
tag: 
- Manifolds
---

Here are some notes/questions I have 
when reading the book Lie Groups by 
Varadarajan.

# Questions/Notes

## Page 13

### 07/01/2020 

Q1: I couldn't seem to 
explain the equation obtained by partial 
integration. To me it seems to be missing
some extra term? 

Q2: (Abuse of notation?) 
The integral on this page should be 
over $U$ instead of over $M$? Because 
$f,g$ seem to have domain $U$ not $M$?

Answer: Not necessarily. 
$f\in C_c^{\infty}(U)$ means 
support of $f$ is compact and lies in 
$U$. By partition of unity (page 2, (i)),
there exists $\varphi\in C^{\infty}(M)$ such 
that $\varphi=1$ in open set $U$ 
and $0$ elsewhere. Then 
$\int_M (Df)(x) g(x) d\mu$ should really mean 
$\int_M \varphi(x) (Df)(x)g(x)d\mu$
(here the function $\varphi \cdot Df\cdot g$
is smooth and is $0$ outside $U$, is 
$Df\cdot g$ inside $U$)
which is just $\int_U (Df)g d\mu$.

Q3: So we know 
$\int_M (Df)gd\mu=\int_M f(D'g)\mu$
for all $f,g\in C^{\infty}_c(U)$.
How to extend this to any 
$f,g\in C^{\infty}_c(M)$? 

Answer: Pick an open cover $\{U_{\alpha}\}_{\alpha\in A}$, 
there exists partition of unity 
$\{\varphi_{\alpha}:C^{\infty}\to M\}$
having compact support in $U_{\alpha}$.
This follows 
$f=\sum \varphi_{\alpha}f|_{U_{\alpha}}$
and $g=\sum\varphi_{\alpha}g|_{U_{\alpha}}$.
Then $\int_M (Df)g\mu$ is just sum 
of integrals over $U_{\alpha}$:

$$\int_M (Df)gd\mu=\sum_{\alpha,\beta} \int_{U_{\alpha\cap}U_{\beta}} D(\varphi_{\alpha}f|_{U_{\alpha}})\varphi_{\beta}g|_{U_{\beta}}d\mu=\sum_{\alpha,\beta} \int_{U_{\alpha}\cap U_{\beta}} \varphi_{\alpha}f|_{U_{\alpha}}D(\varphi_{\beta}g|_{U_{\beta}})d\mu=\int_M f(Dg)\mu$$

(This is how integration is defined on manifolds with more than one coordinate charts I believe).

## Page 7: Differential operators

### 07/01/2020

Q1: Verify some claims made here. 

# Typos

* Page 7: (b) If 
$V_{i_1}\cap V_{i_2}\ne \emptyset$. 
