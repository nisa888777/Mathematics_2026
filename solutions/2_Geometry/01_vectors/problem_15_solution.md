# Exercise 15. Comparing Directions Using the Cosine of the Angle

## Question

Given

$$
a = (1, 2, 1), \qquad b = (2, 4, 2), \qquad c = (2, 0, 3).
$$

For each pair, compute

$$
\frac{u \cdot v}{\|u\| \, \|v\|}.
$$

Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

---

## Solution

For any two nonzero vectors $u, v \in \mathbb{R}^3$, the **geometric dot product formula** gives the cosine of the angle $\theta \in [0, \pi]$ between them:

$$
\cos\theta = \frac{u \cdot v}{\|u\| \, \|v\|}
$$

Because $\cos\theta$ is strictly decreasing on $[0, \pi]$, a **larger** cosine value corresponds to a **smaller** angle $\theta$.

---

### 1. Compute the Euclidean Norms of $a$, $b$, and $c$

* **Norm of $a = (1, 2, 1)$:**

$$
\|a\| = \sqrt{1^2 + 2^2 + 1^2} = \sqrt{1 + 4 + 1} = \sqrt{6}
$$

* **Norm of $b = (2, 4, 2)$:**

$$
\|b\| = \sqrt{2^2 + 4^2 + 2^2} = \sqrt{4 + 16 + 4} = \sqrt{24} = 2\sqrt{6}
$$

* **Norm of $c = (2, 0, 3)$:**

$$
\|c\| = \sqrt{2^2 + 0^2 + 3^2} = \sqrt{4 + 0 + 9} = \sqrt{13}
$$

---

### 2. Compute $\frac{u \cdot v}{\|u\| \, \|v\|}$ for Each Pair

* **Pair 1 — $a = (1, 2, 1)$ and $b = (2, 4, 2)$:**

$$
a \cdot b = (1)(2) + (2)(4) + (1)(2) = 2 + 8 + 2 = 12
$$

$$
\cos\theta_{ab} = \frac{a \cdot b}{\|a\| \, \|b\|} = \frac{12}{\sqrt{6} \cdot 2\sqrt{6}} = \frac{12}{2 \cdot 6} = \frac{12}{12} = 1
$$

* **Pair 2 — $a = (1, 2, 1)$ and $c = (2, 0, 3)$:**

$$
a \cdot c = (1)(2) + (2)(0) + (1)(3) = 2 + 0 + 3 = 5
$$

$$
\cos\theta_{ac} = \frac{a \cdot c}{\|a\| \, \|c\|} = \frac{5}{\sqrt{6}\sqrt{13}} = \frac{5}{\sqrt{78}} \approx 0.5661
$$

* **Pair 3 — $b = (2, 4, 2)$ and $c = (2, 0, 3)$:**

$$
b \cdot c = (2)(2) + (4)(0) + (2)(3) = 4 + 0 + 6 = 10
$$

$$
\cos\theta_{bc} = \frac{b \cdot c}{\|b\| \, \|c\|} = \frac{10}{2\sqrt{6}\sqrt{13}} = \frac{5}{\sqrt{78}} \approx 0.5661
$$

---

### 3. Order the Pairs by Increasing Angle Between the Vectors

Compare the cosine values:

$$
\cos\theta_{ab} = 1 > \cos\theta_{ac} = \cos\theta_{bc} = \frac{5}{\sqrt{78}}
$$

Since smaller angles produce larger cosines on $[0, \pi]$:

1. **Smallest angle:** The pair **$(a, b)$**, with $\cos\theta_{ab} = 1 \implies \theta_{ab} = 0^\circ$ ($0\text{ rad}$).
2. **Tied for larger angle:** The pairs **$(a, c)$ and $(b, c)$** have the **exact same angle**, with $\cos\theta_{ac} = \cos\theta_{bc} = \frac{5}{\sqrt{78}} \implies \theta_{ac} = \theta_{bc} = \arccos\!\left(\frac{5}{\sqrt{78}}\right) \approx 55.52^\circ$ ($0.969\text{ rad}$).

Thus, the ordering by increasing angle is:

$$
\theta_{ab} < \theta_{ac} = \theta_{bc}
$$

---

### 4. Why the Value Is $1$ for $a$ and $b$ Despite Different Lengths

* **Scale Invariance of Direction (Normalization):** Dividing $u \cdot v$ by $\|u\|\|v\|$ normalizes each vector to its unit direction vector $\hat{u} = \frac{u}{\|u\|}$ and $\hat{v} = \frac{v}{\|v\|}$, removing magnitude information so that $\frac{u \cdot v}{\|u\|\|v\|} = \hat{u} \cdot \hat{v}$ depends **only on direction**, not length.
* **Same Ray / Positive Scalar Multiple:** Observe that $b = (2, 4, 2) = 2(1, 2, 1) = 2a$. Because $b$ is a **positive scalar multiple** of $a$, both vectors point in the exact same direction along the same ray from the origin, so their unit vectors are identical: $\hat{a} = \hat{b} = \frac{1}{\sqrt{6}}(1, 2, 1)$. Consequently, the angle between them is $\theta_{ab} = 0$, giving $\cos(0) = 1$, and both make the exact same angle with $c$.

---

### Conclusion

* **Cosine values:**
  * Pair $(a, b)$: $\frac{a \cdot b}{\|a\|\|b\|} = 1$.
  * Pair $(a, c)$: $\frac{a \cdot c}{\|a\|\|c\|} = \frac{5}{\sqrt{78}}$.
  * Pair $(b, c)$: $\frac{b \cdot c}{\|b\|\|c\|} = \frac{5}{\sqrt{78}}$.
* **Ordering by increasing angle:** $(a, b)$ first ($\theta_{ab} = 0^\circ$), followed by $(a, c)$ and $(b, c)$ tied ($\theta_{ac} = \theta_{bc} = \arccos\!\left(\frac{5}{\sqrt{78}}\right) \approx 55.52^\circ$).
* **Reason $\cos\theta_{ab} = 1$:** Dividing by $\|a\|\|b\|$ removes vector lengths and compares only unit directions; since $b = 2a$ points in the exact same direction as $a$, the angle between them is $0$ and $\cos(0) = 1$.
