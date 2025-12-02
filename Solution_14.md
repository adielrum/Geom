### **Problem Statement**
Classify the projectivities of a given line $l$ in terms of their fixed point behavior.

---

### **Solution**

A projectivity $T: l \to l$ corresponds to a matrix $A \in PGL(2)$.
The fixed points of $T$ correspond to the eigenvectors of $A$.
$A \mathbf{x} = \lambda \mathbf{x}$.
Since $A$ is a $2 \times 2$ matrix, the characteristic equation $\det(A - \lambda I) = 0$ is a quadratic equation in $\lambda$.
$$\lambda^2 - \text{tr}(A)\lambda + \det(A) = 0$$

The discriminant $\Delta = (\text{tr}(A))^2 - 4\det(A)$ determines the nature of the roots (eigenvalues).

**Classification:**

1.  **Two Distinct Fixed Points (Hyperbolic Projectivity)**
    *   **Condition:** $\Delta \neq 0$ (and roots are in the base field).
    *   There are two distinct eigenvalues $\lambda_1, \lambda_2$.
    *   There are two distinct eigenvectors, hence two distinct fixed points on $l$.
    *   **Canonical Form:** Matrix is diagonalizable $\begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$.
    *   Transformation: $x' = kx$ (in non-homogeneous coordinate $x$ with fixed points $0, \infty$).

2.  **One Double Fixed Point (Parabolic Projectivity)**
    *   **Condition:** $\Delta = 0$ (and not the identity).
    *   There is one repeated eigenvalue $\lambda$.
    *   There is only one independent eigenvector (matrix is not diagonalizable, Jordan block).
    *   There is exactly one fixed point on $l$.
    *   **Canonical Form:** $\begin{pmatrix} \lambda & 1 \\ 0 & \lambda \end{pmatrix}$.
    *   Transformation: $x' = x + c$ (translation in affine coordinate).

3.  **No Fixed Points (Elliptic Projectivity)**
    *   **Condition:** $\Delta \neq 0$ but roots are not in the base field (e.g., complex roots for real projective line).
    *   If we are working over $\mathbb{C}$, this case doesn't exist (always 2 or 1).
    *   Over $\mathbb{R}$, if $\Delta < 0$, there are no real eigenvalues.
    *   The transformation rotates the line (like a rotation of the sphere).

4.  **Identity (Every point is fixed)**
    *   **Condition:** $A = kI$.
    *   Every vector is an eigenvector.
    *   Infinite fixed points.

**Summary for Real Projective Line:**
*   **Hyperbolic:** 2 fixed points.
*   **Parabolic:** 1 fixed point.
*   **Elliptic:** 0 fixed points.
*   **Identity:** All points fixed.
