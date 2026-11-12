# Exercise 3. Swapping Two Rows

## Question

For

$$
A = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 3 & 1 \\\ 2 & 1 & 1 \end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

---

## Solution

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 3 & 1 \\\ 2 & 1 & 1 \end{pmatrix}
$$

---

### 1. Computing $\det(A)$

We compute $\det(A)$ by cofactor expansion along the first row (which contains a zero entry):

$$
\det(A) = 1 \cdot \det \begin{pmatrix} 3 & 1 \\\ 1 & 1 \end{pmatrix} - 2 \cdot \det \begin{pmatrix} 0 & 1 \\\ 2 & 1 \end{pmatrix} + 0 \cdot \det \begin{pmatrix} 0 & 3 \\\ 2 & 1 \end{pmatrix}
$$

Evaluating the $2 \times 2$ determinants:

$$
\det \begin{pmatrix} 3 & 1 \\\ 1 & 1 \end{pmatrix} = (3)(1) - (1)(1) = 3 - 1 = 2
$$

$$
\det \begin{pmatrix} 0 & 1 \\\ 2 & 1 \end{pmatrix} = (0)(1) - (1)(2) = 0 - 2 = -2
$$

Substituting these values back:

$$
\det(A) = 1(2) - 2(-2) + 0 = 2 + 4 = 6
$$

---

### 2. Predicting $\det(B)$ Using a Determinant Property

Forming matrix $B$ by swapping the first and second rows of $A$ ($R_1 \leftrightarrow R_2$) gives:

$$
B = \begin{pmatrix} 0 & 3 & 1 \\\ 1 & 2 & 0 \\\ 2 & 1 & 1 \end{pmatrix}
$$

* **Determinant Property (Row Swap):**  
  Swapping any two rows of a square matrix multiplies its determinant by $-1$.

* **Prediction:**  
  Since $\det(A) = 6$, swapping two rows must negate the determinant:

$$
\det(B) = -\det(A) = -6
$$

---

### 3. Verifying $\det(B)$ by Direct Calculation

We compute $\det(B)$ by expanding along the first row of $B$:

$$
\det(B) = 0 \cdot \det \begin{pmatrix} 2 & 0 \\\ 1 & 1 \end{pmatrix} - 3 \cdot \det \begin{pmatrix} 1 & 0 \\\ 2 & 1 \end{pmatrix} + 1 \cdot \det \begin{pmatrix} 1 & 2 \\\ 2 & 1 \end{pmatrix}
$$

Evaluating the non-zero $2 \times 2$ determinants:

$$
\det \begin{pmatrix} 1 & 0 \\\ 2 & 1 \end{pmatrix} = (1)(1) - (0)(2) = 1
$$

$$
\det \begin{pmatrix} 1 & 2 \\\ 2 & 1 \end{pmatrix} = (1)(1) - (2)(2) = 1 - 4 = -3
$$

Substituting these values back:

$$
\det(B) = 0 - 3(1) + 1(-3) = -3 - 3 = -6
$$

This direct calculation matches our prediction $\det(B) = -6$.

---

### Conclusion

* **Determinant of $A$:**

$$
\det(A) = 6
$$

* **Predicted and Verified Determinant of $B$:**

$$
\det(B) = -6
$$

* **Summary:** Interchanging two rows reverses the sign of the determinant, confirming $\det(B) = -\det(A)$.
