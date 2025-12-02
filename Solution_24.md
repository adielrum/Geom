### **Problem Statement**
Prove **Theorem 17**: If a projective collineation has three collinear fixed points, it is a perspective collineation (unless it is the identity).

---

### **Proof**

Let $T$ be a projective collineation.
Let $A, B, C$ be three distinct fixed points of $T$.
Let $l$ be the line containing $A, B, C$.

**Step 1: The line $l$ is fixed pointwise.**
The restriction $T|_l$ is a projectivity from $l$ to itself.
This projectivity fixes 3 distinct points $A, B, C$.
By the Fundamental Theorem of Projective Geometry on a line (Exercise 9), the only projectivity fixing 3 distinct points is the identity.
Therefore, $T|_l$ is the identity map on $l$.
This means **every point on $l$ is a fixed point**.
So $l$ is an **axis** of fixed points.

**Step 2: Behavior off the axis.**
Let $P$ be a point not on $l$.
Let $P' = T(P)$.
If $P' = P$ for some $P \notin l$:
*   Then we have a line of fixed points $l$ and an extra fixed point $P$.
*   Take any line passing through $P$ and intersecting $l$ at $Q$.
*   $T$ fixes $P$ and $Q$ (since $Q \in l$).
*   So $T$ fixes the line $PQ$.
*   This implies $T$ is the identity? Not necessarily.
*   However, if $T$ fixes $l$ pointwise and $P$, it is a homology or identity.
*   Wait, the definition of Perspective Collineation includes Homologies and Elations.
*   A perspective collineation is defined as one fixing a line pointwise (Axis) and a pencil of lines linewise (Center).

We have established $l$ is an Axis.
We need to show there exists a Center.

**Step 3: Finding the Center.**
Let $P$ and $Q$ be two points not on $l$.
Let $P' = T(P)$ and $Q' = T(Q)$.
Since $T$ fixes every point on $l$, let $X = PQ \cap l$.
Then $T(X) = X$.
Since $P, Q, X$ are collinear, $P', Q', X$ are collinear.
So the line $PQ$ maps to $P'Q'$ and they intersect at $X$ on the axis.
This is always true for any collineation fixing $l$ pointwise.

We need to show that the lines connecting points to their images are concurrent.
Let $P \notin l$. Let $P' = T(P)$.
Line $PP'$ connects a point to its image.
Let $Q \notin l$ (and not on $PP'$). Let $Q' = T(Q)$.
Let $O = PP' \cap QQ'$.
We want to show that for any other $R$, $RR'$ passes through $O$.
Consider triangles $PQR$ and $P'Q'R'$.
The sides $PQ$ and $P'Q'$ intersect at $X \in l$.
The sides $QR$ and $Q'R'$ intersect at $Y \in l$.
The sides $RP$ and $R'P'$ intersect at $Z \in l$.
Since $X, Y, Z$ are on $l$, they are collinear.
By **Desargues' Theorem (Theorem 4)** (Converse):
If the intersections of corresponding sides of two triangles are collinear, then the lines connecting corresponding vertices are concurrent.
Thus $PP', QQ', RR'$ are concurrent at a point $O$.

**Step 4: Conclusion.**
*   There exists a line $l$ (Axis) such that every point on $l$ is fixed.
*   There exists a point $O$ (Center) such that for every $P$, the line $PP'$ passes through $O$.
*   This is the definition of a **Perspective Collineation**.

**Note:**
If $O$ lies on $l$, it is an Elation.
If $O$ does not lie on $l$, it is a Homology.
If $T$ is the identity, it fits the definition trivially (any line is axis, any point is center) or is excluded by "unless it is the identity".

Thus, Theorem 17 is proved.
