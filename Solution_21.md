### **Problem Statement**
Prove **Theorem 14**: Suppose that $P$ lies on $l$. Then every projective collineation leaving $P$ and $l$ fixed is uniquely represented by a matrix of the form $\begin{bmatrix}a&b&p\\ 0&c&q\\ 0&0&1\end{bmatrix}$ where $ac\ne0$. Conversely, each such matrix determines a projective collineation leaving $P$ and $l$ fixed.

---

### **Proof**

**1. Choice of Coordinates**
Let $P$ be a point on line $l$.
Choose a basis such that:
*   $P = [1, 0, 0]$ (Point on $x_1$ axis).
*   $l$ is the line $x_2 = 0$ (The line $x_1x_3$-plane? No, $x_2=0$ contains $[1,0,0]$ and $[0,0,1]$).
    *   Let's check: $P=[1,0,0]$ satisfies $x_2=0$. Yes.
    *   Wait, usually we choose $l$ to be $x_3=0$ (line at infinity).
    *   If $l$ is $x_3=0$, and $P \in l$, then $P$ could be $[1, 0, 0]$.
    *   Let's stick to the form in the theorem. The matrix form suggests specific coordinates.
    *   The matrix fixes $[0,0,1]$?
        *   $M [0,0,1]^T = [p, q, 1]^T$. This is NOT fixed unless $p=q=0$.
    *   The matrix fixes $[1,0,0]$?
        *   $M [1,0,0]^T = [a, 0, 0]^T = a[1,0,0]^T$. Fixed!
    *   So **$P$ corresponds to $[1, 0, 0]$**.

    *   Does it fix the line $x_3=0$?
        *   Points $[x, y, 0]$. Image: $[ax+by, cy, 0]$. $x_3$ component is 0.
        *   So the line $x_3=0$ is fixed.
    *   Does $P=[1,0,0]$ lie on $x_3=0$? Yes.
    *   So the setup is: $P=[1,0,0]$ and $l$ is the line $x_3=0$.

**2. Derivation**
Let $M = \begin{bmatrix} m_{11} & m_{12} & m_{13} \\ m_{21} & m_{22} & m_{23} \\ m_{31} & m_{32} & m_{33} \end{bmatrix}$.

**Condition 1: $l$ ($x_3=0$) is fixed.**
For any $[x_1, x_2, 0]$, the image must have $x'_3 = 0$.
$x'_3 = m_{31}x_1 + m_{32}x_2 + m_{33}(0) = 0$ for all $x_1, x_2$.
$\implies m_{31} = 0, m_{32} = 0$.

**Condition 2: $P$ ($[1,0,0]$) is fixed.**
$M \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} = \begin{bmatrix} m_{11} \\ m_{21} \\ 0 \end{bmatrix} = k \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}$.
$\implies m_{21} = 0$.
(And $m_{11} \neq 0$ for invertibility/non-zero image).

So far:
$$M = \begin{bmatrix} m_{11} & m_{12} & m_{13} \\ 0 & m_{22} & m_{23} \\ 0 & 0 & m_{33} \end{bmatrix}$$

**3. Normalization**
Since it's a projective transformation, we can scale the matrix.
Assume $m_{33} \neq 0$. (If $m_{33}=0$, then $\det(M) = m_{11}m_{22} \cdot 0 = 0$, singular).
Divide by $m_{33}$. Set $m_{33} = 1$.
Let $a = m_{11}, b = m_{12}, p = m_{13}$.
Let $c = m_{22}, q = m_{23}$.
(Note: $m_{21}$ is already 0).

$$M = \begin{bmatrix} a & b & p \\ 0 & c & q \\ 0 & 0 & 1 \end{bmatrix}$$

**4. Invertibility**
$\det(M) = a \cdot c \cdot 1 = ac$.
For $M$ to be invertible, we need $ac \neq 0$.

**5. Converse**
If $M$ is of this form with $ac \neq 0$:
*   $M[1,0,0]^T = [a, 0, 0]^T \sim [1,0,0]$. $P$ is fixed.
*   $M[x, y, 0]^T = [ax+by, cy, 0]^T$. The third coordinate is 0. So $l$ is fixed.
*   $\det \neq 0$, so it is a valid projective collineation.

**Conclusion:**
Theorem 14 is proved.
