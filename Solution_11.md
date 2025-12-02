### **Problem Statement**
Show that any projectivity is the product of three or fewer perspectivities.

---

### **Proof**

**Case 1: Distinct Lines ($l \neq l'$)**
From **Exercise 10**, if the domain and codomain lines are distinct, the projectivity can be expressed as the product of 2 perspectivities.

**Case 2: Same Line ($l = l'$)**
Let $T: l \to l$ be a projectivity.
We want to show $T = \pi_3 \circ \pi_2 \circ \pi_1$.

1.  Choose an auxiliary line $k \neq l$.
2.  Choose any perspectivity $\pi_1: l \to k$.
3.  Consider the map $S = T \circ \pi_1^{-1}: k \to l$.
    *   $\pi_1^{-1}$ maps $k \to l$.
    *   $T$ maps $l \to l$.
    *   So $S$ maps $k \to l$.
4.  Since $k$ and $l$ are distinct lines, by **Exercise 10**, the projectivity $S$ can be written as the product of 2 perspectivities:
    $$S = \pi_3 \circ \pi_2$$
    where $\pi_2: k \to m$ and $\pi_3: m \to l$ (for some intermediate line $m$).
5.  Substitute back:
    $$T \circ \pi_1^{-1} = \pi_3 \circ \pi_2$$
    $$T = \pi_3 \circ \pi_2 \circ \pi_1$$

Thus, any projectivity from $l$ to itself is the product of 3 perspectivities.

**Conclusion:**
Any projectivity is the product of 3 or fewer perspectivities.
(2 if lines are distinct, 3 if lines are the same).
