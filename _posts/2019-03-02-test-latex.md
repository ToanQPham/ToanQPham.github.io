---
layout: post
title: "Test $\\LaTeX$"
categories: misc
---

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt 
ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit 
in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat 
cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

The main idea in this chapter is that the count for
number of walks of length $\ell$ in a graph can be done by finding
the entries of certain matrix or equivalently, finding the
eigenvalues of such matrix. Conversely, one can even
find the eigenvalues of such matrix by counting number
of closed walks of lenght $\ell$ in a graph corresponding to such matrix:

The \vocab{adjacency matrix} of graph $G$ is $p\times p$
matrix $\mathbf{A}=\mathbf{A}(G)$, over the field
of complex numbers, whose $(i,j)$-entry $a_{i,j}$ is equal
to number of edges incident to $v_i$ and $v_j$. Thus
$\mathbf{A}$ is a real symmetric matrix (so real
eigenvalues) whose trace is the number of loops in $G$. 

This chapter shows that for any integer $\ell\ge 1$, the $(i,j)$-entry
of the matrix $\mathbf{A}(G)^{\ell}$ is equal to the number of walks
from $v_i$ to $v_j$ in $G$ of length $\ell$. Furthermore, due to
the fact that $\mathbf{A}(G)$ is real symmetric means there
exists orthogonal matrix $U$ such that 
$U^{-1}\mathcal{A}^{\ell}U$ is a diagonal matrix. This implies
that if $\lambda_1,\ldots, \lambda_p$ are eigenvalues of 
$\mathbf{A}(G)$ then there exists real numbers $c_1,\ldots, c_p$
such that for all $\ell\ge 1$ then 
\[ (\mathbf{A}(G)^{\ell})_{i,j}=c_1\lambda_1^{\ell}
+c_2\lambda_2^{\ell}+\ldots+c_p\lambda_p^{\ell}.\]
In a particular case where we want to count number of closed walks
of length $\ell$ (from any vertex), 
this is then equal to 
\[f_G(\ell)=\sum_{i=1}^p
(\mathbf{A}(G)^{\ell})_{i,i}=\text{trace}(\mathbf{A}(G)^{\ell})
=\lambda_1^{\ell}+\ldots+\lambda_p^{\ell}.\]
An amazing fact is that if we know formula for $f_G(\ell)$ for 
all $\ell$ then we can determine eigenvalues of $\mathbf{A}$.
In particular, if we can show 
$f_G(\ell)=\alpha_1^{\ell}+\ldots+\alpha_p^{\ell}$
for all $\ell\ge1 $ then $\alpha_i$'s are eigenvalues of $\mathbf{A}$.