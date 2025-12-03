### **Problem Statement**
Prove that every projective collineation is of the form $\bar{A}$ for some $A\in GL(3)$.

---

### **Proof**

**Definition:**
A **projective collineation** is defined in **Summary.md** as a transformation of $P^2$ induced by an invertible linear transformation $A$ of $R^3$.
If this is the definition, there is nothing to prove.

However, often "Collineation" is defined as *any bijection preserving collinearity*, and the "Fundamental Theorem of Projective Geometry" states that any such collineation (for dimension $\ge 2$) is a projective collineation (induced by linear map) possibly composed with an automorphism of the field.
Since we are working over $\mathbb{R}$ (implied by $E^3, S^2$ definitions), the only field automorphism is identity.

**Assuming the definition is "Bijection preserving collinearity":**
1.  Let $T: P^2 \to P^2$ be a collineation.
2.  Let $P_1, P_2, P_3, P_4$ be the standard basis points $[1,0,0], [0,1,0], [0,0,1], [1,1,1]$.
3.  Let $Q_i = T(P_i)$. Since $T$ preserves collinearity, $Q_i$ are in general position.
4.  By the Fundamental Theorem of Projective Geometry (Theorem 11), there exists a linear map $A \in GL(3)$ such that $\tilde{A}$ maps $P_i$ to $Q_i$.
5.  Consider $S = \tilde{A}^{-1} \circ T$.
    *   $S$ fixes $P_1, P_2, P_3, P_4$.
    *   $S$ is a collineation.
6.  By **Exercise 15**, a projective collineation fixing 4 points is identity.
    *   But we need to show any *collineation* fixing 4 points is identity (Theorem of Mobius?).
    *   Actually, over $\mathbb{R}$, this is true. (Fundamental Theorem of Projective Geometry).
    *   For the full proof, one constructs the field operations geometrically (Von Staudt algebra) and shows the map preserves addition and multiplication, hence is an automorphism. Since Field is $\mathbb{R}$, it's Identity.
7.  Thus $S = I$, so $T = \tilde{A}$.

**Reference to Summary:**
Summary.md defines "Projective Collineation" as "A transformation ... induced by ... A".
It defines "Collineation" as "A bijection ... that preserves collinearity".
Exercise 17 asks to prove that every *projective collineation* is of the form $\tilde{A}$.
This seems tautological based on the definition in Summary.md line 12:
*"Projective Collineation: A transformation of $P^2$ induced by an invertible linear transformation $A$ of $R^3$."*

**Interpretation:**
Perhaps the question asks to show that the map $\tilde{A}$ is well-defined and is a collineation?
Or maybe it asks to prove Theorem 11? (But Ex 16 covers uniqueness).
Or maybe "Projective Collineation" in the question refers to "Collineation" (bijective + collinearity)?

Given the context of standard textbooks:
The term "Projective Collineation" usually *means* the linear one.
The term "Collineation" means the geometric one.
Theorem: Collineation = Projective Collineation (over Reals).

**Proof Sketch (Fundamental Theorem):**
1.  Let $\alpha$ be a collineation.
2.  Map a basis to a basis using a linear map $A$.
3.  Compose to get $\beta$ fixing the basis.
4.  Show $\beta$ fixes every rational point (by harmonic construction).
5.  By continuity (topology of $\mathbb{R}$), it fixes every real point.
6.  Thus $\alpha$ is linear.

**If the question assumes "Projective Collineation" = "Linear Map induced":**
Then the proof is:
By definition.
If the question asks "Prove that every **Collineation** is projective":
See above.

**Decision:**
I will assume the question asks to justify the matrix representation of a general projective transformation defined geometrically.
Since Summary.md defines it directly, I will point that out and provide the consistency check.

**Answer:**
By definition in the Summary, a projective collineation is induced by $A \in GL(3)$.
If the question implies "Prove that any map preserving cross-ratio / collinearity is linear":
1.  Let $T$ be the map.
2.  Let $T$ map the standard frame to $Q_1, Q_2, Q_3, Q_4$.
3.  There exists $A$ mapping standard frame to $Q_i$.
4.  $T \circ \tilde{A}^{-1}$ fixes the frame.
5.  A map fixing the frame and preserving projective properties must be the identity (Fundamental Theorem of Projective Geometry).
6.  Therefore $T = \tilde{A}$.
