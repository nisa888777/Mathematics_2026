# Exercise 11. Decomposition into Parallel and Perpendicular Components

## Question

Decompose $u = (3, 4)$ into components parallel and perpendicular to $v = (1, 2)$. Check

$$
u = u_{\parallel} + u_{\perp}, \qquad u_{\perp} \cdot v = 0.
$$

Explain why these are two independent checks of correctness.

---

## Solution

In $\mathbb{R}^2$, any vector $u$ can be uniquely decomposed relative to a nonzero direction vector $v$ into a **parallel component** $u_{\parallel}$ (the orthogonal projection of $u$ onto $v$) and a **perpendicular component** $u_{\perp}$:

$$
u_{\parallel} = \text{proj}_{v} u = \frac{u \cdot v}{v \cdot v} v, \qquad u_{\perp} = u - u_{\parallel}
$$

---

### 1. Compute the Parallel and Perpendicular Components ($u_{\parallel}$ and $u_{\perp}$)

* **Step 1 — Compute the dot products $u \cdot v$ and $v \cdot v$:**

$$
u \cdot v = (3)(1) + (4)(2) = 3 + 8 = 11
$$

$$
v \cdot v = \|v\|^2 = 1^2 + 2^2 = 1 + 4 = 5
$$

* **Step 2 — Compute the parallel component $u_{\parallel}$:**

$$
u_{\parallel} = \frac{11}{5}(1, 2) = \left(\frac{11}{5}, \, \frac{22}{5}\right)
$$

* **Step 3 — Compute the perpendicular component $u_{\perp}$:**

$$
u_{\perp} = u - u_{\parallel} = (3, 4) - \left(\frac{11}{5}, \, \frac{22}{5}\right) = \left(\frac{15}{5} - \frac{11}{5}, \, \frac{20}{5} - \frac{22}{5}\right) = \left(\frac{4}{5}, \, -\frac{2}{5}\right)
$$

---

### 2. Perform Both Verification Checks

* **Check 1 — Reconstruction ($u = u_{\parallel} + u_{\perp}$):**

$$
u_{\parallel} + u_{\perp} = \left(\frac{11}{5}, \, \frac{22}{5}\right) + \left(\frac{4}{5}, \, -\frac{2}{5}\right) = \left(\frac{11 + 4}{5}, \, \frac{22 - 2}{5}\right) = \left(\frac{15}{5}, \, \frac{20}{5}\right) = (3, 4) = u
$$

* **Check 2 — Orthogonality ($u_{\perp} \cdot v = 0$):**

$$
u_{\perp} \cdot v = \left(\frac{4}{5}\right)(1) + \left(-\frac{2}{5}\right)(2) = \frac{4}{5} - \frac{4}{5} = 0
$$

---

### 3. Why These Are Two Independent Checks of Correctness

Neither condition implies the other on its own, because each verifies a separate geometric requirement of an orthogonal decomposition:

1. **What $u = u_{\parallel} + u_{\perp}$ tests (Additive Completeness):** This equation checks only that the two pieces sum back to $u$ without arithmetic subtraction errors. However, infinitely many wrong decompositions satisfy $u = w_1 + w_2$ (for instance, choosing a wrong scalar multiple $w_1 = 2v = (2, 4)$ and $w_2 = u - 2v = (1, 0)$ still gives $w_1 + w_2 = (3, 4) = u$, even though $w_2$ is not perpendicular to $v$).
2. **What $u_{\perp} \cdot v = 0$ tests (Orthogonality / Correct Projection Scale):** This equation checks that $u_{\perp}$ is genuinely perpendicular to $v$, which happens if and only if the scalar factor $\frac{u \cdot v}{v \cdot v} = \frac{11}{5}$ in $u_{\parallel}$ was computed accurately. However, orthogonality alone does not check whether $u_{\parallel}$ and $u_{\perp}$ recombine to form $u$ (for instance, any multiple of $u_{\perp}$, such as $(4, -2)$, satisfies $(4, -2) \cdot v = 0$ without summing with $u_{\parallel}$ to give $u$).

Together with $u_{\parallel}$ being a scalar multiple of $v$, these two independent conditions guarantee that the decomposition is both **exact** and **unique**.

---

### Conclusion

* **Parallel component:** $u_{\parallel} = \left(\frac{11}{5}, \, \frac{22}{5}\right)$.
* **Perpendicular component:** $u_{\perp} = \left(\frac{4}{5}, \, -\frac{2}{5}\right)$.
* **Verification:** $u_{\parallel} + u_{\perp} = (3, 4) = u$ and $u_{\perp} \cdot v = \frac{4}{5} - \frac{4}{5} = 0$.
* **Independence of checks:** $u = u_{\parallel} + u_{\perp}$ verifies additive reconstruction while $u_{\perp} \cdot v = 0$ verifies perpendicularity (correct projection scaling); neither condition holds automatically from the other.
