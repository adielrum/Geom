### **I. Fundamental Definitions & Concepts**

* **The Projective Plane ($P^2$):** Defined as the set of all pairs $\{x, -x\}$ of antipodal points of the sphere $S^2$.
    * *Alternative Definition 1:* The set of all lines through the origin in $E^3$.
    * *Alternative Definition 2:* The set of equivalence classes of ordered triples $(x_1, x_2, x_3) \neq (0,0,0)$, where two vectors are equivalent if they are proportional.
* **The Map $\pi$:** The mapping $\pi: S^2 \to P^2$ sends each $x$ to the pair $\{x, -x\}$.
* **Line in $P^2$:** A set of the form $\pi l$, where $l$ is a line of $S^2$ (a great circle). If $\xi$ is a pole of $l$, then $\pi\xi$ is called the **pole** of the line $\pi l$.
* **Incidence Condition:** A point $\pi x$ lies on the line with pole $\pi \xi$ if and only if the inner product $\langle \xi, x \rangle = 0$.
* **Homogeneous Coordinates:** If $\{e_1, e_2, e_3\}$ is a basis of $R^3$, any vector $x \in R^3$ determines a triple $(x_1, x_2, x_3)$ such that $x = x_1e_1 + x_2e_2 + x_3e_3$. If $\pi x \in P^2$, the triple $(u_1, u_2, u_3)$ is a homogeneous coordinate vector of $\pi x$ if $\lambda x = u_1e_1 + u_2e_2 + u_3e_3$ for some $\lambda \neq 0$.
* **Line at Infinity ($l_\infty$):** When modeling $E^2$ inside $P^2$, the line $x_3 = 0$ corresponds to the "line at infinity" which contains the points corresponding to parallel directions in $E^2$.
* **Collineation:** A bijection $T: P^2 \to P^2$ that preserves collinearity.
* **Projective Collineation:** A transformation of $P^2$ induced by an invertible linear transformation $A$ of $R^3$. If $y = Ax$, then the induced map is $\tilde{A}\pi x = \pi Ax$.
* **PGL(2):** The group of all projective collineations of $P^2$. It is isomorphic to the quotient group $GL(3) / \{kI | k \neq 0\}$.
* **Perspective Collineation:** A projective collineation that fixes every point on a specific line (the **axis**) and fixes every line through a specific point (the **center**).
    * **Elation:** A perspective collineation where the center lies on the axis.
    * **Homology:** A perspective collineation where the center does not lie on the axis.
* **Polarity:** A relation determined by a symmetric, nondegenerate bilinear form $b(x, y)$ on $R^3$. Points $\pi x$ and $\pi y$ are **conjugate** if $b(x, y) = 0$.
* **Conic:** The set of self-conjugate points of a polarity ($\pi x$ such that $b(x, x) = 0$).

---

### **II. Important Theorems**

**Incidence Properties**
* **Theorem 1:**
    1.  Two lines of $P^2$ have exactly one point of intersection.
    2.  Two points of $P^2$ lie on exactly one line.

**Coordinates and Bases**
* **Theorem 2 (Fundamental Theorem of Coordinates):** If $P, Q, R, S$ are four points in $P^2$, no three of which are collinear, there exists a basis of $R^3$ such that their coordinates are $(1,0,0), (0,1,0), (0,0,1)$, and $(1,1,1)$ respectively.
* **Theorem 3:** If $x$ and $y$ are homogeneous coordinate vectors for two points, then $\lambda x + \mu y$ represents a typical point on the line connecting them.

