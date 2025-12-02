### **Problem Statement**
Let $A$, $B$, $C$, and $D$ be four collinear points. Show that there is a unique projectivity that interchanges $A$ and $B$ and also interchanges $C$ and $D$.

---

### **Proof**

**1. Objective**
We seek a projectivity $T: l \to l$ such that:
$T(A) = B$
$T(B) = A$
$T(C) = D$
$T(D) = C$

**2. Degrees of Freedom**
A projectivity on a line is uniquely determined by the images of **3 distinct points** (Exercise 9).
Here we have conditions on 4 points. This system is overdetermined. We must show that the unique projectivity determined by the first 3 conditions *automatically* satisfies the fourth condition? No, that's not generally true.
Wait, the problem asks to show there *is* a unique projectivity. This implies such a projectivity exists for *any* 4 points?
**Correction:** The problem likely implies $A, B, C, D$ are distinct.
If we specify $A \to B, B \to A, C \to D$, that is 3 conditions.
By Exercise 9, there is a **unique** projectivity $T$ satisfying these 3 conditions.
The question is: Does this unique $T$ necessarily satisfy $T(D) = C$?

**3. Involution Property**
Let $T$ be the unique projectivity defined by:
$T(A) = B$
$T(B) = A$
$T(C) = D$

Consider $T^2 = T \circ T$.
$T^2(A) = T(B) = A$
$T^2(B) = T(A) = B$
$T^2(C) = T(D)$

If $T^2$ fixes 3 points, it is the identity.
We know $T^2$ fixes $A$ and $B$.
Does it fix $C$?
$T^2(C) = T(D)$.
If we *require* $T(D) = C$, then $T^2(C) = C$.
In that case, $T^2$ fixes $A, B, C$, so $T^2 = I$.
So $T$ must be an **involution**.

**4. Existence of Involution swapping pairs**
Is there always an involution swapping $A, B$ and $C, D$?
Let's use coordinates.
$A = \infty$ (1,0)
$B = 0$ (0,1)
$C = 1$ (1,1)
$D = k$ (k,1)

We want $T$ such that:
$T(\infty) = 0$
$T(0) = \infty$
$T(1) = k$
$T(k) = 1$

General form of projectivity $T(z) = \frac{az+b}{cz+d}$.
$T(\infty) = a/c = 0 \implies a = 0$.
$T(0) = b/d = \infty \implies d = 0$.
So $T(z) = \frac{b}{cz} = \frac{\lambda}{z}$.
Now check the other conditions:
$T(1) = \lambda/1 = \lambda$. We want $T(1) = k$. So $\lambda = k$.
$T(z) = k/z$.
Check the fourth condition:
$T(k) = k/k = 1$.
This matches!

**5. Conclusion**
Yes, the conditions are consistent.
1.  The conditions $A \to B, B \to A, C \to D$ uniquely determine a projectivity $T$ (Exercise 9).
2.  We showed (via coordinates) that this unique $T$ automatically satisfies $D \to C$.
3.  Therefore, there exists a unique projectivity interchanging $A, B$ and $C, D$.

**Note:** This transformation is an involution ($T^2 = I$).
The pairs $(A, B)$ and $(C, D)$ are harmonic conjugates if and only if... wait.
Actually, the cross ratio $(A, B; C, D) = -1$ is NOT required for the existence of the involution.
Any two pairs can be swapped by an involution.
(Harmonic separation is relevant if the fixed points of the involution separate the pairs).
The existence is guaranteed for any distinct 4 points.
