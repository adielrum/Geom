### **Problem Statement**
Show that a projectivity relating distinct lines is a perspectivity if and only if it has a fixed point.

---

### **Proof**

Let $T: l \to l'$ be a projectivity between distinct lines $l$ and $l'$.
Let $X = l \cap l'$. Since $l \neq l'$, $X$ is a unique point.

**Direction 1: Perspectivity $\implies$ Fixed Point**
If $T$ is a perspectivity, there exists a center $O$ such that for all $P \in l$, $P, T(P), O$ are collinear.
Consider the intersection point $X = l \cap l'$.
$T(X)$ must be on $l'$ (codomain).
Also, $X, T(X), O$ must be collinear.
Since $X \in l$ and $X \in l'$, $X$ lies on both lines.
If $O$ is not on $l$ or $l'$:
The line connecting $O$ and $X$ intersects $l'$ at a unique point.
Since $X$ is on $l'$, the line $OX$ intersects $l'$ at $X$.
Thus $T(X) = X$.
So $X$ is a fixed point.

**Direction 2: Fixed Point $\implies$ Perspectivity**
Suppose $T: l \to l'$ has a fixed point.
Since $T(P) \in l'$, a fixed point $P$ must satisfy $P \in l \cap l'$.
Since $l \neq l'$, the only possible fixed point is $X = l \cap l'$.
So we assume $T(X) = X$.

We need to show there exists a center $O$ such that $T = [O; l \to l']$.
Let $A, B$ be two other points on $l$ (distinct from $X$).
Let $A' = T(A)$ and $B' = T(B)$ on $l'$.
Construct the lines $AA'$ and $BB'$.
Let $O = AA' \cap BB'$.
(If $AA' = BB'$, then $A, A', B, B'$ are collinear, which implies $l=l'$, contradiction).
So $O$ is a unique point.

Now consider the perspectivity $S = [O; l \to l']$.
$S(A) = A'$ (by construction of $O$).
$S(B) = B'$ (by construction of $O$).
$S(X)$?
The line $OX$ intersects $l'$ at $X$ (since $X \in l'$ and $X \in l$).
So $S(X) = X$.

Now compare $T$ and $S$.
Both are projectivities from $l$ to $l'$.
They agree on 3 distinct points: $A, B, X$.
$T(A) = A' = S(A)$
$T(B) = B' = S(B)$
$T(X) = X = S(X)$
By the Fundamental Theorem (Exercise 9), $T = S$.
Since $S$ is a perspectivity, $T$ is a perspectivity.

**Conclusion:**
A projectivity between distinct lines is a perspectivity if and only if the intersection point of the two lines is a fixed point.