**Classical Theorems**
* **Theorem 4 (Desargues' Theorem):** If two triangles $PQR$ and $P'Q'R'$ are perspective from a point (the lines connecting corresponding vertices are concurrent), then they are perspective from a line (the intersections of corresponding sides are collinear).
* **Theorem 5 (Pappus' Theorem):** If $A_1B_1C_1$ and $A_2B_2C_2$ are collinear triples of points, then the cross-intersection points $A_1B_2 \cap A_2B_1$, $B_1C_2 \cap B_2C_1$, and $A_1C_2 \cap A_2C_1$ are collinear.

**Projective Transformations**
* **Theorem 11 (Fundamental Theorem of Projective Geometry):** Given two quadrangles (sets of 4 points, no 3 collinear) $PQRS$ and $P'Q'R'S'$, there is a unique projective collineation $T$ such that $TP=P', TQ=Q', TR=R', TS=S'$.
* **Theorem 12:** Every projective collineation has at least one fixed point and one fixed line.
* **Theorem 17:** If a projective collineation has three collinear fixed points, it is a perspective collineation (unless it is the identity).

**Polarities and Conics**
* **Theorem 21 (Reciprocity):** If point $P$ lies on the polar line of $Q$, then $Q$ lies on the polar line of $P$.
* **Theorem 23:** A line contains exactly one self-conjugate point if and only if the line itself is self-conjugate (tangent to the conic).
* **Corollary:** A line meets a conic in at most two points.

---

### **III. Formulas and Matrix Representations**

**Line Equation from Pole**
If $\xi = (\xi_1, \xi_2, \xi_3)$ is the pole, the line consists of points $x$ satisfying:
$$\xi_1x_1 + \xi_2x_2 + \xi_3x_3 = 0$$

**Homogeneous to Euclidean Conversion**
To map a point $(x_1, x_2, x_3)$ in $P^2$ to $E^2$ (assuming $x_3 \neq 0$):
$$\left( \frac{x_1}{x_3}, \frac{x_2}{x_3} \right)$$

**Cross Product for Incidence**
* **Line joining two points:** If points correspond to vectors $x$ and $y$, the pole of the line joining them is $x \times y$.
* **Intersection of two lines:** If lines have poles $\xi$ and $\eta$, their intersection point corresponds to the vector $\xi \times \eta$.

**Polarity Condition**
A point represented by vector $x$ is on the conic defined by matrix $B$ if:
$$x^t B x = 0$$
Examples:
* **Unit Circle:** $B = \text{diag}(1, 1, -1) \implies x_1^2 + x_2^2 - x_3^2 = 0$.
* **Parabola ($x_2^2 = 4x_1$):** $B = \begin{bmatrix} 0 & 0 & -2 \\ 0 & 1 & 0 \\ -2 & 0 & 0 \end{bmatrix}$.

---

### **IV. Useful Information for Problem Solving**

1.  **Linearizing Problems:**
    Many geometric problems regarding intersection and collinearity in $P^2$ can be solved using linear algebra in $R^3$.
    * To show points $P, Q, R$ are collinear, show their representative vectors $u, v, w$ are linearly dependent ($\det(u,v,w) = 0$).
    * To show lines are concurrent, show their poles are linearly dependent.

2.  **Using the "Line at Infinity":**
    When solving problems involving parallelism in Euclidean geometry ($E^2$), map the problem to $P^2$.
    * Two lines are parallel in $E^2$ if and only if they intersect on the line at infinity ($l_\infty$, where $x_3=0$) in $P^2$.
    * A parallelogram in $E^2$ is a quadrilateral in $P^2$ where two pairs of sides meet on $l_\infty$.

3.  **Simplifying via Basis Choice:**
    Use **Theorem 2** to simplify coordinates. If a problem involves a general quadrangle, you can assume without loss of generality that the points are $(1,0,0), (0,1,0), (0,0,1)$, and $(1,1,1)$. This often drastically reduces algebraic complexity.

4.  **Duality:**
    In $P^2$, statements about points and lines are dual.
    * Points $\leftrightarrow$ Lines.
    * Collinear $\leftrightarrow$ Concurrent.
    * Intersection of lines $\leftrightarrow$ Line joining points.
    If you prove a theorem, the dual theorem is also true.

5.  **Distinguishing Elations and Homologies:**
    When classifying a perspective collineation $T$:
    * It is an **Elation** if the center $P$ lies on the axis $l$ (trace properties or geometric configuration will show incidence).
    * It is a **Homology** if the center $P$ does not lie on the axis $l$.

6.  **Calculating Lines and Points:**
    * To find the line through two points $u$ and $v$, calculate the cross product $u \times v$. The result is the pole of the line.
    * To find the intersection of two lines with poles $\xi$ and $\eta$, calculate $\xi \times \eta$. The result is the vector for the point.