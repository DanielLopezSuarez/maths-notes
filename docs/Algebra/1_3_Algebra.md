# 1.3 Algebra: The Inverse Matrix

This section explains how to "divide" matrices using the Inverse Matrix ($A^{-1}$). We cover the concept, the Cofactor method, and the Gauss-Jordan elimination method.

## Topic 1: The Concept of the Inverse

### Step 1: Definition & Analogy

**Arithmetic Analogy:**
In numbers, the multiplicative inverse of 5 is $1/5$ because $5 \times 1/5 = 1$. The number **1** is the "identity" because it leaves numbers unchanged.

**Matrix Definition:**
For a square matrix $A$, the inverse (written $A^{-1}$) is the matrix you multiply by $A$ to get the **Identity Matrix** ($I$).
* **Identity Matrix ($I$):** A square matrix with 1s on the diagonal and 0s elsewhere.
  $$I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$$

**The Rule:**
$$A \times A^{-1} = A^{-1} \times A = I$$

### Step 2: Singular vs. Nonsingular

* **Nonsingular:** A matrix that **has** an inverse ($\det(A) \neq 0$).
* **Singular:** A matrix that **does not** have an inverse ($\det(A) = 0$).

**Why is this important?**
The inverse allows us to solve matrix equations. To solve $A\mathbf{x} = \mathbf{b}$, we multiply by $A^{-1}$:
$$\mathbf{x} = A^{-1}\mathbf{b}$$

### Step 3: Verification Example

Let's check if $B$ is the inverse of $A$.
$A = \begin{bmatrix} 2 & 1 \\ 5 & 3 \end{bmatrix}, \quad B = \begin{bmatrix} 3 & -1 \\ -5 & 2 \end{bmatrix}$

Compute $A \times B$:
1.  **Top-Left:** $(2)(3) + (1)(-5) = 6-5 = \mathbf{1}$
2.  **Top-Right:** $(2)(-1) + (1)(2) = -2+2 = \mathbf{0}$
3.  **Bottom-Left:** $(5)(3) + (3)(-5) = 15-15 = \mathbf{0}$
4.  **Bottom-Right:** $(5)(-1) + (3)(2) = -5+6 = \mathbf{1}$

**Result:** $\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$. Yes, $B$ is the inverse ($A^{-1}$).

---

## Topic 2: The Cofactor Method (Formula Based)

### The Formula
$$A^{-1} = \frac{1}{\det(A)} \text{adj}(A)$$

### Step 1: The 5-Step Process
1.  **Determinant:** Calculate $\det(A)$. If 0, stop (no inverse).
2.  **Matrix of Minors ($M$):** Replace every element with the determinant of its sub-matrix (delete its row/col).
3.  **Cofactor Matrix ($C$):** Apply the "Checkerboard of Signs" to $M$.
    $$\begin{bmatrix} + & - & + \\ - & + & - \\ + & - & + \end{bmatrix}$$
4.  **Adjugate ($\text{adj}(A)$):** Transpose the Cofactor matrix ($C^T$).
5.  **Multiply:** Scale the adjugate by $1/\det(A)$.

### Step 2: Guided Calculation (3x3)

Calculate the inverse of $A = \begin{bmatrix} 1 & 2 & 3 \\ 0 & 1 & 4 \\ 5 & 6 & 0 \end{bmatrix}$.

**1. Determinant:**
$\det(A) = 1(0-24) - 2(0-20) + 3(0-5) = -24 + 40 - 15 = \mathbf{1}$.

**2. Matrix of Minors ($M$):**
$$
M = \begin{bmatrix}
(0-24) & (0-20) & (0-5) \\
(0-18) & (0-15) & (6-10) \\
(8-3) & (4-0) & (1-0)
\end{bmatrix} = \begin{bmatrix} -24 & -20 & -5 \\ -18 & -15 & -4 \\ 5 & 4 & 1 \end{bmatrix}
$$

**3. Cofactor Matrix ($C$):** (Apply signs)
$$
C = \begin{bmatrix} -24 & -(-20) & -5 \\ -(-18) & -15 & -(-4) \\ 5 & -4 & 1 \end{bmatrix} = \begin{bmatrix} -24 & 20 & -5 \\ 18 & -15 & 4 \\ 5 & -4 & 1 \end{bmatrix}
$$

**4. Adjugate Matrix ($C^T$):** (Swap rows/cols)
$$
\text{adj}(A) = \begin{bmatrix} -24 & 18 & 5 \\ 20 & -15 & -4 \\ -5 & 4 & 1 \end{bmatrix}
$$

**5. Final Inverse:**
Since $\det(A)=1$, $A^{-1} = \text{adj}(A)$.

### Step 3: The 2x2 Shortcut
For $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$:
$$A^{-1} = \frac{1}{ad-bc} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$$

---

## Topic 3: Gauss-Jordan Elimination (Row Operations)

### Step 1: The Setup
Create an **Augmented Matrix** $[A | I]$ placing the Identity matrix next to $A$.
Goal: Use row operations to transform the left side into $I$. The right side will become $A^{-1}$.
$$[A | I] \xrightarrow{\text{Row Ops}} [I | A^{-1}]$$

### Step 2: Guided Calculation
Find inverse of $A = \begin{bmatrix} 1 & 3 & 3 \\ 1 & 4 & 3 \\ 1 & 3 & 4 \end{bmatrix}$.

**0. Setup:**
$$
\left[ \begin{array}{ccc|ccc} 1 & 3 & 3 & 1 & 0 & 0 \\ 1 & 4 & 3 & 0 & 1 & 0 \\ 1 & 3 & 4 & 0 & 0 & 1 \end{array} \right]
$$

**1. Zeros in Col 1:** ($R_2 - R_1$ and $R_3 - R_1$)
$$
\left[ \begin{array}{ccc|ccc} 1 & 3 & 3 & 1 & 0 & 0 \\ 0 & 1 & 0 & -1 & 1 & 0 \\ 0 & 0 & 1 & -1 & 0 & 1 \end{array} \right]
$$

**2. Zeros in Col 2:** ($R_1 - 3R_2$)
$$
\left[ \begin{array}{ccc|ccc} 1 & 0 & 3 & 4 & -3 & 0 \\ 0 & 1 & 0 & -1 & 1 & 0 \\ 0 & 0 & 1 & -1 & 0 & 1 \end{array} \right]
$$

**3. Zeros in Col 3:** ($R_1 - 3R_3$)
$$
\left[ \begin{array}{ccc|ccc} \mathbf{1} & \mathbf{0} & \mathbf{0} & 7 & -3 & -3 \\ \mathbf{0} & \mathbf{1} & \mathbf{0} & -1 & 1 & 0 \\ \mathbf{0} & \mathbf{0} & \mathbf{1} & -1 & 0 & 1 \end{array} \right]
$$

**Result:** $A^{-1} = \begin{bmatrix} 7 & -3 & -3 \\ -1 & 1 & 0 \\ -1 & 0 & 1 \end{bmatrix}$.

---

## Comparison & Applications

### Which method to use?
* **2x2 Matrices:** Use the **Cofactor Formula** (Fastest).
* **3x3 Matrices:** Use **Gauss-Jordan** (Less messy arithmetic).
* **Computers:** Use **Gauss-Jordan** (Complexity is $O(n^3)$ vs $O(n!)$ for cofactors).

### Python Implementation
Finding an inverse using NumPy:

```python
import numpy as np
import numpy.linalg as LA

# Define Matrix
A = np.array([
    [1, 2, 3],
    [0, 1, 4],
    [5, 6, 0]
])

# Compute Inverse
A_inv = LA.inv(A)

print(A_inv)