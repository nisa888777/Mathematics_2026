# Exercise 13. Determinant by Elimination

## Question

Compute the determinant

$$
A = \begin{pmatrix} 1 & 2 & 3 \\\ 2 & 5 & 7 \\\ 1 & 0 & 2 \end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

---

## Solution

We reduce matrix $A$ to an upper triangular form using Gaussian elimination while tracking the effect of each row operation on the determinant.

* **Rule on Row Operations:**  
  Adding a scalar multiple of one row to another row ($R_i \to R_i + c R_j$, $i \neq j$) **does not change** the value of the determinant.

---

### Step 1: Eliminate Entries Below the First Pivot ($a_{11} = 1$)

**1. Operation $R_2 \to R_2 - 2R_1$:**
* **Effect on determinant:** Unchanged ($\det$ remains the same).
* **Calculation:**

$$
(2, 5, 7) - 2(1, 2, 3) = (2 - 2, \, 5 - 4, \, 7 - 6) = (0, 1, 1)
$$

**2. Operation $R_3 \to R_3 - R_1$:**
* **Effect on determinant:** Unchanged ($\det$ remains the same).
* **Calculation:**

$$
(1, 0, 2) - (1, 2, 3) = (1 - 1, \, 0 - 2, \, 2 - 3) = (0, -2, -1)
$$

After Step 1, the matrix becomes:

$$
A_1 = \begin{pmatrix} 1 & 2 & 3 \\\ 0 & 1 & 1 \\\ 0 & -2 & -1 \end{pmatrix}
$$

Since both operations preserved the determinant:

$$
\det(A) = \det(A_1)
$$

---

### Step 2: Eliminate the Entry Below the Second Pivot ($a_{22} = 1$)

**Operation $R_3 \to R_3 + 2R_2$:**
* **Effect on determinant:** Unchanged ($\det$ remains the same).
* **Calculation:**

$$
(0, -2, -1) + 2(0, 1, 1) = (0, \, -2 + 2, \, -1 + 2) = (0, 0, 1)
$$

The matrix is now in upper triangular form $U$:

$$
U = \begin{pmatrix} 1 & 2 & 3 \\\ 0 & 1 & 1 \\\ 0 & 0 & 1 \end{pmatrix}
$$

Since all three row operations were row additions of multiples, the determinant is completely preserved:

$$
\det(A) = \det(U)
$$

---

### Step 3: Compute the Determinant of the Upper Triangular Matrix

The determinant of an upper triangular matrix equals the product of its main diagonal entries:

$$
\det(U) = (1) \cdot (1) \cdot (1) = 1
$$

Therefore:

$$
\det(A) = 1
$$

---

### Conclusion

* **Summary of Row Operations and Effects:**
  1. $R_2 \to R_2 - 2R_1$ — Determinant unchanged.
  2. $R_3 \to R_3 - R_1$ — Determinant unchanged.
  3. $R_3 \to R_3 + 2R_2$ — Determinant unchanged.
* **Final Determinant Value:**

$$
\det(A) = 1
$$
