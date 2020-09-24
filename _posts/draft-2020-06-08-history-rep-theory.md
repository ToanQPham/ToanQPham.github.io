---
layout: post
title: "Historical account of Representation theory"
categories: 
- Representation Theory
- Lie Groups
tag: 
---

I think the idea is that lots of representations of reductive groups (in this case I think SL2) can be realized as representations in spaces of functions satisfying some convenient equation, and Whittaker functions happen to be in these spaces.

There is some functional equation involved with spherical harmonics etc in Jacquet's 1967 paper, so I believe the so-called Whittaker model arises from the rep theory of SO(2, R). 
On the other hand, q-deformed Whittaker functions (showing up as solutions to quantum D-modules over flag varieties) have another physical interpretation as eigenfunctions of the quantum Toda lattice, being related to the rep theory of quantum Yang-Baxter.

https://mathoverflow.net/questions/109629/definitions-of-reductive-and-semisimple-groups

# Lie groups:

From 
https://mathoverflow.net/q/16399/89665

The primary reason for studying Lie algebras is the following fundamental fact: the representation theory of a Lie algebra is the same as the representation theory of the corresponding connected, simply connected Lie group.

Of course, the representation theory of a Lie group in general is very complicated. First of all, it might not be connected. Then the Lie algebra cannot tell the difference between the whole group and the connected component of the identity. This connected component is normal, and the quotient is discrete. So to understand the representation theory of the whole group requires, at the very least, knowing the representation theory of that discrete quotient. Even in the compact case, this would require knowing the representation theory of finite groups. For a given finite group, the characters know everything, but of course the classification problem in general is completely intractable.

The other thing that can go wrong is that even a connected group need not be simply connected. Any connected Lie group is a group quotient of a connected, simply connected group with the same Lie algebra, where the kernel is a discrete central subgroup of the connected, simply connected guy. So the representation theory of the quotient is the same as the representations of the simply connected group for which this central discrete acts trivially.

There is a complete classification of connected compact groups. You start with the steps above: classifying the disconnected groups is intractable, but a connected one is a quotient of a connected simply connected one. This simply connected group is compact iff the corresponding Lie algebra is semisimple; otherwise it has some abelian parts. In general, any compact group is a quotient by a central finite subgroup of a direct product: torus times (connected simply connected) semisimple. Torus actions are easy, and the representation theory of semisimples is classified as well. Whether your representation descends to the quotient I'm not entirely sure I know how to read off of the character. When the group is semisimple (no torus part), I do: finite-dimensional representations are determined by their highest weights (which can be read from the character), which all lie in the "weight" lattice; quotients of the simply-connected semisimple correspond exactly to lattices between the weight lattice and the "root" lattice, and you can just check that your character/weights are in the sublattice.

All of this should be explained well in your favorite Lie theory textbook.