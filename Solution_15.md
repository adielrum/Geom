### **Problem Statement**
Prove that a projective collineation that leaves fixed four points, no three of which are collinear, must be the identity. (Hint: Choose $l_{\infty}$ to be one of the fixed lines, and apply Theorem 2.2 to $P^{2}-l_{\infty}.$)

---

### **Proof**

**Method 1: Using Fundamental Theorem of Coordinates (as in Solution 16)**
This is exactly the core lemma proven in **Solution_16.md**.
1.  Let the four fixed points be $A, B, C, D$.
2.  Choose a basis such that $A=[1,0,0], B=[0,1,0], C=[0,0,1], D=[1,1,1]$.
3.  Let $M$ be the matrix of the collineation.
4.  $M$ fixing $A, B, C$ implies $M$ is diagonal.
5.  $M$ fixing $D$ implies the diagonal entries are equal ($M = kI$).
6.  $M = kI$ induces the identity map.

**Method 2: Using the Hint (Affine Approach)**
1.  Let the four points be $P_1, P_2, P_3, P_4$.
2.  Since no three are collinear, we can form a triangle with $P_1, P_2, P_3$.
3.  The hint suggests choosing a fixed line to be $l_\infty$.
    *   However, we are not given a fixed line initially, only points.
    *   But if $P_1$ and $P_2$ are fixed, the line $P_1P_2$ is a fixed line (invariant line).
    *   Similarly $P_2P_3$ and $P_3P_1$ are fixed lines.
    *   Let's choose the line $P_1P_2$ to be $l_\infty$.
4.  If $l_\infty$ is fixed (pointwise? No, just the line is mapped to itself), we can restrict to the affine plane $E^2 = P^2 - l_\infty$.
    *   Wait, if $P_1$ and $P_2$ are fixed points on $l_\infty$, the transformation at infinity is a projectivity with 2 fixed points.
5.  In the affine plane, we have fixed points $P_3$ and $P_4$.
6.  An affine transformation fixing 2 points fixes the line connecting them.
7.  Also, the lines connecting $P_3$ to $P_1$ (direction 1) and $P_3$ to $P_2$ (direction 2) are invariant lines?
    *   $T(P_3) = P_3$.
    *   $T(P_1) = P_1$.
    *   So line $P_1P_3$ is invariant.
    *   Similarly $P_2P_3$ is invariant.
8.  In $E^2$, $T$ fixes the origin ($P_3$ as origin) and the directions of axes ($P_1, P_2$ at infinity).
    *   So $T$ is a scaling: $x' = ax, y' = by$.
9.  We also have $P_4$ fixed. $P_4 = (x_0, y_0)$ with $x_0 \neq 0, y_0 \neq 0$ (since no 3 collinear).
    *   $ax_0 = x_0 \implies a = 1$.
    *   $by_0 = y_0 \implies b = 1$.
10. So $T$ is the identity in $E^2$.
11. Thus $T$ is the identity in $P^2$.

**Conclusion:**
A projective collineation fixing 4 points in general position is the identity.
