---
layout: post
title: "OPPD - Day 3: Structure theory of linear algebraic groups"
categories: 
- Algebraic groups
tag: 
- OPPD
---

On 21/03/2020, I had a quick read through structure theory of linear algebraic groups
so that I know certain terminologies, how they are defined. 

I learn these from [Fiona Murnaghan's short note](http://www.math.toronto.edu/murnaghan/courses/algp.pdf)
about linear algebraic groups and [Daniel Bump's note](http://sporadic.stanford.edu/bump/math263/hecke.pdf),
starting from section 4. 

Also, I am stuck at a certain argument when reading Bushnell, Henniart's book 
Local Langlands for GL(2) and spend some time with it but with no 
progress. 

I will try to write something if I have time. 

OK, here is roughly what I learnt on this day:

## Structure of $\text{GL}_n(F)$
Center of $GL_n$ is denoted $Z$. 

In matrix manners, the diagonal torus $T$ 
is subgroup of all diagonal matrices, the 
standard Borel subgroup $B$ consists of all 
upper triangular matrices. The unipotent radical 
$U$ consists of all upper triangular unipotent 
matrices. Note $T$ normalizes $U$ and $B$ is 
semidirect product $TU$. Let $W$, the \vocab{Weyl 
group} of $G$, is the group $N_G(T)/T$ where 
$N_G(T)$ normalizer of $T$. For $G=GL_n(F)$,
$W$ is subgroup of all monomial matrices (one 
nonzero entry in each row and each column) so 
$W$ can be identified with $S_n$.

In different view, by picking $n$-dimensional vector 
space $V$ over $F$, $GL_n(F)$ can be identified with 
$GL(V)$. Define a **flag** $W_{\bullet}$ in $V$
to be strictly increasing sequence of subspaces 
$W_0\subset W_1\subset \cdots \subset W_m=V$. 
Subgroup of $GL(V)$ that stabilizes flag $W_{.}$,
i.e. with the property that $gW_i=W_i$ for all $i$ 
is called \vocab{parabolic subgroup} of $G$
associated to flag $W_{\bullet}$.

If $\{v_1,\ldots, v_n\}$ basis of $V$ then 
stabilizer of flag $\{(v_1)\subset (v_1,v_2)\subset 
\cdots \subset (v_1,\ldots, v_n)\}$ is called 
\vocab{Borel subgroup}. In the case of $GL(V)$,
stabilizer of any two such (maximal) flags 
are conjugate under $GL(V)$. 

If $W_{\bullet}=\{W_0\subset W_1\subset \cdots 
\subset W_m\}$ then inside the associated 
parabolic subgroup $P$, there exists normal 
subgroup $N$ consisting of elements who operating 
trivially on $W_{i+1}/W_i$ for $0\le i \le m-1$,
which is called unipotent radical of $P$. 
There is a semidirect product decomposition $P=MN$
with $M=\prod_{i=0}^{m-1} GL(W_{i+1}/W_i)$. 
The decomposition $P=MN$ is called **Levi 
decomposition** of $P$ with $M$ called **Levi
subgroup** of $P$. 

Let $K=GL_n(\mathfrak{o})$ denote subgroups of 
elements in $G$ in $\mathfrak{o}$ and whose 
determinant is unit in $\mathfrak{o}$. This 
is a maximal open compact subgroup of $GL_n(F)$,
as shown in following exercise.

*Exercise.*
Let $V$ be $n$-dimensional vector space over $F$.
Let $L$ be lattice on $V$, i.e. $\mathfrak{o}$-submodule 
rank $n$. Show that stabilizer of $L$ is open compact 
subgroup of $G=GL(V)$. If $C$ is any open compact 
subgroup then there is lattice $L$ such that 
$C$ lies in stabilizer of $L$. Hence, up to 
conjugacy, $K$ is the unique maximal open compact subgroup 
of $GL_n(F)$. 

For every integer $m\ge 1$, the map $\mathfrak{o} 
\to \mathfrak{o}/\mathfrak{p}^m$ induces map 
$K\to GL_n(\mathfrak{o}/\mathfrak{p}^m)$. 
The kernel $K_m$ of this map is called 
\vocab{principal congruence subgroup of level $m$}.
We also define $K_0$ to be $K$. For all $m\ge 1$,
we have $K_m = 1_n+\mathfrak{p}^m M_n(\mathfrak{o})$.
$K_m$ are open compact subgroups of $G$ and 
gives basis of neighborhood at the identity. 

**Bruhat decomposition** gives 
$G=\bigsqcup_{w\in W}BwB=\bigsqcup_{w\in W}BwU$.
Proof use row reduction (on the left) and 
column reduction (on the right) by elementary
operations.

**Cartan decomposition** gives,
for $A=\{\text{diag}(\Pi^{m_1},\ldots,\Pi^{m_n})
: m_i\in \ZZ_{\ge 0}, m_1\le \cdots \le m_n\}$ then 
$G=\bigsqcup_{a\in A} KaK$. 

**Iwasawa decomposition** gives $G=KB$. 

**Iwahori factorization** gives 
for $m\ge 1$ then $K_m=(K_m\cap U^-)(K_m\cap T)
(K_m\cap U)$ where $U^-$ subgroup of all 
lower triangular unipotent matrices. 

## In language of algebraic groups
(Very roughly, so that I can read other things)


An **algebraic group** is an algebraic variety $G$
defined over some field $F$ with morphims $m:G\times 
G\to G$ and $\text{inv}: G\to G$ becomes multiplication 
and inverse map on $G(E)$ making $G(E)$ of 
$E$-rational points (i.e. $G(E)=G\cap E^n$) into 
a group when $E$ is commutative $F$-algebra. 
Affine algebraic group is when $G$ is affine variety, 
example is multiplicative group $G_m$, with 
$G(E)=E^{\times}$. 

A **torus** is group $T$ that is isomorphic to 
direct product of $G_m^k$ for some $k$. If 
the isomorphism is defined over $F$ we say $T$ 
\vocab{split} (over $F$). 

For affine algebraic group $G$ over $F$. 
By \vocab{representation} we mean morphism 
$\rho:G\to GL_n$ for some $n$ such that 
$\rho:G(E)\to GL_n(E)$ group hom for any 
commutative $F$-algebra $E$. 

By Jordan decomposition, $g\in G$ then 
exists $g_s,g_u\in G$ such that $g=g_sg_u=g_ug_s$,
$g_s$ semisimple, $g_u$ unipotent.
Hence $g\in G$ is called **semisimple**
if $g=g_s$ and **unipotent** if $g=g_u$. 

$G$ is unipotent if all its elements are unipotnent.
Group $G$ has maximal normal unipotent subgroup 
$U$, called **unipotent radical**. If $U$ 
is trivial then $G$ is **reductive**. 
If it is reductive and has no nontrivial normal 
tori then $G$ is **semisimple**. For example 
group of $\left\{\begin{pmatrix}
a & b \\ 0 &d
\end{pmatrix}\right\}$ is not reductive since 
$\left\{ \begin{pmatrix}
1 & x\\ 0 & 1
\end{pmatrix} \right\}$ is normal unipotent subgroup.
Group $SL_n$ is semisimple. Group $GL_n$ is 
reductive but not semisimple. 

Maximal torus $T$ is subgroup as large as possible 
such that $T$ product of multiplicative groups. 
If $T$ splits over $F$ then $G$ is **$F$-split**.
All maximal tori in $G(F)$ are conjugate if $F$
algebraically closed. 

If $G$ is $F$-split reductive group and $T$ is 
$F$-split maximal torus, $N$ normalizer of $T$
then $N/T$ is Weyl group $W$. 