### **Problem Statement**
Prove **Theorem 19**: Suppose that a nontrivial perspective collineation with center $P$ takes $X$ to $X^{\prime}$. Then $P$, $X$, and $X^{\prime}$ are collinear.

---

### **Proof**

**Definition of Perspective Collineation:**
A perspective collineation is a projective collineation that fixes a line $l$ pointwise (Axis) and fixes a pencil of lines through a point $P$ (Center).

**Proof:**
1.  Let $T$ be the perspective collineation with center $P$.
2.  By definition of the center, every line passing through $P$ is an invariant line ($T(m) = m$ for all $m \ni P$).
3.  Let $X$ be any point.
4.  Consider the line $m = \overleftrightarrow{PX}$ connecting $P$ and $X$.
5.  Since $m$ passes through $P$, $m$ is an invariant line.
6.  Therefore, if $X \in m$, then $T(X) \in T(m) = m$.
7.  So $X' = T(X)$ lies on the line $m$.
8.  Since $P, X, X'$ all lie on line $m$, they are collinear.

**Note:**
If $X=P$, then $X'=P$, so they are collinear.
If $T$ is the identity, $X'=X$, so they are collinear.

**Conclusion:**
Theorem 19 is proved directly from the definition of the Center.
