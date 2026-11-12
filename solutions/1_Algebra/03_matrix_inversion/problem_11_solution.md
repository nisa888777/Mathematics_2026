# Exercise 11. Parameter and Invertibility

## Question

For

$$
A(t) = \begin{pmatrix} 1 & t \\ t & 1 \end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

---

## Solution

We are given the parameterized $2 \times 2$ matrix[span_1](start_span)[span_1](end_span):

$$
A(t) = \begin{pmatrix} 1 & t \\ t & 1 \end{pmatrix}
$$

---

### 1. Find All Values of $t$ for Which $A(t)$ Is Invertible

A square matrix is invertible if and only if its determinant is non-zero. Computing the determinant of $A(t)$[span_2](start_span)[span_2](end_span):

$$
\det(A(t)) = (1)(1) - (t)(t) = 1 - t^2
$$

Setting the determinant equal to zero to find the singular (non-invertible) cases:

$$
1 - t^2 = 0 \quad \Longrightarrow \quad (1 - t)(1 + t) = 0 \quad \Longrightarrow \quad t = 1 \quad \text{or} \quad t = -1
$$

Therefore, $A(t)$ is invertible for all real (or complex) numbers $t$ except $t = 1$ and $t = -1$:

$$
t \neq \pm 1 \qquad (\text{i.e., } t \in \mathbb{R} \setminus \{-1, 1\})
$$

---

### 2. Formula for $A(t)^{-1}$

For any $t \neq \pm 1$, we apply the $2 \times 2$ inverse formula using $\det(A(t)) = 1 - t^2$:

$$
A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{1 - t^2} & -\frac{t}{1 - t^2} \\ -\frac{t}{1 - t^2} & \frac{1}{1 - t^2} \end{pmatrix}
$$

---

### 3. Behavior at the Excluded Values ($t = 1$ and $t = -1$)

* **Algebraic breakdown (division by zero):** At $t = 1$ and $t = -1$, the denominator $1 - t^2$ in the scalar factor $\frac{1}{1 - t^2}$ becomes $0$. Since division by zero is undefined, every entry of the formula diverges ($\pm \infty$) and the inverse formula ceases to exist.
* **Matrix structure (linear dependence):** Substituting the excluded values directly into $A(t)$ produces singular matrices whose rows are linearly dependent[span_3](start_span)[span_3](end_span):
  * For $t = 1$:

$$
A(1) = \begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix} \qquad (\text{Row } 1 = \text{Row } 2)
$$

  * For $t = -1$:

$$
A(-1) = \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix} \qquad (\text{Row } 1 = -\text{Row } 2)
$$

In both cases, the matrix collapses the plane onto a single line and cannot be inverted.

---

### Conclusion

* **Invertibility condition:** $A(t)$ is invertible for all $t \neq \pm 1$.
* **Inverse formula:**

$$
A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix}
$$

* **Excluded values:** At $t = \pm 1$, the denominator $1 - t^2$ equals zero, causing division by zero in the inverse formula, while $A(t)$ becomes singular with linearly dependent rows.
