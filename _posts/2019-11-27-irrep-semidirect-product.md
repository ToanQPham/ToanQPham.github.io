---
layout: post
title: "Irreducible representation of semidirect product by abelian group"
categories: 
- Representation Theory
tag: 
- Group Representation
---

I would like the write down the argument of $\S 8.2$
of Serre's book Linear Representations of Finite Groups. 

Let $A$ and $H$ be two subgroups of finite group $G$, with 
$A$ normal and abelian. $G$ is the semidirect product 
of $H$ by $A$ (i.e. $G=AH$ and $A\cap H=\{1\}$,
or in other words, each element of $G$ can be 
written uniquely as product of $ah$). Irreducible representations 
of $G$ can then 
be constructed from those of certain subgroups of $H$,
as follow:

Since $A$ is abelian, its irreducible characters are 
of degree $1$ (i.e. dimension of the space is $1$) and 
form a group $X=\text{Hom }(A,\mathbf{C}^*)$. The group 
$G$ acts on $X$ by 

$$s_{\chi}(a)=\chi(s^{-1}as), s\in G,\chi\in X, a\in A.$$

Let $(\chi_i)_{i\in X/H}$ be a system of representatives
of for the orbits of $H$ in $X$. For each $i\in X/H$, let
$H_i$ be the subgroup of $H$ consisting of those elements
$h$ such that $h\chi_i=\chi_i$, and let $G_i=A\cdot H_i$
the corresponding subgroup of $G$. Extend the function
$\chi_i$ to $G_i$ by setting 

$$\chi_i(ah)=\chi_i(a) \; \text{for }a\in A,h\in H_i.$$

> Using the fact that $h\chi_i=\chi_i$ for $h\in H_i$,
we see that $\chi_i$ is a character of degree $1$ of $G_i$.

*Proof.* It suffices to show $\chi_i:G_i\to \mathbf{C}^*$
is a group homomorphism. Note since $A$ normal so 
$t^{-1}at\in A$ for all $t\in G,a\in A$. We have for 
$ah,a'h'\in G_i$ then 

