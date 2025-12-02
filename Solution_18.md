### **Problem Statement**
The fixed lines of a projective collineation $\tilde{A}$ can be found by computing the eigenvectors of $A^{t}$. Justify this statement and use it to prove Theorem 12.

---

### **Solution**

#### **1. Justification**
Let $\tilde{A}$ be a projective collineation induced by $A \in GL(3)$.
A line $l$ in $P^2$ is represented by a pole vector $\xi \in R^3$ (where $l = \{x \mid \xi^t x = 0\}$).
We want to find when the line $l$ is invariant under $\tilde{A}$.
The image of a point $x$ is $Ax$.
The line $l$ is invariant if for every $x \in l$, $Ax \in l$.
$x \in l \iff \xi^t x = 0$.
$Ax \in l \iff \xi^t (Ax) = 0$.
So, $\xi^t x = 0 \implies (\xi^t A) x = 0$.
This implies that the linear functional $\xi^t A$ must be proportional to $\xi^t$.
$\xi^t A = \lambda \xi^t$ for some scalar $\lambda$.
Taking the transpose:
$A^t \xi = \lambda \xi$.

Thus, the pole $\xi$ of a fixed line must be an eigenvector of $A^t$.

#### **2. Proof of Theorem 12**
**Theorem 12:** Every projective collineation has at least one fixed point and one fixed line.

**Proof:**
Let $A$ be the $3 \times 3$ matrix representing the collineation (over $\mathbb{R}$ or $\mathbb{C}$).

**Case 1: Field is $\mathbb{C}$ (Algebraically Closed)**
The characteristic polynomial of $A$, $p(\lambda) = \det(A - \lambda I)$, is of degree 3.
It always has at least one root $\lambda_1$.
Thus $A$ has at least one eigenvector $v_1$.
$\implies$ There is at least one fixed point $P = [v_1]$.

Similarly, the characteristic polynomial of $A^t$ is the same.
It has at least one root $\mu_1$.
Thus $A^t$ has at least one eigenvector $\xi_1$.
$\implies$ There is at least one fixed line $l = [\xi_1]$.

**Case 2: Field is $\mathbb{R}$**
The characteristic polynomial is a cubic with real coefficients.
Every cubic polynomial with real coefficients has at least one real root (Intermediate Value Theorem, limits are $\pm \infty$).
Let $\lambda_1$ be this real root.
Then there exists a real eigenvector $v_1$ for $A$.
$\implies$ At least one fixed point.

Since $A$ and $A^t$ have the same eigenvalues, $A^t$ also has a real eigenvalue $\lambda_1$.
Then there exists a real eigenvector $\xi_1$ for $A^t$.
$\implies$ At least one fixed line.

**Conclusion:**
Every projective collineation has at least one fixed point and one fixed line.
