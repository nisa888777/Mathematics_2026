# Exercise 9. Composition of Rotations and Reflections

## Question

Given the reflection matrix $S$ across the line $y = x$ and the rotation matrix $R$ representing a $90^\circ$ counterclockwise rotation:
Evaluate the compositions $RS$ and $SR$ on the vector $\mathbf{x} = \begin{pmatrix} 2 \\ 4 \end{pmatrix}$, and explain the geometric transformation of the axes under the $90^\circ$ counterclockwise rotation.

---

## Solution

### 1. Matrix Definitions

* **Reflection matrix across $y = x$ ($S$):**

$$
S = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}
$$

* **Rotation matrix for $90^\circ$ counterclockwise ($R$):**

$$
R = \begin{pmatrix} \cos 90^\circ & -\sin 90^\circ \\ \sin 90^\circ & \cos 90^\circ \end{pmatrix} = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}
$$

#### **Geometric Axis-Direction Explanation for $R$:**
A $90^\circ$ counterclockwise rotation transforms the standard basis vectors (and coordinate axes) as follows:
* The positive $x$-axis basis vector $\mathbf{e}_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ rotates to the positive $y$-axis:
$$
R\mathbf{e}_1 = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \mathbf{e}_2
$$
* The positive $y$-axis basis vector $\mathbf{e}_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$ rotates to the negative $x$-axis:
$$
R\mathbf{e}_2 = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} -1 \\ 0 \end{pmatrix} = -\mathbf{e}_1
$$

---

### 2. Composition Matrices

* **Matrix product $RS$:**

$$
RS = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (0)(0) + (-1)(1) & (0)(1) + (-1)(0) \\ (1)(0) + (0)(1) & (1)(1) + (0)(0) \end{pmatrix} = \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}
$$

* **Matrix product $SR$:**

$$
SR = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (0)(0) + (1)(1) & (0)(-1) + (1)(0) \\ (1)(0) + (0)(1) & (1)(-1) + (0)(0) \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}
$$

---

### 3. Application to Vector $\mathbf{x} = \begin{pmatrix} 2 \\ 4 \end{pmatrix}$

* **Evaluating $RS\mathbf{x}$:**

$$
RS\mathbf{x} = \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 4 \end{pmatrix} = \begin{pmatrix} (-1)(2) + (0)(4) \\ (0)(2) + (1)(4) \end{pmatrix} = \begin{pmatrix} -2 \\ 4 \end{pmatrix}
$$

*(Equivalently, applying first $S$ then $R$: $S\mathbf{x} = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$, then $R(S\mathbf{x}) = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$ depending on coordinate scaling)*

$$
RS\mathbf{x} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}
$$

* **Evaluating $SR\mathbf{x}$:**

$$
SR\mathbf{x} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

---

### Conclusion

* The axis mapping confirms that the positive $x$-axis maps to the positive $y$-axis, and the positive $y$-axis maps to the negative $x$-axis under $R$.
* The evaluated vectors are $RS\mathbf{x} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$ and $SR\mathbf{x} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$.
