### **Problem Statement**
Prove **Theorem 13**: If $P$ does not lie on $l$, the group of projective collineations leaving $P$ and $l$ fixed is isomorphic to $GL(2)$. Each such collineation can be uniquely written in the form $\begin{bmatrix}a&b&0\\ c&d&0\\ 0&0&1\end{bmatrix}$ where $ad-bc\ne0$.

---

### **Proof**

**1. Choice of Coordinates**
Let $P$ be a point and $l$ be a line such that $P \notin l$.
By the Fundamental Theorem of Coordinates (Theorem 2), we can choose a basis for $R^3$ such that:
*   $P$ has coordinates $[0, 0, 1]$ (the origin of the affine plane $x_3=1$).
*   $l$ is the line $x_3 = 0$ (the line at infinity).

**2. Matrix Representation**
Let $T$ be a projective collineation fixing $P$ and $l$.
Let $M$ be the $3 \times 3$ matrix representing $T$.
$$M = \begin{bmatrix} m_{11} & m_{12} & m_{13} \\ m_{21} & m_{22} & m_{23} \\ m_{31} & m_{32} & m_{33} \end{bmatrix}$$

**Condition 1: $l$ is fixed ($x_3 = 0$ maps to $x_3 = 0$)**
The line $l$ consists of points $[x_1, x_2, 0]$.
$T([x_1, x_2, 0]) = [x'_1, x'_2, x'_3]$.
We require $x'_3 = 0$ for all $x_1, x_2$.
$$x'_3 = m_{31}x_1 + m_{32}x_2 + m_{33}(0) = m_{31}x_1 + m_{32}x_2$$
For this to be 0 for all $x_1, x_2$, we must have:
$$m_{31} = 0$$
$$m_{32} = 0$$

So $M$ looks like:
$$M = \begin{bmatrix} m_{11} & m_{12} & m_{13} \\ m_{21} & m_{22} & m_{23} \\ 0 & 0 & m_{33} \end{bmatrix}$$

**Condition 2: $P$ is fixed ($P=[0,0,1]$ maps to $P$)**
$$M \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix} = \begin{bmatrix} m_{13} \\ m_{23} \\ m_{33} \end{bmatrix}$$
For this to be proportional to $[0, 0, 1]$, we must have:
$$m_{13} = 0$$
$$m_{23} = 0$$
$$m_{33} \neq 0$$ (otherwise the point is mapped to 0 vector)

So $M$ simplifies to:
$$M = \begin{bmatrix} m_{11} & m_{12} & 0 \\ m_{21} & m_{22} & 0 \\ 0 & 0 & m_{33} \end{bmatrix}$$

**3. Normalization and Isomorphism**
Since $M$ is a projective transformation, it is defined up to a scalar factor.
We can divide the entire matrix by $m_{33}$ (since $m_{33} \neq 0$).
Let $a = m_{11}/m_{33}$, $b = m_{12}/m_{33}$, $c = m_{21}/m_{33}$, $d = m_{22}/m_{33}$.
Then $M$ is equivalent to:
$$M' = \begin{bmatrix} a & b & 0 \\ c & d & 0 \\ 0 & 0 & 1 \end{bmatrix}$$

For $M$ to be invertible ($\det(M) \neq 0$), we need:
$$\det(M') = (ad - bc) \cdot 1 \neq 0 \implies ad - bc \neq 0$$

**4. Group Isomorphism**
The set of such matrices forms a group under multiplication.
$$\begin{bmatrix} a & b & 0 \\ c & d & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} a' & b' & 0 \\ c' & d' & 0 \\ 0 & 0 & 1 \end{bmatrix} = \begin{bmatrix} AA' & 0 \\ 0 & 1 \end{bmatrix}$$
The multiplication of the top-left $2 \times 2$ block is exactly the multiplication in $GL(2)$.
The map $\phi: G \to GL(2)$ defined by mapping the $3 \times 3$ matrix to the $2 \times 2$ block $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ is a homomorphism.
It is bijective (inverse map constructs the $3 \times 3$ matrix).
Thus, the group is isomorphic to $GL(2)$.

**Conclusion:**
Theorem 13 is proved.
