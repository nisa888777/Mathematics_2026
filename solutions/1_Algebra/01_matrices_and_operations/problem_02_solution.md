# Exercise 2. Addition and Scalar Multiplication

**Problem Statement:** For the given matrices:
$$A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \quad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}$$

Compute:
- **a)** $A + B$
- **b)** $A - B$
- **c)** $3A - 2B$

Explain why matrix addition is possible only for matrices of the same size.

---

### **I. Theoretical Core Concept**
Matrix addition, matrix subtraction, and scalar multiplication are defined component-wise (entry-by-entry).

- **Compatibility Condition:**
  Two matrices $X$ and $Y$ can be added or subtracted if and only if they share identical dimensions ($m \times n$).
  
- **Entry-by-Entry Definitions:**
  $$(X \pm Y)_{ij} = X_{ij} \pm Y_{ij}$$
  $$(c \cdot X)_{ij} = c \cdot X_{ij} \quad (c \in \mathbb{R})$$

---

### **II. Step-by-Step Evaluation**

#### **1. Addition ($A + B$)**
We add corresponding entries located at the exact same indices:
$$A + B = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} + \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 1 + 4 & 2 + (-2) \\ -1 + 0 & 3 + 5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$$

#### **2. Subtraction ($A - B$)**
We subtract the entries of matrix $B$ from matrix $A$:
$$A - B = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} - \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 1 - 4 & 2 - (-2) \\ -1 - 0 & 3 - 5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}$$

#### **3. Linear Combination ($3A - 2B$)**
First, evaluate scalar multiples $3A$ and $2B$:
$$3A = 3 \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}$$
$$2B = 2 \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}$$

Now compute the difference $3A - 2B$:
$$3A - 2B = \begin{pmatrix} 3 - 8 & 6 - (-4) \\ -3 - 0 & 9 - 10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}$$

---

### **III. Dimensional Restriction Explanation**
Matrix addition is strictly defined as an entry-by-entry operation where an element at position $(i, j)$ in matrix $A$ is mapped directly to the element at the identical position $(i, j)$ in matrix $B$. If the dimensions differ, at least one entry will lack a corresponding partner, making the algebraic addition undefined.

---

### **IV. Computational Verification (C++)**
```cpp
#include <iostream>
#include <vector>

using namespace std;

void printMat(const string& label, const vector<vector<int>>& M) {
    cout << label << ":\n";
    for (const auto& r : M) {
        for (int v : r) cout << v << "\t";
        cout << "\n";
    }
    cout << "\n";
}

int main() {
    vector<vector<int>> A = {{1, 2}, {-1, 3}};
    vector<vector<int>> B = {{4, -2}, {0, 5}};

    vector<vector<int>> add(2, vector<int>(2));
    vector<vector<int>> sub(2, vector<int>(2));
    vector<vector<int>> comb(2, vector<int>(2));

    for(int i = 0; i < 2; ++i) {
        for(int j = 0; j < 2; ++j) {
            add[i][j] = A[i][j] + B[i][j];
            sub[i][j] = A[i][j] - B[i][j];
            comb[i][j] = 3 * A[i][j] - 2 * B[i][j];
        }
    }

    printMat("A + B", add);
    printMat("A - B", sub);
    printMat("3A - 2B", comb);

    return 0;
}
