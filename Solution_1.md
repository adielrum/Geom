### **Proof Objective**
Prove **Theorem 3**: If $x$ and $y$ are homogeneous coordinate vectors for two points, then $\lambda x + \mu y$ represents a typical point on the line connecting them.

---

### **Proof**

**1. Definition of Line in $P^2$**
From **Summary.md**, a line in $P^2$ is defined as a set of the form $\pi l$, where $l$ is a line of $S^2$ (a great circle). Alternatively, it is the set of all lines through the origin in $E^3$ that lie in a plane through the origin.

**2. Vector Representation**
Let the two distinct points in $P^2$ be $P$ and $Q$.
Let $x \in R^3$ be a homogeneous coordinate vector for $P$ ($x \neq 0$).
Let $y \in R^3$ be a homogeneous coordinate vector for $Q$ ($y \neq 0$).

Since $P$ and $Q$ are distinct points in $P^2$, the vectors $x$ and $y$ are linearly independent in $R^3$.

**3. Plane Spanned by $x$ and $y$**
The vectors $x$ and $y$ span a 2-dimensional subspace (a plane) $W$ in $R^3$ passing through the origin.
$$W = \{ \lambda x + \mu y \mid \lambda, \mu \in R \}$$

**4. Correspondence to Line in $P^2$**
The line connecting $P$ and $Q$ in $P^2$ corresponds to the set of all 1-dimensional subspaces (lines through the origin) contained in $W$.

Any non-zero vector $z \in W$ is of the form $z = \lambda x + \mu y$ for some scalars $\lambda, \mu$, not both zero.
The point $\pi z$ in $P^2$ represented by $z$ lies on the line connecting $P$ and $Q$.

**5. Conclusion**
Thus, any point on the line connecting the points represented by $x$ and $y$ has a homogeneous coordinate vector of the form $\lambda x + \mu y$. Conversely, any vector of this form (provided it is not the zero vector) represents a point on that line.

This proves Theorem 3.
