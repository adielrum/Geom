### **Problem Statement**
Let $x=(1,0,0)$, $y=(1,1,0)$, $z=(1,0,1)$, $w=(1,1,1).$ Let $l$ be the line joining $x$ and $y$, and let $m$ be the line joining $z$ and $w$. Find $l\cap m$.

---

### **Solution**

**1. Find the pole of line $l$**
The line $l$ joins $x$ and $y$. The pole of $l$, denoted $\xi_l$, is given by the cross product $x \times y$.
$$x = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \quad y = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}$$

$$\xi_l = x \times y = \begin{vmatrix} e_1 & e_2 & e_3 \\ 1 & 0 & 0 \\ 1 & 1 & 0 \end{vmatrix} = (0)(0) - (0)(1) e_1 - ((1)(0) - (0)(1)) e_2 + ((1)(1) - (0)(1)) e_3$$
$$\xi_l = 0e_1 - 0e_2 + 1e_3 = \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}$$

**2. Find the pole of line $m$**
The line $m$ joins $z$ and $w$. The pole of $m$, denoted $\xi_m$, is given by the cross product $z \times w$.
$$z = \begin{pmatrix} 1 \\ 0 \\ 1 \end{pmatrix}, \quad w = \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$$

$$\xi_m = z \times w = \begin{vmatrix} e_1 & e_2 & e_3 \\ 1 & 0 & 1 \\ 1 & 1 & 1 \end{vmatrix}$$
$$= ((0)(1) - (1)(1)) e_1 - ((1)(1) - (1)(1)) e_2 + ((1)(1) - (0)(1)) e_3$$
$$= -1e_1 - 0e_2 + 1e_3 = \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix}$$

**3. Find the intersection $l \cap m$**
The intersection point $P$ of two lines with poles $\xi_l$ and $\xi_m$ is given by the cross product of their poles: $P = \xi_l \times \xi_m$.

$$P = \xi_l \times \xi_m = \begin{vmatrix} e_1 & e_2 & e_3 \\ 0 & 0 & 1 \\ -1 & 0 & 1 \end{vmatrix}$$
$$= ((0)(1) - (1)(0)) e_1 - ((0)(1) - (1)(-1)) e_2 + ((0)(0) - (0)(-1)) e_3$$
$$= 0e_1 - (0 - (-1)) e_2 + 0e_3$$
$$= 0e_1 - 1e_2 + 0e_3 = \begin{pmatrix} 0 \\ -1 \\ 0 \end{pmatrix}$$

**4. Homogeneous Coordinates**
The vector $(0, -1, 0)$ represents the same point as $(0, 1, 0)$ in $P^2$.

**Answer:**
The intersection point is $l \cap m = (0, 1, 0)$.
