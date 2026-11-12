# Exercise 4. Triangular Matrix

## Question

Without expanding the determinant, compute

$$
\det \begin{pmatrix} 2 & 4 & 1 \\\ 0 & -3 & 5 \\\ 0 & 0 & 7 \end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

---

## Solution

Let the given matrix be denoted as $U$:

$$
U = \begin{pmatrix} 2 & 4 & 1 \\\ 0 & -3 & 5 \\\ 0 & 0 & 7 \end{pmatrix}
$$

---

### 1. General Rule for an Arbitrary Triangular Matrix

* **Rule:**  
  The determinant of any square upper triangular, lower triangular, or diagonal $n \times n$ matrix $T = [t_{ij}]$ is equal to the **product of its main diagonal entries**:

$$
\det(T) = t_{11} \cdot t_{22} \cdots t_{nn} = \prod_{i=1}^{n} t_{ii}
$$

* **Why This Rule Holds:**  
  In an upper triangular matrix, all entries strictly below the main diagonal are zero ($t_{ij} = 0$ for all $i > j$). When computing the determinant recursively along the first column at each step, only the diagonal entry has a non-zero contribution, leaving the next smaller triangular submatrix until only the product of the diagonal entries remains.

---

### 2. Application to the Given Example

Observing the structure of matrix $U$:
* All entries below the main diagonal are zero ($u_{21} = 0$, $u_{31} = 0$, $u_{32} = 0$), so $U$ is an **upper triangular matrix**.
* Its main diagonal entries are $u_{11} = 2$, $u_{22} = -3$, and $u_{33} = 7$.

Applying the triangular matrix rule directly without full cofactor expansion:

$$
\det(U) = (2) \cdot (-3) \cdot (7) = -42
$$

Notice that the entries above the main diagonal ($4$, $1$, and $5$) do not affect the value of the determinant.

---

### Conclusion

* **General Rule:** For any triangular matrix, $\det(T)$ equals the product of its main diagonal elements.
* **Determinant Value:**

$$
\det \begin{pmatrix} 2 & 4 & 1 \\\ 0 & -3 & 5 \\\ 0 & 0 & 7 \end{pmatrix} = -42
$$
