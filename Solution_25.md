### **Problem Statement**
Prove **Theorem 18**: When a perspective collineation is represented as in Theorem 17 (Matrix $M = \begin{bmatrix}a&0&0\\ 0&a&q\\ 0&0&1\end{bmatrix}$ with $a\ne0$), it is:
*   **i.** an elation if $a=1$ and $q\ne0$;
*   **ii.** the identity if $a=1$ and $q=0$;
*   **iii.** a homology if $a\ne1$.

---

### **Proof**

**1. Context from Theorem 17**
Theorem 17 states that a projective collineation with three collinear fixed points can be written in the form:
$$M = \begin{bmatrix} a & 0 & 0 \\ 0 & a & q \\ 0 & 0 & 1 \end{bmatrix}$$
*   **Fixed Points:**
    *   The line $x_1=0$ (axis) is fixed pointwise?
        *   Let $X = [0, x_2, x_3]$.
        *   $MX = [0, ax_2 + qx_3, x_3]$.
        *   For $X$ to be fixed pointwise ($MX \sim X$), we need $[0, ax_2+qx_3, x_3] = k[0, x_2, x_3]$.
        *   $x_3 = k x_3 \implies k=1$ (if $x_3 \neq 0$).
        *   $ax_2 + qx_3 = x_2 \implies (a-1)x_2 + qx_3 = 0$.
        *   This must hold for ALL $x_2, x_3$ on the line?
        *   Theorem 17 says "Every point on the line $x_1=0$ is fixed" is NOT generally true for this matrix unless specific conditions met?
        *   Let's re-read Theorem 17 in `Theorems.md`: "Every point on the line $x_1=0$ is fixed."
        *   Let's check: If $x_1=0$ is pointwise fixed, then $(a-1)x_2 + qx_3 = 0$ for all $x_2, x_3$.
        *   This implies $a=1$ and $q=0$.
        *   This contradicts the matrix form having variable $a, q$.
    *   **Correction:** Theorem 17 says "If a projective collineation has three collinear fixed points...".
        *   Maybe the axis is $x_3=0$?
        *   Let's check $x_3=0$: Points $[x_1, x_2, 0]$.
        *   $M[x_1, x_2, 0]^T = [ax_1, ax_2, 0]^T = a[x_1, x_2, 0]^T$.
        *   Yes! **The line $x_3=0$ is fixed pointwise.**
        *   So the **Axis** is $l_\infty$ ($x_3=0$).

*   **Center:**
    *   The center is the point $C$ such that all lines through $C$ are invariant.
    *   Lines through $C$ correspond to eigenvectors of $M^T$ (fixed lines).
    *   $M^T = \begin{bmatrix} a & 0 & 0 \\ 0 & a & 0 \\ 0 & q & 1 \end{bmatrix}$.
    *   Eigenvalues: $a, a, 1$.
    *   Eigenvectors for $a$:
        *   $\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & q & 1-a \end{bmatrix} \begin{bmatrix} u \\ v \\ w \end{bmatrix} = 0$.
        *   $qv + (1-a)w = 0$.
        *   This gives a plane of fixed lines (pencil of lines through Center).
        *   The center $C$ is the intersection of these lines.
        *   The pole of the plane $qv + (1-a)w = 0$ is the point $C = [0, q, 1-a]$? No.
        *   Let's find the center directly.
        *   $C$ is a fixed point.
        *   Fixed points of $M$:
            *   $x_3=0$ (Axis).
            *   Is there another?
            *   $M \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\ a \\ 0 \end{bmatrix} \sim [0,1,0]$. (On axis).
            *   $M \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\ q \\ 1 \end{bmatrix}$. Not fixed unless $q=0$.
            *   Solve $Mv = v$ (since $k=1$ for center off axis? or $k=a$?).
            *   If $k=a$: $ax_1 = ax_1$, $ax_2+qx_3 = ax_2 \implies qx_3=0 \implies x_3=0$ (Axis).
            *   If $k=1$: $ax_1 = x_1 \implies (a-1)x_1=0$.
                *   $ax_2+qx_3 = x_2 \implies (a-1)x_2 + qx_3 = 0$.
                *   $x_3 = x_3$.
            *   If $a \neq 1$: $x_1=0$. Then $(a-1)x_2 = -qx_3$.
                *   $x_2 = \frac{-q}{a-1} x_3$.
                *   Point $C = [0, -q, a-1]$. (Or $[0, q, 1-a]$).
                *   This point is the **Center**.

**2. Classification**

**Case i: $a=1$ and $q \neq 0$**
*   Matrix $M = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & q \\ 0 & 0 & 1 \end{bmatrix}$.
*   Axis: $x_3=0$.
*   Center:
    *   Solve $Mv = v$ (since $a=1$).
    *   $x_1=x_1$, $x_2+qx_3=x_2 \implies qx_3=0 \implies x_3=0$.
    *   The only fixed points are on the axis $x_3=0$.
    *   This means the Center must lie on the Axis.
    *   Where is the center?
    *   Consider lines. $M^T = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & q & 1 \end{bmatrix}$.
    *   Eigenvectors for $\lambda=1$:
        *   $\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & q & 0 \end{bmatrix} v = 0 \implies qv = 0 \implies v=0$.
        *   So $x_2$ component of line is 0. Line $[u, 0, w]$.
        *   Equation $ux_1 + wx_3 = 0$.
        *   These lines all pass through $[0, 1, 0]$.
    *   So Center $C = [0, 1, 0]$.
*   Does $C=[0,1,0]$ lie on Axis $x_3=0$?
    *   Yes.
*   Center on Axis $\implies$ **Elation**.

**Case ii: $a=1$ and $q=0$**
*   Matrix $M = I$.
*   **Identity**.

**Case iii: $a \neq 1$**
*   Center $C = [0, q, 1-a]$ (from derivation above).
*   Axis $x_3=0$.
*   Does $C$ lie on Axis?
    *   $x_3$-coordinate of $C$ is $1-a$.
    *   Since $a \neq 1$, $1-a \neq 0$.
    *   So $C \notin$ Axis.
*   Center not on Axis $\implies$ **Homology**.

**Conclusion:**
Theorem 18 is proved.
