### **Problem Statement**
A perspective collineation induces a projectivity on any fixed line. Discuss the fixed point behavior of such a projectivity.

---

### **Discussion**

Let $T$ be a perspective collineation with Axis $a$ and Center $C$.
Let $l$ be a fixed line (invariant line, $T(l) = l$).

**Case 1: The fixed line is the Axis ($l = a$)**
*   Every point on the axis is fixed.
*   The restriction $T|_a$ is the Identity.
*   **Fixed Points:** All points on $l$.

**Case 2: The fixed line passes through the Center ($C \in l$)**
*   By definition of Center, every line passing through $C$ is invariant.
*   So $l$ is mapped to itself.
*   The intersection of $l$ with the axis $a$ is a point $X = l \cap a$.
*   Since $X \in a$, $X$ is a fixed point.
*   Since $C$ is the center, $C$ is a fixed point (lines through $C$ are fixed, intersection of two such lines is fixed? No).
    *   Let's check if $C$ is fixed.
    *   Take line $m$ through $C$. $T(m) = m$.
    *   Take line $n$ through $C$. $T(n) = n$.
    *   $T(C) = T(m \cap n) = T(m) \cap T(n) = m \cap n = C$.
    *   Yes, the Center $C$ is always a fixed point.
*   **Subcase 2a: Homology ($C \notin a$)**
    *   $l$ passes through $C$ and intersects $a$ at $X$.
    *   $C$ and $X$ are distinct.
    *   $T|_l$ has two fixed points: $C$ and $X$.
    *   This is a **Hyperbolic** projectivity on $l$.
*   **Subcase 2b: Elation ($C \in a$)**
    *   $l$ passes through $C$.
    *   The intersection $l \cap a$ is $C$.
    *   So $C$ is the only fixed point on $l$ (unless $l=a$).
    *   $T|_l$ has exactly one fixed point: $C$.
    *   This is a **Parabolic** projectivity on $l$.

**Case 3: The fixed line is neither the Axis nor through the Center**
*   Can there be such a line?
*   Let $l$ be a fixed line.
*   $l$ must intersect the axis $a$ at some point $X$. $X$ is fixed.
*   If $l$ is not $a$, then $T$ maps $l$ to a line through $T(X)=X$.
*   For $l$ to be invariant, $T(P)$ must lie on $l$ for all $P \in l$.
*   But lines connecting $P$ and $T(P)$ pass through $C$.
*   So for $P \in l$, the line $PP'$ is the line $PC$.
*   If $P' \in l$, then $P, P', C$ are collinear.
*   This implies $C$ lies on the line containing $P$ and $P'$, which is $l$.
*   So if $l$ is invariant and not the axis, it **must** pass through the Center.
*   **Conclusion:** There are no other fixed lines.

**Summary of Fixed Point Behavior on Fixed Lines:**
1.  **On the Axis:** Identity (all points fixed).
2.  **On lines through Center (Homology):** Hyperbolic (2 fixed points: Center and Axis-intersection).
3.  **On lines through Center (Elation):** Parabolic (1 fixed point: Center).
