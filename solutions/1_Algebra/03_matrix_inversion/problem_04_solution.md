# Exercise 4. Gauss–Jordan

## Question

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A = \begin{pmatrix} 1 & 2 \\\ 3 & 5 \end{pmatrix}.
$$

Show the augmented matrix $[A \mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

---

## Solution

We are given the $2 \times 2$ matrix:

$$
A = \begin{pmatrix} 1 & 2 \\\ 3 & 5 \end{pmatrix}
$$

To find $A^{-1}$ via Gauss–Jordan elimination, we form the augmented matrix $[A \mid I]$ using the $2 \times 2$ identity matrix $I$ and apply elementary row operations until the left side becomes $I$:

$$
[A \mid I] = \left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\\ 3 & 5 & 0 & 1 \end{array}\right)
$$

---

### 1. Step-by-Step Row Operations

* **Step 1:** Eliminate the entry below the pivot in Column 1 using $R_2 \leftarrow R_2 - 3R_1$:

$$
\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\\ 3 - 3(1) & 5 - 3(2) & 0 - 3(1) & 1 - 3(0) \end{array}\right) = \left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\\ 0 & -1 & -3 & 1 \end{array}\right)
$$

* **Step 2:** Scale Row 2 to create a leading $1$ in Column 2 using $R_2 \leftarrow -R_2$:

$$
\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\\ 0 & 1 & 3 & -1 \end{array}\right)
$$

* **Step 3:** Eliminate the entry above the pivot in Column 2 using $R_1 \leftarrow R_1 - 2R_2$:

$$
\left(\begin{array}{cc|cc} 1 - 2(0) & 2 - 2(1) & 1 - 2(3) & 0 - 2(-1) \\\ 0 & 1 & 3 & -1 \end{array}\right) = \left(\begin{array}{cc|cc} 1 & 0 & -5 & 2 \\\ 0 & 1 & 3 & -1 \end{array}\right)
$$

Now the augmented matrix is in the form $[I \mid A^{-1}]$, which yields:

$$
A^{-1} = \begin{pmatrix} -5 & 2 \\\ 3 & -1 \end{pmatrix}
$$

---

### 2. Why Obtaining $I$ on the Left Gives $A^{-1}$ on the Right

Each elementary row operation corresponds to multiplying the matrix on the left by an elementary matrix $E_k$. Performing $k$ row operations in sequence multiplies both blocks of $[A \mid I]$ by the product $E = E_k \cdots E_2 E_1$:

$$
E [A \mid I] = [EA \mid EI] = [EA \mid E]
$$

When the left block is reduced to the identity matrix, we have:

$$
EA = I
$$

By the definition of the matrix inverse, any matrix $E$ satisfying $EA = I$ is the inverse matrix $A^{-1}$. Consequently, the right block $EI = E$ is guaranteed to equal $A^{-1}$.

---

### Conclusion

* Applying Gauss–Jordan elimination transforms $[A \mid I]$ into $[I \mid A^{-1}]$.
* The inverse matrix is:

$$
A^{-1} = \begin{pmatrix} -5 & 2 \\\ 3 & -1 \end{pmatrix}
$$
