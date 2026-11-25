# Exercise 5. Angle Between Vectors

## Question

Given $u = (1, 1, 0)$ and $v = (1, 0, 1)$:

1. Use the sign of $u \cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

---

## Solution

In $\mathbb{R}^3$, the dot product connects algebraic components to the angle $\theta \in [0, \pi]$ ($0^\circ \le \theta \le 180^\circ$) between two nonzero vectors via the **geometric dot product formula**:

$$
u \cdot v = \|u\|\|v\|\cos\theta
$$

Since $\|u\| > 0$ and $\|v\| > 0$ for nonzero vectors, the sign of $u \cdot v$ matches the sign of $\cos\theta$.

---

### 1. Predict the Type of Angle Using the Sign of $u \cdot v$

* **Mechanism (Dot Product Sign Criterion):**
  * If $u \cdot v > 0$, then $\cos\theta > 0$, so the angle $\theta$ is **acute** ($0^\circ \le \theta < 90^\circ$).
  * If $u \cdot v = 0$, then $\cos\theta = 0$, so the angle $\theta$ is **right** ($\theta = 90^\circ$).
  * If $u \cdot v < 0$, then $\cos\theta < 0$, so the angle $\theta$ is **obtuse** ($90^\circ < \theta \le 180^\circ$).

* **Calculation of $u \cdot v$:**

$$
u \cdot v = (1)(1) + (1)(0) + (0)(1) = 1 + 0 + 0 = 1
$$

* **Prediction:** Because $u \cdot v = 1 > 0$, we predict that the angle $\theta$ between $u$ and $v$ is **acute** ($0^\circ \le \theta < 90^\circ$).

---

### 2. Compute the Exact Angle $\theta$

* **Mechanism (Cosine Angle Formula):** Solving $u \cdot v = \|u\|\|v\|\cos\theta$ for $\cos\theta$ gives:

$$
\cos\theta = \frac{u \cdot v}{\|u\|\|v\|}
$$

* **Step 1 — Compute the Euclidean norms $\|u\|$ and $\|v\|$:**

$$
\|u\| = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{2}, \qquad \|v\| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{2}
$$

* **Step 2 — Substitute into the cosine formula:**

$$
\cos\theta = \frac{1}{\sqrt{2} \cdot \sqrt{2}} = \frac{1}{2}
$$

* **Step 3 — Apply $\arccos$ on $[0, \pi]$:**

$$
\theta = \arccos\left(\frac{1}{2}\right) = \frac{\pi}{3}\text{ radians} = 60^\circ
$$

---

### 3. Compare the Result with the Prediction & Geometric Interpretation

* **Comparison:** The exact angle $\theta = 60^\circ$ ($\frac{\pi}{3}$ radians) satisfies $0^\circ < 60^\circ < 90^\circ$, confirming that it is indeed an **acute angle**, which matches our qualitative prediction from $u \cdot v > 0$.
* **Geometric Interpretation:** Geometrically, $u = (1, 1, 0)$, $v = (1, 0, 1)$, and their difference vector $u - v = (0, 1, -1)$ all have equal length ($\|u\| = \|v\| = \|u - v\| = \sqrt{2}$). Thus, placing $u$ and $v$ tail-to-tail at the origin forms two sides of an **equilateral triangle** in $\mathbb{R}^3$, whose interior angles are all $60^\circ$.

---

### Conclusion

* **Sign prediction:** $u \cdot v = 1 > 0$, predicting an **acute angle** ($0^\circ \le \theta < 90^\circ$).
* **Exact angle:** $\theta = \frac{\pi}{3}\text{ radians} = 60^\circ$.
* **Comparison:** The computed angle ($60^\circ$) is strictly between $0^\circ$ and $90^\circ$, fully confirming the initial prediction.
