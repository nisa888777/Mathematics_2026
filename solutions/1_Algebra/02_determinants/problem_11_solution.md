# Exercise 11. Shortening the Calculation with Row Operations

## Question

Compute

$$
\det \begin{pmatrix} 1 & 2 & 3 \\\ 1 & 3 & 4 \\\ 1 & 4 & 6 \end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

---

## Solution

Let the given matrix be denoted as $A$:

$$
A = \begin{pmatrix} 1 & 2 & 3 \\\ 1 & 3 & 4 \\\ 1 & 4 & 6 \end{pmatrix}
$$

To simplify the determinant calculation, we perform elementary row operations of the form $R_i \to R_i + c R_j$ ($i \neq j$). 

* **Rule on Determinant Invariance:**  
  Adding a scalar multiple of one row to another row does not change the determinant ($\det \text{ remains unchanged}$).

---

### Step 1: Create Zeros in the First Column

The first column has all entries equal to $1$. We use row 1 ($R_1$) as the pivot row to eliminate the entries below it.

**1. Operation $R_2 \to R_2 - R_1$:**
* **Effect on determinant:** Does not change the determinant.
* **Calculation:**

$$
(1, 3, 4) - (1, 2, 3) = (0, 1, 1)
$$

**2. Operation $R_3 \to R_3 - R_1$:**
* **Effect on determinant:** Does not change the determinant.
* **Calculation:**

$$
(1, 4, 6) - (1, 2, 3) = (0, 2, 3)
$$

After these operations, the determinant satisfies:

$$
\det(A) = \det \begin{pmatrix} 1 & 2 & 3 \\\ 0 & 1 & 1 \\\ 0 & 2 & 3 \end{pmatrix}
$$

---

### Step 2: Create a Zero in the Second Column

We now eliminate the entry in row 3, column 2 using row 2 ($R_2$).

**Operation $R_3 \to R_3 - 2R_2$:**
* **Effect on determinant:** Does not change the determinant.
* **Calculation:**

$$
(0, 2, 3) - 2(0, 1, 1) = (0, 2 - 2, 3 - 2) = (0, 0, 1)
$$

The matrix is now transformed into an upper triangular matrix $U$:

$$
U = \begin{pmatrix} 1 & 2 & 3 \\\ 0 & 1 & 1 \\\ 0 & 0 & 1 \end{pmatrix}
$$

Because every row operation performed was of type $R_i \to R_i + c R_j$, the determinant remains unchanged:

$$
\det(A) = \det(U)
$$

---

### Step 3: Compute the Determinant of the Triangular Matrix

The determinant of an upper triangular matrix is simply the product of its diagonal entries:

$$
\det(U) = 1 \cdot 1 \cdot 1 = 1
$$

Therefore:

$$
\det(A) = 1
$$

---

### Conclusion

* **Row Operations Performed:**
  * $R_2 \to R_2 - R_1$ (Determinant unchanged)
  * $R_3 \to R_3 - R_1$ (Determinant unchanged)
  * $R_3 \to R_3 - 2R_2$ (Determinant unchanged)
* **Final Result:**

$$
\det(A) = 1
$$
