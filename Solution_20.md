### **Problem Statement**
If $T$ is a projective collineation, prove that the restriction of $T$ to one line $l$ is a projectivity. Prove also that every projectivity arises in this way.

---

### **Proof**

**Part 1: Restriction is a Projectivity**
Let $T: P^2 \to P^2$ be a projective collineation.
Let $l$ be a line in $P^2$.
Since $T$ is a collineation, it maps lines to lines.
Let $l' = T(l)$.
The restriction $T|_l: l \to l'$ is a bijection.
We need to show it is a projectivity.
A projectivity is defined as a composition of perspectivities, or algebraically as a map induced by a linear transformation.
Since $T$ is induced by $A \in GL(3)$, the restriction to the subspace corresponding to $l$ (a 2D subspace of $R^3$) is induced by the restriction of the linear map $A$ to that subspace.
The restriction of a linear map to a subspace is a linear map.
Since $T$ is invertible, the restriction is invertible.
Thus, $T|_l$ is induced by an invertible linear map between the 2D subspaces representing $l$ and $l'$.
Therefore, $T|_l$ is a projectivity.

**Part 2: Every Projectivity Arises in This Way**
Let $S: l \to l'$ be a given projectivity.
We want to find a projective collineation $T: P^2 \to P^2$ such that $T|_l = S$.

1.  Let $A, B, C$ be three distinct points on $l$.
2.  Let $A' = S(A), B' = S(B), C' = S(C)$ be their images on $l'$.
3.  Choose a point $D$ not on $l$.
4.  Choose a point $D'$ not on $l'$.
5.  Consider the set of 4 points $\{A, B, C, D\}$ and $\{A', B', C', D'\}$.
    *   No three of $\{A, B, C, D\}$ are collinear?
        *   $A, B, C$ are collinear (on $l$).
        *   This violates the "General Position" requirement for the Fundamental Theorem (Theorem 11).
        *   We cannot directly apply Theorem 11 to these 4 points.

**Correct Construction:**
We need to define $T$ on a basis.
Let $u, v$ be a basis for the subspace $W_l$ corresponding to $l$.
Let $S$ be induced by a linear map $L: W_l \to W_{l'}$.
We can extend the linear map $L$ to the whole space $R^3$.
Let $w$ be a vector not in $W_l$.
Let $W_{l'}$ be the subspace for $l'$.
Choose any vector $w'$ not in $W_{l'}$.
Define a linear map $\bar{A}: R^3 \to R^3$ by:
$\bar{A}(x) = L(x)$ for $x \in W_l$.
$\bar{A}(w) = w'$.
Since $L$ is invertible on $W_l$ and $w \notin W_l$, $w' \notin W_{l'}$, the map $\bar{A}$ is invertible (it maps a basis $\{u, v, w\}$ to a basis $\{L(u), L(v), w'\}$).
Let $T$ be the projective collineation induced by $\bar{A}$.
Then for any $P \in l$, represented by $x \in W_l$:
$T(P) = [\bar{A}(x)] = [L(x)] = S(P)$.
Thus $T|_l = S$.

**Conclusion:**
Every projectivity between lines can be extended to a projective collineation of the plane.
