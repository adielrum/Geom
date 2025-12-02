### **Problem Statement**
Let $P$, $Q$, and $R$ be distinct points on a line $l$, and let $P'$, $Q'$, and $R'$ be distinct points on a line $l'$. Prove that there is a unique projectivity sending $P$ to $P'$, $Q$ to $Q'$, and $R$ to $R'$.

---

### **Proof**

**1. Fundamental Theorem of Projective Geometry (Dimension 1)**
The problem asks to prove the Fundamental Theorem for the projective line $P^1$.
While **Theorem 11** in Summary.md applies to $P^2$ (4 points), the 1-dimensional analog states that a projectivity on a line is uniquely determined by the images of **3 distinct points**.

**2. Coordinate Approach**
Let $l$ and $l'$ be identified with $P^1$.
We can choose coordinates on $l$ such that:
$P = [1, 0]$
$Q = [0, 1]$
$R = [1, 1]$ (Unit point)
This is always possible by the Fundamental Theorem of Coordinates (Theorem 2 applied to subspace).

Similarly, on $l'$, we can choose coordinates such that:
$P' = [1, 0]$
$Q' = [0, 1]$
$R' = [1, 1]$

**3. Existence**
We want a transformation $T$ (represented by matrix $M$) such that $T(P)=P', T(Q)=Q', T(R)=R'$.
If we map the basis of $l$ to the basis of $l'$ via the identity matrix in these specific coordinates, we get the desired map.
In general coordinates, there exists a linear map $A$ sending basis vectors of $P, Q$ to representatives of $P', Q'$ scaled such that $R \to R'$.

**4. Uniqueness**
Suppose there are two projectivities $T$ and $S$ mapping $P, Q, R$ to $P', Q', R'$.
Consider $U = S^{-1} \circ T$.
$U$ is a projectivity from $l$ to $l$ such that:
$U(P) = P$
$U(Q) = Q$
$U(R) = R$

Let $U$ be represented by a $2 \times 2$ matrix $M$.
Using the standard basis $P=[1,0], Q=[0,1], R=[1,1]$:
$M \begin{pmatrix} 1 \\ 0 \end{pmatrix} = k_1 \begin{pmatrix} 1 \\ 0 \end{pmatrix} \implies$ 1st col is $(k_1, 0)^T$.
$M \begin{pmatrix} 0 \\ 1 \end{pmatrix} = k_2 \begin{pmatrix} 0 \\ 1 \end{pmatrix} \implies$ 2nd col is $(0, k_2)^T$.
$M = \begin{pmatrix} k_1 & 0 \\ 0 & k_2 \end{pmatrix}$.

Action on $R=[1,1]$:
$M \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \begin{pmatrix} k_1 \\ k_2 \end{pmatrix} = k_3 \begin{pmatrix} 1 \\ 1 \end{pmatrix}$.
This implies $k_1 = k_3$ and $k_2 = k_3$.
So $k_1 = k_2$.
$M = k_1 I$.
This represents the identity transformation.
So $U = I \implies S = T$.

**Conclusion:**
There is a unique projectivity sending any 3 distinct points to any 3 distinct points.
