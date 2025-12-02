### **Problem Statement**
Let $l$ and $l'$ be distinct lines, and let $C$ be a point not on either line. The perspectivity $[C; l \to l']$ is the mapping $\alpha$ that sends each point $P\in l$ to the intersection of $\overleftrightarrow{PC}$ with $l'$.

*   **i.** Verify that the mapping $\alpha$ is well-defined.
*   **ii.** Verify that $\alpha$ is a bijection with exactly one fixed point.
*   **iii.** Verify that $\alpha^{-1}$ is a perspectivity.
*   **iv.** Show that the composition of two perspectivities need not be a perspectivity.
*   **v.** Given four distinct points $P$, $Q$, $P'$, and $Q'$, prove that there is a unique perspectivity taking $P$ to $P'$ and $Q$ to $Q'$.

---

### **Solution**

#### **i. Well-defined**
Let $P \in l$. Since $C \notin l$, $P \neq C$. Thus, there is a unique line $\overleftrightarrow{PC}$ connecting $P$ and $C$ (Theorem 1.2).
Since $C \notin l'$, the line $\overleftrightarrow{PC}$ is distinct from $l'$ (unless $P$ is the intersection $l \cap l'$, in which case $\overleftrightarrow{PC}$ intersects $l'$ at $P$).
By Theorem 1.1, two distinct lines in $P^2$ intersect at exactly one point.
Thus, $\overleftrightarrow{PC} \cap l'$ consists of a unique point $P'$.
So $\alpha(P) = P'$ is well-defined for all $P \in l$.

#### **ii. Bijection and Fixed Point**
**Injective:** Suppose $\alpha(P_1) = \alpha(P_2) = X'$. Then $X' \in l'$. The line connecting $C$ and $X'$ is unique. Since $P_1$ lies on $\overleftrightarrow{CX'}$ and $l$, and $P_2$ lies on $\overleftrightarrow{CX'}$ and $l$, and $\overleftrightarrow{CX'}$ intersects $l$ at a unique point (since $C \notin l$), $P_1$ must equal $P_2$.
**Surjective:** Let $X' \in l'$. Since $C \notin l'$, $X' \neq C$. The line $\overleftrightarrow{CX'}$ is well-defined. It intersects $l$ at a unique point $P$ (since $C \notin l$). Then $\alpha(P) = X'$.
**Fixed Point:** A point $P$ is fixed if $\alpha(P) = P$, meaning $P \in l'$. Since $P \in l$ by definition, a fixed point must be in $l \cap l'$. Since $l$ and $l'$ are distinct, they intersect at exactly one point $O = l \cap l'$.
$\alpha(O)$: Line $\overleftrightarrow{OC}$ intersects $l'$ at $O$. So $\alpha(O) = O$.
Thus, the intersection $l \cap l'$ is the unique fixed point.

#### **iii. Inverse is a perspectivity**
Let $\alpha: l \to l'$ be $[C; l \to l']$.
The inverse map $\alpha^{-1}: l' \to l$ takes a point $P' \in l'$ to $P \in l$ such that $P, P', C$ are collinear.
This is exactly the definition of the perspectivity $[C; l' \to l]$.
So $\alpha^{-1} = [C; l' \to l]$.

#### **iv. Composition**
Let $\alpha = [C_1; l_1 \to l_2]$ and $\beta = [C_2; l_2 \to l_3]$.
Let $\gamma = \beta \circ \alpha: l_1 \to l_3$.
If $\gamma$ were a perspectivity, lines connecting $P$ and $\gamma(P)$ would all pass through a common center $C$.
Consider $l_1, l_2, l_3$ in general position (forming a triangle).
$\alpha$ fixes $l_1 \cap l_2$. $\beta$ moves $l_1 \cap l_2$ to some point on $l_3$.
The fixed point of a perspectivity $l_1 \to l_3$ must be $l_1 \cap l_3$.
However, generally $\beta(\alpha(l_1 \cap l_3)) \neq l_1 \cap l_3$.
Specifically, if $C_1, C_2$ and $l_1 \cap l_3$ are not collinear in a specific way, the concurrency fails.
A composition of two perspectivities is a **projectivity**, but not necessarily a perspectivity. (Theorem: A projectivity is a perspectivity iff it fixes the intersection of the lines).

#### **v. Unique Perspectivity for 4 points**
Given $P, Q \in l$ and $P', Q' \in l'$.
We want a center $C$ such that $P, P', C$ are collinear and $Q, Q', C$ are collinear.
This implies $C$ must lie on the line $\overleftrightarrow{PP'}$ and on the line $\overleftrightarrow{QQ'}$.
Let $C = \overleftrightarrow{PP'} \cap \overleftrightarrow{QQ'}$.
Since $P, Q, P', Q'$ are distinct and $l \neq l'$, $\overleftrightarrow{PP'}$ and $\overleftrightarrow{QQ'}$ are distinct lines (unless $P, P', Q, Q'$ are all collinear, which is impossible as they are on distinct lines $l, l'$).
Thus $C$ is uniquely determined as the intersection of these two cross-lines.
The perspectivity is $[C; l \to l']$.
**Exception:** If $\overleftrightarrow{PP'} = \overleftrightarrow{QQ'}$, then $P, P', Q, Q'$ are collinear, meaning $l=l'$, which contradicts distinct lines.
**Check:** Does this center $C$ work? Yes, by construction.
Is it unique? Yes, because $C$ *must* lie on $\overleftrightarrow{PP'}$ and $\overleftrightarrow{QQ'}$.
