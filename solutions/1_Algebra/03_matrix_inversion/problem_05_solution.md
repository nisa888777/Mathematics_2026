# Exercise 5. A $3 \times 3$ Matrix

## Question

Use Gauss–Jordan elimination to find the inverse of

$$
A = \begin{pmatrix} 1 & 1 & 0 \\\ 0 & 1 & 1 \\\ 1 & 0 & 1 \end{pmatrix}.
$$

Check the result by multiplication.

---

## Solution

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix} 1 & 1 & 0 \\\ 0 & 1 & 1 \\\ 1 & 0 & 1 \end{pmatrix}
$$

To find $A^{-1}$ using Gauss–Jordan elimination, we form the augmented matrix $[A \mid I]$ using the $3 \times 3$ identity matrix $I$ and apply elementary row operations until the left side becomes $I$:

$$
[A \mid I] = \left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\ 0 & 1 & 1 & 0 & 1 & 0 \\\ 1 & 0 & 1 & 0 & 0 & 1 \end{array}\right)
$$

---

### 1. Step-by-Step Row Operations

* **Step 1:** Eliminate the entry below the pivot in Column 1 using $R_3 \leftarrow R_3 - R_1$:

$$
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\ 0 & 1 & 1 & 0 & 1 & 0 \\\ 1 - 1 & 0 - 1 & 1 - 0 & 0 - 1 & 0 - 0 & 1 - 0 \end{array}\right) = \left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\ 0 & 1 & 1 & 0 & 1 & 0 \\\ 0 & -1 & 1 & -1 & 0 & 1 \end{array}\right)
$$

* **Step 2:** Eliminate the entry below the pivot in Column 2 using $R_3 \leftarrow R_3 + R_2$:

$$
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\ 0 & 1 & 1 & 0 & 1 & 0 \\\ 0 + 0 & -1 + 1 & 1 + 1 & -1 + 0 & 0 + 1 & 1 + 0 \end{array}\right) = \left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\ 0 & 1 & 1 & 0 & 1 & 0 \\\ 0 & 0 & 2 & -1 & 1 & 1 \end{array}\right)
$$

* **Step 3:** Scale Row 3 to create a leading $1$ in Column 3 using $R_3 \leftarrow \frac{1}{2} R_3$:

$$
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\ 0 & 1 & 1 & 0 & 1 & 0 \\\ 0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{array}\right)
$$

* **Step 4:** Eliminate the entry above the pivot in Column 3 using $R_2 \leftarrow R_2 - R_3$:

$$
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\ 0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\\ 0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{array}\right)
$$

* **Step 5:** Eliminate the entry above the pivot in Column 2 using $R_1 \leftarrow R_1 - R_2$:

$$
\left(\begin{array}{ccc|ccc} 1 & 0 & 0 & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\\ 0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\\ 0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{array}\right)
$$

Now the augmented matrix is in the form $[I \mid A^{-1}]$, giving:

$$
A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\\ \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\\ -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 1 & -1 & 1 \\\ 1 & 1 & -1 \\\ -1 & 1 & 1 \end{pmatrix}
$$

---

### 2. Check the Result by Multiplication

We verify that $A A^{-1} = I$:

$$
A A^{-1} = \begin{pmatrix} 1 & 1 & 0 \\\ 0 & 1 & 1 \\\ 1 & 0 & 1 \end{pmatrix} \cdot \frac{1}{2} \begin{pmatrix} 1 & -1 & 1 \\\ 1 & 1 & -1 \\\ -1 & 1 & 1 \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 1 & 1 & 0 \\\ 0 & 1 & 1 \\\ 1 & 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 & 1 \\\ 1 & 1 & -1 \\\ -1 & 1 & 1 \end{pmatrix}
$$

Computing the matrix product:

* Row 1: $(1 + 1 + 0, \ -1 + 1 + 0, \ 1 - 1 + 0) = (2, \ 0, \ 0)$
* Row 2: $(0 + 1 - 1, \ 0 + 1 + 1, \ 0 - 1 + 1) = (0, \ 2, \ 0)$
* Row 3: $(1 + 0 - 1, \ -1 + 0 + 1, \ 1 + 0 + 1) = (0, \ 0, \ 2)$

Multiplying by $\frac{1}{2}$:

$$
A A^{-1} = \frac{1}{2} \begin{pmatrix} 2 & 0 & 0 \\\ 0 & 2 & 0 \\\ 0 & 0 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\\ 0 & 1 & 0 \\\ 0 & 0 & 1 \end{pmatrix} = I
$$

Since $A A^{-1} = I$, the inverse matrix is verified.

---

### Conclusion

* The inverse of $A$ is:

$$
A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\\ \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\\ -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{pmatrix}
$$
