# Exercise 2. Determinant of a 3×3 Matrix

## Question

For

$$
A = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & 3 & 4 \\\ 2 & 1 & 5 \end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

---

## Solution

We are given the $3 \times 3$ matrix[span_2](start_span)[span_2](end_span):

$$
A = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & 3 & 4 \\\ 2 & 1 & 5 \end{pmatrix}
$$

---

### 1. Computing $\det(A)$ Using Sarrus' Rule

To apply Sarrus' rule, we repeat the first two columns to the right of the matrix[span_3](start_span)[span_3](end_span):

$$
\begin{array}{ccc|cc}
1 & 2 & -1 & 1 & 2 \\
0 & 3 & 4 & 0 & 3 \\
2 & 1 & 5 & 2 & 1
\end{array}
$$

* **Sum of the downward (main) diagonals:**

$$
(1)(3)(5) + (2)(4)(2) + (-1)(0)(1) = 15 + 16 + 0 = 31
$$

* **Sum of the upward (anti-) diagonals:**

$$
(2)(3)(-1) + (1)(4)(1) + (5)(0)(2) = -6 + 4 + 0 = -2
$$

* **Determinant calculation:**

$$
\det(A) = 31 - (-2) = 31 + 2 = 33
$$

---

### 2. Simple Check Using a Determinant Property

We verify the result using the **row operation invariance property**[span_4](start_span)[span_4](end_span): adding a scalar multiple of one row to another row does not change the determinant ($R_3 \to R_3 - 2R_1$).

* **Perform $R_3 \to R_3 - 2R_1$:**

$$
(2, 1, 5) - 2(1, 2, -1) = (2 - 2, \, 1 - 4, \, 5 - (-2)) = (0, -3, 7)
$$

The transformed matrix is:

$$
\tilde{A} = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & 3 & 4 \\\ 0 & -3 & 7 \end{pmatrix}
$$

* **Expand along the first column** (which now has two zeros):

$$
\det(A) = \det(\tilde{A}) = 1 \cdot \det \begin{pmatrix} 3 & 4 \\\ -3 & 7 \end{pmatrix} = (3)(7) - (4)(-3) = 21 - (-12) = 33
$$

Both methods yield $\det(A) = 33$, confirming the calculation[span_5](start_span)[span_5](end_span).

---

### Conclusion

* **Determinant via Sarrus' rule:**

$$
\det(A) = 33
$$

* **Verification:** Applying the row operation $R_3 \to R_3 - 2R_1$ preserves the determinant and confirms $\det(A) = 33$[span_6](start_span)[span_6](end_span).