$$\begin{aligned}
\chi_i((ah)(a'h')) & = \chi_i(aha'h^{-1}hh'), \\
& = \chi_i (aha'h^{-1}), \\
& = \chi_i(a)\chi_i(ha'h^{-1}), \\
& = \chi_i(a)(h\chi_i)(a'), \\
& = \chi_i(a)\chi_i(a'), \; (h\in H_i) \\
& = \chi_i(ah)\chi_i(a'h').
\end{aligned}$$

---
Now let $\rho$ be an irreducible representation of 
$H_i$. By composing $\rho$ with the canonical
projection $G_i\to H_i$ we obtain an irreducible
representation $\tilde{\rho}$ of $G_i$. Finally, 
by making the tensor product of $\chi_i$ and 
$\tilde{\rho}$ we obtain an irreducible representation 
$\chi_i\otimes \tilde{\rho}$ of $G_i$. Note 
since $\chi_i:G_i\to \mathbf{C}^{\times}$ so one can view 
$\chi_i\otimes \tilde{\rho}$ as 
$g \mapsto\chi_i(g)\tilde{\rho}(g)$ (where 
$\chi_i(g)\in\mathbf{C}^{\times}$ and 
$\tilde{\rho}(g):V\to V$
where $V$ representation space of $\rho$). 
Let $\theta_{i,\rho}$
be the corresponding induced representation of $G$. 

**Proposition 25.**  
1. $\theta_{i,\rho}$ is irreducible.
2. If $\theta_{i,\rho}$ and $\theta_{i',\rho'}$ are 
isomorphic, then $i=i'$ and $\rho$ is isomorphic to 
$\rho'$. 
3. Every irreducible representation of $G$
is isomorphic to one of $\theta_{i,\rho}$.

(1) is proved using Mackey's criterion ($\S 7.4$ of 
Serre's book), as follow: Let $s\not\in G_i$ and let 
$K_s=G_i\cap sG_is^{-1}$. We have to show that if 
we compose the representation $\chi_i\otimes \tilde{\rho}$
of $G_i$ with the two injections $K_s\to G_i$ defined
by $x\mapsto x$ and $x\mapsto s^{-1}xs$, we obtain 
two disjoint representations of $K_s$ (i.e. 
they have no common subrepresentations). To do this, 
it is enough to check that the restrictions of these 
representations to subgroup $A$ of $K_s$ are disjoint
(since common subrepresentation of $K_s$ implies 
common subrepresentation of $A$). 

> But the first restricts to a multiple of $\chi_i$
and the second to a multiple of $s\chi_i$; since 
$s\not\in G_i=A\cdot H_i$ we have $s\chi_i\ne \chi_i$
and so the two representations in question are 
indeed disjoint. 

*Proof.* Consider the first restriction $A\to K_s\to G_i$
by $x\mapsto x$. Then for $x\in A$, we have 
$\tilde{\rho}(a)=\rho(1)=\text{id}_V$ so 

$$x\mapsto (\chi_i\otimes \tilde{\rho})(x)
=\chi_i(x)\text{id}_V.$$
Consider the second restriction $x\mapsto s^{-1}xs$.
If $x\in A$ then $s^{-1}xs\in A$ so similarly, we have 
$\tilde{\rho}(s^{-1}xs)=\text{id}_V$ so 

$$x \mapsto \chi_i(s^{-1}xs)\text{id}_V=(s\chi_i)(x)\text{id}_V$$

---

Now we prove (2): 

> The restriction of $\theta_{i,\rho}$ to $A$ only 
involves characters $\chi$ belonging to the orbit $H\chi_i$
of $\chi_i$. This shows that $\theta_{i,\rho}$ determines $i$. 

As the statement said, we consider character $\chi^i$ of $\theta_{i,\rho}$
for $a\in A$. Recall the character for induced representation for $s\in G$,
$H$ subgroup of $G$, $f:H\to \mathbf{C}^{\times}$, is 

$$\text{Ind}_H^G(f)(s)=f'(s)=\frac{1}{|H|}\sum_{t\in G, t^{-1}st\in H}f(t^{-1}st)$$
Hence, 

$$\begin{aligned}
\chi^i(a) & = \frac{1}{|G_i|}\sum_{t\in G, t^{-1}at\in G_i}
\chi_{\chi_i\otimes \tilde{\rho}}(t^{-1}at), \\
& = \frac{1}{|G_i|}\sum_{t\in G} \chi_i(t^{-1}at)\chi_{\tilde{\rho}}(t^{-1}at), 
\; (A \text{ normal so }  t^{-1}at\in A\subset G_i \; \forall t\in G), \\
& = \frac{\text{dim }V}{|G_i|}\sum_{t\in G}\chi_i(t^{-1}at), \; 
(t^{-1}at\in A \Rightarrow \tilde{\rho}(t^{-1}at)=\rho(1)=\text{id}_V), \\
& = \frac{\text{dim }V}{|G_i|} \sum_{a'\in A,h\in H}\chi_i((a'h)^{-1}a(a'h)),\\
& = \frac{\text{dim }V}{|G_i|} \sum_{a'\in A,h\in H} \chi_i(h^{-1}ah), \; 
(A \text{ abelian}) \\
& = \frac{|A|\text{dim }V}{|G_i|} \sum_{h\in H} (h\chi_i)(a).
\end{aligned}$$

We would like to show that $\chi^i\ne \chi^{i'}$ for 
$i\ne i'$. Observe that $|G_i|$ divides $|G|$
and that $h\chi_i\in \text{Hom }(A,\mathbf{C}^*)$
is $1$-dimensional irreducible representation of $A$
so the character defined by 
$\tau^i(a)=\frac{|G|}{|G_i|}\sum_{h\in H}(h\chi_i)(a)$
corresponds to direct sum of representations from $H\chi_i$.
Since with $i\ne i'$ then $H\chi_i$ and $H\chi_{i'}$
are disjoint so $\tau^i\ne \tau^{i'}$, implying 
$\chi^i\ne \chi^{i'}$. 

> Let $W$ be the representation space for $\theta_{i,\rho}$, let 
$W_i$ be the subspace of $W$ corresponding to $\chi_i$ (the set 
of $x\in W$ such that $\theta_{i,\rho}(a)x=\chi_i(a)x$ for all 
$a\in A$). The subspace $W_i$ is stable under $H_i$ and the representation
of $H_i$ in $W_i$ is isomorphic to $\rho$; whence $\theta_{i,\rho}$
determines $\rho$.

Recall from $\S 7.1$ of Serre's book, $W$ can be identified with 
$W=\mathbf{C}[G]\otimes_{\mathbf{C}[G_i]}V$ where 
$V$ is the representation space of $\chi_i\otimes \tilde{\rho}$.
In particular, this is a $\mathbf{C}[G]$-module where $g$ acts 
on $g'\otimes v$ by $(gg')\otimes v$. Also note that, 
$(gg_i)\otimes v$ and $g\otimes (\chi_i\otimes \tilde{\rho})(g_i)v$
are considered the same in $W$ for $g_i\in G_i$. 

Now, we identify $W_i$. For $a\in A, g\otimes v\in W$, we have 
$\theta_{i,\rho}(a)(g\otimes v)= (ag)\otimes v=g\otimes(g^{-1}ag)v$. 
Since $g^{-1}ag\in A$ so 
$(\chi_i\otimes \tilde{\rho})(g^{-1}ag)v=\chi_i(g^{-1}ag)v$.
Thus, 
$\theta_{i,\rho}(a)(g\otimes v)=\chi_i(g^{-1}ag)(g\otimes v$. Thus, in order for 
$\theta_{i,\rho}(a)(g\otimes v)=\chi_i(a)(g\otimes v)$ for all 
$a\in A$, we must have $\chi_i(a)=(g\chi_i)(a)$ for all $a\in A$.
This follows $g\in H_i$. Thus, 
$W_i=\mathbf{C}[H_i]\otimes_{\mathbf{C}[G_i]} V$. 

With this, it is obvious that $W_i$ is stable under $H_i$. 
Furthermore, observe $W_i$ is spanned by $1\otimes v_j$
where $v_j$'s basis of $V$, $1$ identity in $H_i$ (this holds
since $h\otimes v=1\otimes \rho(h)v$ for all $h\in H_i,v\in V$). 
Hence, one can easily construct isomorphism representation of 
$H_i$ in $W$ to $\rho$, as desired. 

---

To show (3), it suffices to show that 

$$\sum_{i\in X/H}\sum_{\rho}(\text{dim }
\theta_{i,\rho})^2=|G|$$

where $\rho$ is summed over all irreducible 
representations of $H_i$. We have 

$$\begin{aligned} 
\text{dim }\theta_{i,\rho}
&=\text{dim }\text{Ind}_{G_i}^G
(\chi_i\otimes \tilde{\rho}),\\
& = \frac{|G|}{|G_i|}\text{dim } 
(\chi_i\otimes \tilde{\rho}), \\
& = \frac{|G|}{|G_i|}\text{dim }\rho
\end{aligned}$$

so for fixed $i$ then 

$$\sum_{\rho}(\text{dim }\theta_{i,\rho})^2
= \frac{|G|^2}{|G_i|^2}|H_i|= \frac{|H|^2}{|H_i|}.$$

Hence, it suffices to show that 
$\sum_{i\in X/H}\frac{|H|^2}{|H_i|}=|G|$
or $\sum_{i\in X/H}\frac{|H|}{|H_i|}=|A|$.
Note that $X=\text{Hom }(A,\mathbf{C}^*)$
is isomorphic to $A$ (see 
[Conrad's note](https://kconrad.math.uconn.edu/blurbs/grouptheory/charthyshort.pdf)) so 

$$|A|=|X|=\sum_{i\in X/H}|H\chi_i|=
\sum_{i\in X/H} \frac{|H|}{|H_i|}.$$

We are done.