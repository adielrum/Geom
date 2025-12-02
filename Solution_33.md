### **Problem Statement**
Let $\tilde{b}$ be a polarity, and let $l$ be a non-self-conjugate line. For each $X\in l$, let $\alpha(X)$ be the point where the polar line of $X$ intersects $l$. Prove that $\alpha$ is a projectivity. Show further that $\alpha^{2}=I$, that is, $\alpha$ is an involution.

---

### **Proof**

**1. Setup**
*   Let $\pi: P^2 \to (P^2)^*$ be the polarity map sending a point $X$ to its polar line $X^\perp$.
*   The map $\pi$ is a projective correlation (linear map from $V$ to $V^*$).
*   Let $l$ be a line.
*   For $X \in l$, $\alpha(X) = X^\perp \cap l$.

**2. $\alpha$ is a Projectivity**
*   The map $X \mapsto X^\perp$ is a projective map from points to lines.
*   The intersection with a fixed line $l$ ($L \mapsto L \cap l$) is a projective map from lines to points (on $l$).
*   The composition $\alpha$ is a map from points on $l$ to points on $l$.
*   Since it is a composition of projective maps (linear operations), $\alpha$ is a projectivity.

**3. $\alpha$ is an Involution ($\alpha^2 = I$)**
*   Let $Y = \alpha(X)$.
*   By definition, $Y = X^\perp \cap l$.
*   This implies $Y$ lies on the polar line of $X$.
*   By the **Reciprocity Theorem (Theorem 21)**: If $Y$ lies on the polar line of $X$, then $X$ lies on the polar line of $Y$.
*   So $X \in Y^\perp$.
*   Also, $X \in l$ (by definition of domain).
*   Therefore, $X = Y^\perp \cap l$.
*   This means $\alpha(Y) = X$.
*   Substituting $Y = \alpha(X)$, we get $\alpha(\alpha(X)) = X$.
*   So $\alpha^2 = I$.

**Conclusion:**
$\alpha$ is an involution on the line $l$.
(The fixed points of this involution are the intersection points of the conic with $l$, if any).
