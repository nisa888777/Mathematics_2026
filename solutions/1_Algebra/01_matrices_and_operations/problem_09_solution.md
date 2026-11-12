# Exercise 9. Composing Transformations

## Question

Let

$$
S = \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix}, \qquad R = \begin{pmatrix} 0 & -1 \\\ 1 & 0 \end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation. For

$$
x = \begin{pmatrix} 1 \\\ 2 \end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

---

## Solution

We are given the nonuniform scaling matrix $S$, the $90^\circ$ counterclockwise rotation matrix $R$, and the input vector $x$[span_3](start_span)[span_3](end_span):

$$
S = \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix}, \qquad R = \begin{pmatrix} 0 & -1 \\\ 1 & 0 \end{pmatrix}, \qquad x = \begin{pmatrix} 1 \\\ 2 \end{pmatrix}
$$

Recall how each transformation acts on an arbitrary vector $\begin{pmatrix} u \\\ v \end{pmatrix} \in \mathbb{R}^2$:
* **Scaling $S$:** Stretches the horizontal ($x$-axis) coordinate by a factor of $2$ and leaves the vertical ($y$-axis) coordinate unchanged:

$$
S \begin{pmatrix} u \\\ v \end{pmatrix} = \begin{pmatrix} 2u \\\ v \end{pmatrix}
$$

* **Rotation $R$:** Rotates the vector by $90^\circ$ counterclockwise around the origin, mapping the positive $x$-axis to the positive $y$-axis and the positive $y$-axis to the negative $x$-axis:

$$
R \begin{pmatrix} u \\\ v \end{pmatrix} = \begin{pmatrix} -v \\\ u \end{pmatrix}
$$

---

### 1. Computing $RSx$ (Scale First, Then Rotate)

Applying $S$ to $x$ first[span_4](start_span)[span_4](end_span):

$$
Sx = \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\\ 2 \end{pmatrix} = \begin{pmatrix} 2(1) + 0(2) \\\ 0(1) + 1(2) \end{pmatrix} = \begin{pmatrix} 2 \\\ 2 \end{pmatrix}
$$

Next, applying $R$ to the scaled vector $Sx$:

$$
RSx = R(Sx) = \begin{pmatrix} 0 & -1 \\\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\\ 2 \end{pmatrix} = \begin{pmatrix} 0(2) + (-1)(2) \\\ 1(2) + 0(2) \end{pmatrix} = \begin{pmatrix} -2 \\\ 2 \end{pmatrix}
$$

*(Alternatively, via the composite matrix $RS = \begin{pmatrix} 0 & -1 \\\ 2 & 0 \end{pmatrix}$, we obtain $RSx = \begin{pmatrix} -2 \\\ 2 \end{pmatrix}$.)*

---

### 2. Computing $SRx$ (Rotate First, Then Scale)

Applying $R$ to $x$ first[span_5](start_span)[span_5](end_span):

$$
Rx = \begin{pmatrix} 0 & -1 \\\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\\ 2 \end{pmatrix} = \begin{pmatrix} 0(1) + (-1)(2) \\\ 1(1) + 0(2) \end{pmatrix} = \begin{pmatrix} -2 \\\ 1 \end{pmatrix}
$$

Next, applying $S$ to the rotated vector $Rx$:

$$
SRx = S(Rx) = \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\\ 1 \end{pmatrix} = \begin{pmatrix} 2(-2) + 0(1) \\\ 0(-2) + 1(1) \end{pmatrix} = \begin{pmatrix} -4 \\\ 1 \end{pmatrix}
$$

*(Alternatively, via the composite matrix $SR = \begin{pmatrix} 0 & -2 \\\ 1 & 0 \end{pmatrix}$, we obtain $SRx = \begin{pmatrix} -4 \\\ 1 \end{pmatrix}$.)*

---

### 3. Comparison and Geometric Explanation

Comparing the two resulting vectors[span_6](start_span)[span_6](end_span)[span_7](start_span)[span_7](end_span):

$$
RSx = \begin{pmatrix} -2 \\\ 2 \end{pmatrix} \neq \begin{pmatrix} -4 \\\ 1 \end{pmatrix} = SRx
$$

**Why the Order Matters Geometrically:**
* **Nonuniform scaling is tied to fixed coordinate axes:** The matrix $S$ stretches lengths only along the **horizontal ($x$-axis)** direction by a factor of $2$, while leaving the **vertical ($y$-axis)** direction unscaled.
* **In $RSx$ (scale then rotate):** The original $x$-component ($1$) is doubled to $2$ first. When $R$ then rotates the vector $90^\circ$ counterclockwise, that doubled horizontal coordinate moves into the **positive $y$-axis** direction, while the unscaled original $y$-component ($2$) moves into the **negative $x$-axis** direction, landing at $(-2, 2)^T$.
* **In $SRx$ (rotate then scale):** The $90^\circ$ counterclockwise rotation moves the original $y$-component ($2$) onto the **negative $x$-axis** ($-2$) and the original $x$-component ($1$) onto the **positive $y$-axis** ($1$) *before* scaling happens. Consequently, $S$ doubles the new horizontal coordinate ($-2 \to -4$) instead of the original one, landing at $(-4, 1)^T$.

Because rotation changes which coordinate lies along the horizontal axis of stretch, matrix multiplication is non-commutative ($RS \neq SR$).

---

### Conclusion

* **Scale then rotate:** $RSx = \begin{pmatrix} -2 \\\ 2 \end{pmatrix}$
* **Rotate then scale:** $SRx = \begin{pmatrix} -4 \\\ 1 \end{pmatrix}$
* **Geometric takeaway:** Since $S$ stretches strictly along the $x$-axis and $R$ swaps the $x$- and $y$-directions (with a sign change on the new $x$-coordinate), changing the order changes which component gets doubled, so $RSx \neq SRx$.
