### **Problem Statement**
Show that the set of perspective collineations with a given axis and center (with the identity thrown in) is a group. Do these groups have any finite subgroups?

---

### **Solution**

#### **1. Group Property**
Let $a$ be the axis and $C$ be the center.
Let $G_{C, a}$ be the set of all perspective collineations with center $C$ and axis $a$.

*   **Identity:** The identity transformation fixes all points (so fixes $a$ pointwise) and all lines (so fixes lines through $C$). Thus $I \in G_{C, a}$.
*   **Closure:** Let $T_1, T_2 \in G_{C, a}$.
    *   $T_1, T_2$ fix $a$ pointwise $\implies T_1 \circ T_2$ fixes $a$ pointwise.
    *   $T_1, T_2$ fix lines through $C$ $\implies T_1 \circ T_2$ fixes lines through $C$ (maps line $l \ni C$ to $l$).
    *   Thus $T_1 \circ T_2$ is a perspective collineation with center $C$ and axis $a$.
*   **Inverse:** Let $T \in G_{C, a}$.
    *   $T$ is a bijection.
    *   $T(P) = P$ for $P \in a \implies P = T^{-1}(P)$. So $T^{-1}$ fixes $a$ pointwise.
    *   $T(l) = l$ for $C \in l \implies l = T^{-1}(l)$. So $T^{-1}$ fixes lines through $C$.
    *   Thus $T^{-1} \in G_{C, a}$.

Therefore, $G_{C, a}$ is a group.

#### **2. Structure of the Group**
We analyze the restriction of the group to a single line $l$ passing through $C$ (but not $a$).
Let $X = l \cap a$.
For any $T \in G_{C, a}$, $T$ maps $l$ to itself, fixing $C$ and $X$.

**Case A: Homology ($C \notin a$)**
*   $C$ and $X$ are distinct.
*   We can set coordinates on $l$ such that $C = \infty$ (1,0) and $X = 0$ (0,1).
*   A projectivity fixing $0$ and $\infty$ is of the form $x' = kx$ (scaling).
*   The group is isomorphic to the multiplicative group of the field $F^* = \mathbb{R} \setminus \{0\}$.
*   **Finite Subgroups:**
    *   Subgroups of $\mathbb{R}^*$: $\{1, -1\}$. (Cyclic group of order 2).
    *   This corresponds to the **Harmonic Homology** (Involution).

**Case B: Elation ($C \in a$)**
*   $C$ and $X$ coincide ($C=X$).
*   We can set coordinates on $l$ such that $C = \infty$.
*   A projectivity fixing only $\infty$ is of the form $x' = x + t$ (translation).
*   The group is isomorphic to the additive group of the field $F^+ = \mathbb{R}$.
*   **Finite Subgroups:**
    *   The additive group of reals has no finite subgroups other than the trivial group $\{0\}$.
    *   (If $x + x + ... + x = nx = 0 \implies x=0$ in characteristic 0).

**Answer:**
*   Yes, it is a group.
*   If it is a Homology group ($C \notin a$), it has a finite subgroup of order 2 (Harmonic Homology).
*   If it is an Elation group ($C \in a$), it has no non-trivial finite subgroups (over $\mathbb{R}$).
