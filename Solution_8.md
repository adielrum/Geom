### **Problem Statement**
A projectivity is a composition of finitely many perspectivities. Each projectivity relates a pair of (not necessarily distinct) lines. For each line $l$, prove that the set of all projectivities that take $l$ to itself is a group. With respect to an appropriate choice of homogeneous coordinates, find a matrix representation for this group.

---

### **Solution**

#### **1. Group Property**
Let $G_l$ be the set of all projectivities $T: l \to l$.
A projectivity is a bijection from $l$ to $l$ that preserves the cross-ratio (or is defined as a composition of perspectivities).

*   **Closure:** If $T_1, T_2 \in G_l$, then $T_1$ and $T_2$ are compositions of perspectivities. Thus $T_1 \circ T_2$ is a composition of perspectivities mapping $l \to l \to l$, so it is in $G_l$.
*   **Associativity:** Composition of functions is always associative.
*   **Identity:** The identity map $I: l \to l$ is a projectivity (0 perspectivities, or composition of inverses). $I \in G_l$.
*   **Inverse:** If $T \in G_l$ is a projectivity, it is invertible (since it's a bijection and composition of invertible perspectivities). The inverse of a perspectivity is a perspectivity. Thus $T^{-1}$ is a composition of perspectivities mapping $l \to l$. So $T^{-1} \in G_l$.

Therefore, $G_l$ is a group.

#### **2. Matrix Representation**
We can choose a coordinate system on the line $l$.
Since $l$ is a line in $P^2$, it is projectively equivalent to $P^1$.
Points on $l$ can be represented by homogeneous coordinates $(u_1, u_2)$ (parameters on the line).
Alternatively, in $P^2$, we can choose a basis such that $l$ is the line $x_3 = 0$.
Points on $l$ have coordinates of the form $(x_1, x_2, 0)$.

A projectivity on $l$ is induced by a linear transformation of the underlying vector space of $l$ (which is 2-dimensional).
Let the coordinates on $l$ be represented by the vector $u = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$.
Any projectivity $T: l \to l$ corresponds to an invertible $2 \times 2$ matrix $A \in GL(2)$.
$$T([u]) = [Au]$$
where $[u]$ denotes the equivalence class (point in $P^1$).

The matrix representation is the group of invertible $2 \times 2$ matrices, modulo scalar multiples:
$$PGL(2) = GL(2) / \{kI \mid k \neq 0\}$$

**Explicitly in $P^2$ coordinates:**
If we view this as a subgroup of $PGL(3)$ fixing the line $x_3=0$:
The matrix $M$ acting on $P^2$ must map any point $(x_1, x_2, 0)$ to a point $(x'_1, x'_2, 0)$.
$$M \begin{pmatrix} x_1 \\ x_2 \\ 0 \end{pmatrix} = \begin{pmatrix} x'_1 \\ x'_2 \\ 0 \end{pmatrix}$$
This implies the third row of $M$ must be of the form $(0, 0, m_{33})$.
Since it's a projectivity *of* $l$, we are concerned with the action on the first two coordinates.
$$M = \begin{pmatrix} a & b & * \\ c & d & * \\ 0 & 0 & m_{33} \end{pmatrix}$$
Restricting to $l$ (ignoring points off $l$), the action is determined by the submatrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$.
For the restriction to be an isomorphism on $l$, we need $\det \begin{pmatrix} a & b \\ c & d \end{pmatrix} \neq 0$.

Thus, the group is isomorphic to $PGL(2)$.
