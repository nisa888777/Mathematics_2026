# Exercise 5. Row Operations

## Question

For

$$
A = \begin{pmatrix} 1 & 2 & 3 \\\ 2 & 1 & 0 \\\ -1 & 4 & 2 \end{pmatrix}
$$

find $\det(A)$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

---

## Solution

To compute $\det(A)$, we reduce matrix $A$ to an upper triangular form using elementary row operations and track their effects on the determinant:
* Adding a scalar multiple of one row to another row does not change the determinant ($\det \text{ remains unchanged}$).
* Swapping two rows multiplies the determinant by $-1$.
* Multiplying a row by a scalar $c$ multiplies the determinant by $c$.

---

### Step 1: Eliminate the first column below the diagonal

We use the pivot $a_{11} = 1$ in row 1:

1. **Operation $R_2 \to R_2 - 2R_1$:**  
   * **Effect on determinant:** Adding a multiple of row 1 to row 2 does not change the value of the determinant.
   * New row 2:
     $$
     (2, 1, 0) - 2(1, 2, 3) = (2 - 2, \, 1 - 4, \, 0 - 6) = (0, -3, -6)
     $$

2. **Operation $R_3 \to R_3 + R_1$:**  
   * **Effect on determinant:** Adding row 1 to row 3 does not change the value of the determinant.
   * New row 3:
     $$
     (-1, 4, 2) + (1, 2, 3) = (-1 + 1, \, 4 + 2, \, 2 + 3) = (0, 6, 5)
     $$

After these operations, the determinant satisfies:

$$
\det(A) = \det \begin{pmatrix} 1 & 2 & 3 \\\ 0 & -3 & -6 \\\ 0 & 6 & 5 \end{pmatrix}
$$

---

### Step 2: Eliminate the second column below the diagonal

We use the pivot in row 2 to eliminate the entry in row 3 ($a_{32} = 6$):

* **Operation $R_3 \to R_3 + 2R_2$:**  
  * **Effect on determinant:** Adding a multiple of row 2 to row 3 does not change the value of the determinant.
  * New row 3:
    $$
    (0, 6, 5) + 2(0, -3, -6) = (0 + 0, \, 6 - 6, \, 5 - 12) = (0, 0, -7)
    $$

The matrix is now in upper triangular form $U$:

$$
U = \begin{pmatrix} 1 & 2 & 3 \\\ 0 & -3 & -6 \\\ 0 & 0 & -7 \end{pmatrix}
$$

Since none of the elementary row operations performed changed the determinant:

$$
\det(A) = \det(U)
$$

---

### Step 3: Compute the determinant of the triangular matrix

The determinant of an upper triangular matrix is the product of its diagonal elements:

$$
\det(U) = (1) \cdot (-3) \cdot (-7) = 21
$$

Therefore:

$$
\det(A) = 21
$$

---

### Conclusion

* **Row Operations Performed:**
  * $R_2 \to R_2 - 2R_1$ (Determinant unchanged)
  * $R_3 \to R_3 + R_1$ (Determinant unchanged)
  * $R_3 \to R_3 + 2R_2$ (Determinant unchanged)
* **Final Result:**

$$
\det(A) = 21
$$
