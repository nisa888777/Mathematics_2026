# Exercise 13. Undoing a Composite Transformation

## Question

The matrices

$$
S = \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix}, \qquad H = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix}
$$

describe nonuniform scaling and shear. For $T = HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1} = S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

---

## Solution

We are given the scaling matrix $S$ and the horizontal shear matrix $H$:

$$
S = \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix}, \qquad H = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix}
$$

---

### 1. Method 1: Compute $T = HS$ First, Then Invert $T$

First, we compute the composite transformation matrix $T = HS$:

$$
T = HS = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1)(2) + (1)(0) & (1)(0) + (1)(1) \\\ (0)(2) + (1)(0) & (0)(0) + (1)(1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\\ 0 & 1 \end{pmatrix}
$$

Next, we find the determinant of $T$:

$$
\det(T) = (2)(1) - (1)(0) = 2
$$

Since $\det(T) = 2 \neq 0$, $T^{-1}$ exists. Applying the $2 \times 2$ inverse formula:

$$
T^{-1} = \frac{1}{2} \begin{pmatrix} 1 & -1 \\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\ 0 & 1 \end{pmatrix}
$$

---

### 2. Method 2: Compute $(HS)^{-1} = S^{-1}H^{-1}$

First, we compute the individual inverses $S^{-1}$ and $H^{-1}$:

* For $S$: $\det(S) = (2)(1) - (0)(0) = 2$, so

$$
S^{-1} = \frac{1}{2} \begin{pmatrix} 1 & 0 \\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\\ 0 & 1 \end{pmatrix}
$$

* For $H$: $\det(H) = (1)(1) - (1)(0) = 1$, so

$$
H^{-1} = \frac{1}{1} \begin{pmatrix} 1 & -1 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -1 \\\ 0 & 1 \end{pmatrix}
$$

Now, we multiply $S^{-1}$ by $H^{-1}$:

$$
S^{-1}H^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \left(\frac{1}{2}\right)(1) + (0)(0) & \left(\frac{1}{2}\right)(-1) + (0)(1) \\\ (0)(1) + (1)(0) & (0)(-1) + (1)(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\ 0 & 1 \end{pmatrix}
$$

---

### 3. Compare Results and Compute the Incorrect Order $H^{-1}S^{-1}$

**Comparison of Method 1 and Method 2:**

Both methods produce the exact same inverse transformation matrix:

$$
T^{-1} = (HS)^{-1} = S^{-1}H^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\ 0 & 1 \end{pmatrix}
$$

**Computing the Incorrect Order $H^{-1}S^{-1}$:**

Multiplying the inverses in the unreversed order gives:

$$
H^{-1}S^{-1} = \begin{pmatrix} 1 & -1 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} \frac{1}{2} & 0 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1)\left(\frac{1}{2}\right) + (-1)(0) & (1)(0) + (-1)(1) \\\ (0)\left(\frac{1}{2}\right) + (1)(0) & (0)(0) + (1)(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -1 \\\ 0 & 1 \end{pmatrix}
$$

Comparing the two products:

$$
H^{-1}S^{-1} = \begin{pmatrix} \frac{1}{2} & -1 \\\ 0 & 1 \end{pmatrix} \neq \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\ 0 & 1 \end{pmatrix} = S^{-1}H^{-1}
$$

Thus, keeping the original order yields an incorrect matrix (the top-right entry is $-1$ instead of $-\frac{1}{2}$).

---

### 4. Explanation of the Rule: “When Undoing a Composition of Operations, We Undo Them from the End”

* **Geometric and operational sequence:** When the composite transformation $T = HS$ acts on a vector $\mathbf{x}$, matrix multiplication operates from right to left:

$$
T\mathbf{x} = (HS)\mathbf{x} = H(S\mathbf{x})
$$

Here, **scaling $S$ is applied first** (stretching $x$ by $2$), and **shear $H$ is applied second (at the end)** to the already-scaled vector.
* **Reversing the steps:** To recover the original vector $\mathbf{x}$, we must peel off the transformations in reverse chronological order:
  1. First, undo the **last** operation ($H$) by applying $H^{-1}$ (shearing back by $-1$).
  2. Second, undo the **first** operation ($S$) by applying $S^{-1}$ (shrinking $x$ by $\frac{1}{2}$).
* **Algebraic confirmation:** Applying $S^{-1}H^{-1}$ to $T\mathbf{x}$ cancels the operations from the inside out:

$$
(S^{-1}H^{-1})(HS)\mathbf{x} = S^{-1}(H^{-1}H)S\mathbf{x} = S^{-1}IS\mathbf{x} = S^{-1}S\mathbf{x} = \mathbf{x}
$$

If we instead applied $H^{-1}S^{-1}$, we would attempt to shrink the vector before undoing the shear, which alters the shear offset and fails to restore $\mathbf{x}$.

---

### Conclusion

* Both computing $(HS)^{-1}$ directly and multiplying $S^{-1}H^{-1}$ give:

$$
T^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\ 0 & 1 \end{pmatrix}
$$

* Reversing the order fails because

$$
H^{-1}S^{-1} = \begin{pmatrix} \frac{1}{2} & -1 \\\ 0 & 1 \end{pmatrix} \neq T^{-1}
$$

Undoing a sequence of transformations always requires reversing the last operation first.
