---
layout: post
title: "Test commutative diagram drawing with MathJax"
categories: 
- LaTeX
tag: 
- latex
- xypic
- xyjax
---

I use [xyjax](https://github.com/sonoisa/XyJax) which
is [xy-pic](http://xy-pic.sourceforge.net/) extension for MathJax. 

$$
\xymatrix {
U \ar@/_/[ddr]_y \ar@{.>}[dr]|{\langle x,y \rangle} \ar@/^/[drr]^x \\
 & X \times_Z Y \ar[d]^q \ar[r]_p & X \ar[d]_f \\
 & Y \ar[r]^g & Z
}
$$

$$
\begin{xy}
\xymatrix {
U \ar@/_/[ddr]_y \ar@{.>}[dr]|{\langle x,y \rangle} \ar@/^/[drr]^x \\
 & X \times_Z Y \ar[d]^q \ar[r]_p & X \ar[d]_f \\
 & Y \ar[r]^g & Z
}
\end{xy}
$$

$$
\xymatrix{A \ar@{}[dr]|{=} \ar[d] \ar[r] & B \ar[d] \\ B \ar[r] & C }
$$

Here is the [User guide](http://texdoc.net/texmf-dist/doc/generic/xypic/xyguide.pdf)
how to use xy-pic. 
