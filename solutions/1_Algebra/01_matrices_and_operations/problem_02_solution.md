
# Exercise 2. Addition and Scalar Multiplication

**Given:**

$$
A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \quad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
$$

---

### **1. Compute $A + B$**

$$
A + B = \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}
$$

---

### **2. Compute $A - B$**

$$
A - B = \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}
$$

---

### **3. Compute $3A - 2B$**

$$
3A = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}, \quad 2B = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
$$

$$
3A - 2B = \begin{pmatrix} 3-8 & 6-(-4) \\ -3-0 & 9-10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}
$$

---

### **4. Dimension Condition**
Matrix addition is performed entry-by-entry. Corresponding elements can only be paired if both matrices share the exact same number of rows and columns ($m \times n$).

---

### **Verification (C++)**
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<vector<int>> A = {{1, 2}, {-1, 3}};
    vector<vector<int>> B = {{4, -2}, {0, 5}};

    vector<vector<int>> add(2, vector<int>(2));
    vector<vector<int>> sub(2, vector<int>(2));
    vector<vector<int>> res(2, vector<int>(2));

    for (int i = 0; i < 2; ++i) {
        for (int j = 0; j < 2; ++j) {
            add[i][j] = A[i][j] + B[i][j];
            sub[i][j] = A[i][j] - B[i][j];
            res[i][j] = 3 * A[i][j] - 2 * B[i][j];
        }
    }
    return 0;
}
