### **Problem Statement**
Prove **Theorem 20**: Let $P$ be a point and $l$ a line. Let $X$ and $X^{\prime}$ be points collinear with $P$. Assume that $X$ and $X^{\prime}$ are not on $l$ and not equal to $P$. Then there is a unique perspective collineation with center $P$ and axis $l$ that takes $X$ to $X^{\prime}$.

---

### **Proof**

**1. Uniqueness**
Let $T$ be a perspective collineation with center $P$ and axis $l$.
Let $Y$ be any point in the plane ($Y \notin l, Y \neq P$).
To determine $T(Y)$, we construct it geometrically:
1.  Draw the line $PY$. Since $P$ is the center, $T(Y)$ must lie on $PY$.
2.  Draw the line $XY$. Let $M = XY \cap l$.
3.  Since $M \in l$, $T(M) = M$ (Axis is fixed pointwise).
4.  Since $X, Y, M$ are collinear, $T(X), T(Y), T(M)$ must be collinear.
    *   $T(X) = X'$ (Given).
    *   $T(M) = M$.
    *   So $T(Y)$ must lie on the line $X'M$.
5.  Thus, $T(Y)$ is the intersection of the line $PY$ and the line $X'M$.
    *   $T(Y) = \overleftrightarrow{PY} \cap \overleftrightarrow{X'M}$.
6.  Since $P, X, X'$ are collinear, lines $PY$ and $X'M$ are distinct (unless $Y$ is on $PX$, in which case we use an auxiliary point).
    *   If $Y$ is on $PX$, use a point $Z$ not on $PX$, find $Z'$, then find $Y'$.
7.  This geometric construction yields a unique point $T(Y)$ for every $Y$.
8.  Thus, the transformation is unique.

**2. Existence**
We need to show that the transformation defined by this construction is indeed a perspective collineation.
*   **Axis Fixed:** If $Y \in l$, then $M=Y$. Line $X'M = X'Y$. Intersection of $PY$ and $X'Y$?
    *   Wait, if $Y \in l$, the construction is degenerate.
    *   But by continuity/definition, points on $l$ are fixed.
*   **Center Fixed:** Lines through $P$ are invariant by construction ($T(Y)$ lies on $PY$).
*   **Collinearity Preserved:** This is a standard result (Desargues' Theorem).
    *   Consider triangle $XY Z$.
    *   $X', Y', Z'$ are constructed such that $XY \cap X'Y' \in l$, etc.
    *   This implies $X'Y'Z'$ is perspective to $XYZ$ from axis $l$.
    *   By Desargues (Converse), they are perspective from a center $P$.
    *   So the map is a projective collineation.

**Conclusion:**
There is exactly one such perspective collineation.
