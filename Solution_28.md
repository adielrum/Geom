### **Problem Statement**
(Sub-problems regarding Theorem 18):
*   **i.** Verify the remarks following Theorem 18.
*   **ii.** Show that the harmonic homologies are those having $a=-1$ and $q=0$ in Theorem 18.
*   **iii.** Prove that the only projective collineations that are involutions are the harmonic homologies.

---

### **Solution**

**i. Verify remarks following Theorem 18**
Theorem 18 (proven in Ex 25) classifies the matrix $M = \begin{bmatrix} a & 0 & 0 \\ 0 & a & q \\ 0 & 0 & 1 \end{bmatrix}$.
*   $a=1, q \neq 0 \implies$ Elation.
*   $a=1, q=0 \implies$ Identity.
*   $a \neq 1 \implies$ Homology.

Remarks following Theorem 18 usually discuss the geometric properties:
*   **Elation:** Center on Axis. No other fixed points/lines.
*   **Homology:** Center not on Axis. Axis and Center are fixed. Lines through Center are fixed.
    *   Center $C = [0, -q, a-1]$. Axis $x_3=0$.
    *   If $a \neq 1$, $C$ is distinct from Axis.
    *   Cross ratio of $(C, M, P, P')$ is constant.

**ii. Harmonic Homologies ($a=-1, q=0$)**
A **Harmonic Homology** is an involution ($T^2 = I$) that is not the identity.
Let's check the condition $a=-1, q=0$.
$M = \begin{bmatrix} -1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$.
$M^2 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} = I$.
So $T^2 = I$.
Since $a=-1 \neq 1$, it is a Homology.
Center $C = [0, 0, -2] = [0,0,1]$.
Axis $x_3=0$.
For any point $P=[x_1, x_2, x_3]$, $P'=[-x_1, -x_2, x_3]$.
Collinear points $C, P, P'$:
$P' = [-x_1, -x_2, x_3]$. $P = [x_1, x_2, x_3]$. $C = [0,0,1]$.
$P' = -P + 2x_3 C$.
This confirms $P, P', C$ are collinear.
Cross Ratio $(C, X, P, P')$ where $X$ is intersection of $CP$ with Axis ($x_3=0$).
$X = [x_1, x_2, 0]$.
$P = X + x_3 C$.
$P' = -X + x_3 C$.
Coordinate on line $CP$ (basis $X, C$):
$X \to 0$ (pos 0).
$C \to \infty$ (pos 1).
$P \to 1$ (coeff of C / coeff of X? No).
Let's use parameters: $P = 1 \cdot X + x_3 \cdot C$. Parameter $\lambda = x_3$.
$P' = -1 \cdot X + x_3 \cdot C$. Parameter $\lambda' = -x_3$.
Cross ratio $(C, X, P, P') = (\infty, 0, x_3, -x_3) = \frac{x_3 - 0}{x_3 - \infty} / \frac{-x_3 - 0}{-x_3 - \infty} = -1$.
So it is indeed Harmonic.

**iii. Involutions are Harmonic Homologies**
We want to find all $M$ such that $M^2 = kI$.
From Theorem 16/17, we can put any collineation with fixed points into canonical form.
If $T^2=I$, then eigenvalues satisfy $\lambda^2 = k$.
In $\mathbb{R}$, $\lambda = \pm \sqrt{k}$.
If $k=1$, $\lambda = \pm 1$.
Possible Jordan forms:
1.  $\lambda = 1, 1, 1$. $M \sim I$ (Identity).
2.  $\lambda = 1, 1, -1$. $M \sim \text{diag}(1, 1, -1)$.
    *   This is exactly the form of Harmonic Homology ($a=1, a=1, 1=-1$? No).
    *   Our canonical form was $\text{diag}(a, a, 1)$.
    *   If $a=-1$, we get $\text{diag}(-1, -1, 1)$.
    *   This corresponds to eigenvalues $-1, -1, 1$.
    *   This is the Harmonic Homology.
3.  $\lambda = 1, -1, -1$. $M \sim \text{diag}(1, -1, -1)$.
    *   Equivalent to $\text{diag}(-1, 1, 1)$ (multiply by -1).
    *   Same as case 2.
4.  What about Elations?
    *   $M = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & q \\ 0 & 0 & 1 \end{bmatrix}$.
    *   $M^2 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 2q \\ 0 & 0 & 1 \end{bmatrix}$.
    *   $M^2 \sim I \implies 2q = 0 \implies q=0$.
    *   So Elations are not involutions (unless identity).

**Conclusion:**
The only non-identity involutions are Harmonic Homologies.
