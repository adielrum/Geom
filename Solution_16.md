### **Proof Objective**
We must prove that there is **only one** projective collineation relating two specified quadrangles.

Let the first quadrangle consist of points $A, B, C, D$ (no three collinear) and the second consist of $A', B', C', D'$ (no three collinear). We aim to show that if two projective collineations $T$ and $S$ both map $A \to A'$, $B \to B'$, $C \to C'$, and $D \to D'$, then $T = S$.

---

### **Step 1: Reduce to the "Fixed Point" Case**
Consider the composition of mappings $U = S^{-1} \circ T$.

Since $T$ and $S$ both map the first quadrangle to the second:
* $T(A) = A'$ and $S(A) = A' \implies S^{-1}(A') = A$
* Therefore, $U(A) = S^{-1}(T(A)) = S^{-1}(A') = A$.

By the same logic, $U$ fixes $B$, $C$, and $D$.
$$U(A)=A, \quad U(B)=B, \quad U(C)=C, \quad U(D)=D$$

If we can prove that **the only projective collineation that fixes four points in general position is the Identity transformation**, then $U = I$. This would imply $S^{-1} \circ T = I$, and consequently $T = S$, proving uniqueness.

---

### **Step 2: Apply the Fundamental Theorem of Coordinates**
To prove that $U$ is the identity, we use **Theorem 2 (Fundamental Theorem of Coordinates)** from the summary. This theorem states that we can choose a basis for $R^3$ such that the homogeneous coordinates of any four points in general position (no three collinear) are:
* $A = [1, 0, 0]$
* $B = [0, 1, 0]$
* $C = [0, 0, 1]$
* $D = [1, 1, 1]$

Let $M$ be the $3 \times 3$ invertible matrix representing the projective collineation $U$. Since $U$ fixes these points, the matrix $M$ must map the vector representative of each point to a scalar multiple of itself.

---

### **Step 3: Matrix Analysis**

**1. Analyzing the first three points (Basis Vectors):**
* **For point A ($e_1$):**
    $$M \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} = k_1 \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}$$
    This implies the first column of $M$ is $(k_1, 0, 0)^T$.

* **For point B ($e_2$):**
    $$M \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix} = k_2 \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}$$
    This implies the second column of $M$ is $(0, k_2, 0)^T$.

* **For point C ($e_3$):**
    $$M \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix} = k_3 \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}$$
    This implies the third column of $M$ is $(0, 0, k_3)^T$.

At this stage, $M$ is a diagonal matrix:
$$M = \begin{pmatrix} k_1 & 0 & 0 \\ 0 & k_2 & 0 \\ 0 & 0 & k_3 \end{pmatrix}$$

**2. Analyzing the fourth point D ($e_1 + e_2 + e_3$):**
The point $D$ has coordinates $(1, 1, 1)$. Since $U$ fixes $D$:
$$M \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix} = k_4 \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$$

Substituting the diagonal matrix $M$ we found:
$$\begin{pmatrix} k_1 & 0 & 0 \\ 0 & k_2 & 0 \\ 0 & 0 & k_3 \end{pmatrix} \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix} = \begin{pmatrix} k_1 \\ k_2 \\ k_3 \end{pmatrix}$$

For this result to be projectively equivalent to the point $[1, 1, 1]$, the vector $(k_1, k_2, k_3)^T$ must be a scalar multiple of $(1, 1, 1)^T$.
$$k_1 = k_4$$
$$k_2 = k_4$$
$$k_3 = k_4$$

Therefore, $k_1 = k_2 = k_3 = k$.

---

### **Conclusion**
The matrix representing $U$ is:
$$M = \begin{pmatrix} k & 0 & 0 \\ 0 & k & 0 \\ 0 & 0 & k \end{pmatrix} = kI$$

In projective geometry, a transformation represented by a scalar multiple of the identity matrix ($kI$) induces the **Identity Collineation** on $P^2$.

Since $U = I$, then:
$$S^{-1} \circ T = I \implies T = S$$

Thus, the projective collineation relating the two quadrangles is unique.