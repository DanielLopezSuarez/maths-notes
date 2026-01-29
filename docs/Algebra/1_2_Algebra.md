# 1.2 Algebra: Determinants

This section covers the concept of the determinant, its geometric interpretation, and methods for calculating it (Sarrus' rule, Laplace expansion, and Gaussian elimination).

## Topic 1: Definition & Interpretation

### Step 1: Building Intuition

**What is a determinant?**
The determinant is a single number calculated from a square matrix (e.g., $2 \times 2$, $3 \times 3$) that summarizes the matrix's scaling properties.

**Analogy:**
Think of a matrix as a transformation recipe.
* A $2 \times 2$ matrix transforms 2D shapes (like a $1 \times 1$ square).
* A $3 \times 3$ matrix transforms 3D shapes (like a $1 \times 1 \times 1$ cube).

The determinant is the **scaling factor** of this transformation:
* For a square, the determinant is the **area** of the new shape (parallelogram).
* For a cube, the determinant is the **volume** of the new shape (parallelepiped).

**Why only square matrices?**
A non-square matrix (e.g., $3 \times 2$) changes dimensions ($2D \to 3D$). You cannot define a single scaling factor for "area" or "volume" when the dimension itself changes.

**Geometric Interpretation of Sign:**
* **Positive ($det > 0$):** Preserves orientation (like rotating or stretching).
* **Negative ($det < 0$):** Reverses orientation (flips space like a mirror).
* **Zero ($det = 0$):** The transformation flattens space into a lower dimension (e.g., 3D $\to$ 2D plane). The matrix is **singular** (non-invertible).

### Step 2: Visual Example

Consider matrix $A$:

$$
A = \begin{bmatrix} 3 & 1 \\ 4 & 2 \end{bmatrix}
$$

* **Column Vectors:** $v_1 = \begin{bmatrix} 3 \\ 4 \end{bmatrix}$ and $v_2 = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$.
* **Geometric Shape:** These vectors form a parallelogram with vertices at $(0,0), (3,4), (1,2)$, and $(4,6)$.
* **Determinant Calculation:**

$$
det(A) = (3 \times 2) - (1 \times 4) = 6 - 4 = 2
$$

* **Conclusion:** The area of that parallelogram is exactly **2**.

### Step 3: Mini-quiz

1.  **Geometric Concept:** If a $3 \times 3$ matrix has a determinant of 0, what does this imply?
    * **Answer:** The three vectors are linearly dependent (they lie on the same plane or line), so the "volume" they form is 0.

2.  **True/False:** The determinant can be computed for any $m \times n$ matrix.
    * **Answer:** False. Only for square matrices ($n \times n$).

3.  **Analysis:** A matrix $B$ has $det(B) = -5$. What does this mean?
    * **Answer:** It scales the area/volume by a factor of 5, and it reverses orientation (flips the space).

---

## Topic 2: Sarrus’ Rule (2x2 and 3x3)

### Step 1: The 2x2 Formula

For a matrix $A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$:

$$
det(A) = ad - bc
$$

**Example:**

$$
A = \begin{bmatrix} 5 & 3 \\ 2 & 4 \end{bmatrix} \implies det(A) = (5 \times 4) - (3 \times 2) = 20 - 6 = 14
$$

### Step 2: The 3x3 Shortcut (Sarrus)

For a matrix $A$:
1.  Append the first two columns to the right of the matrix.
2.  Sum the products of the 3 diagonals from top-left to bottom-right (Positive).
3.  Subtract the products of the 3 diagonals from top-right to bottom-left (Negative).

**Calculation Example:**

Let $B$:

$$
B = \begin{bmatrix} 2 & 1 & 3 \\ -1 & 0 & 4 \\ 1 & 5 & -2 \end{bmatrix}
$$

**Append Columns:**

$$
\begin{array}{ccc|cc}
2 & 1 & 3 & 2 & 1 \\
-1 & 0 & 4 & -1 & 0 \\
1 & 5 & -2 & 1 & 5
\end{array}
$$

1.  **Positive Diagonals:**
    * $(2 \cdot 0 \cdot -2) = 0$
    * $(1 \cdot 4 \cdot 1) = 4$
    * $(3 \cdot -1 \cdot 5) = -15$
    * **Sum 1:** $0 + 4 - 15 = \mathbf{-11}$

2.  **Negative Diagonals:**
    * $(3 \cdot 0 \cdot 1) = 0$
    * $(2 \cdot 4 \cdot 5) = 40$
    * $(1 \cdot -1 \cdot -2) = 2$
    * **Sum 2:** $0 + 40 + 2 = \mathbf{42}$

3.  **Final Determinant:**

$$
det(B) = (-11) - (42) = -53
$$

### Step 3: Practice

Calculate $det(D)$ for:

$$
D = \begin{bmatrix} 1 & 0 & 4 \\ 2 & 1 & 1 \\ 3 & -1 & 2 \end{bmatrix}
$$

* **Positives:** $(1 \cdot 1 \cdot 2) + (0 \cdot 1 \cdot 3) + (4 \cdot 2 \cdot -1) = 2 + 0 - 8 = -6$
* **Negatives:** $(4 \cdot 1 \cdot 3) + (1 \cdot 1 \cdot -1) + (0 \cdot 2 \cdot 2) = 12 - 1 + 0 = 11$
* **Result:** $(-6) - (11) = \mathbf{-17}$

---

## Topic 3: Laplace Expansion (The Universal Method)

### Step 1: Minors and Cofactors

* **Minor ($M_{ij}$):** Determinant of the smaller matrix obtained by deleting row $i$ and column $j$.
* **Cofactor ($A_{ij}$):** The signed minor. Formula: $A_{ij} = (-1)^{i+j} M_{ij}$.

**Sign Checkerboard:**

$$
\begin{bmatrix} + & - & + \\ - & + & - \\ + & - & + \end{bmatrix}
$$

### Step 2: The Method

Select **one row or column** (ideally the one with the most zeros). Multiply each element by its cofactor and sum them up.

$$
det(A) = a_{i1}A_{i1} + a_{i2}A_{i2} + \dots + a_{in}A_{in}
$$

### Step 3: 4x4 Example

Compute the determinant of $C$ expanding along **Column 3** (because it has two zeros):

$$
C = \begin{bmatrix} 1 & 4 & \mathbf{0} & 2 \\ -1 & 2 & \mathbf{1} & 3 \\ 0 & 1 & \mathbf{0} & -1 \\ 3 & 0 & \mathbf{5} & 1 \end{bmatrix}
$$

Formula: $det(C) = 0 \cdot A_{13} + 1 \cdot A_{23} + 0 \cdot A_{33} + 5 \cdot A_{43}$.
Zeros cancel terms, so we just need: **$1 \cdot A_{23} + 5 \cdot A_{43}$**.

1.  **Find $A_{23}$:** Position (2,3) is odd ($2+3=5 \to$ Negative).

    $$
    M_{23} = det \begin{bmatrix} 1 & 4 & 2 \\ 0 & 1 & -1 \\ 3 & 0 & 1 \end{bmatrix} = -17
    $$

    $A_{23} = -(-17) = \mathbf{17}$

2.  **Find $A_{43}$:** Position (4,3) is odd ($4+3=7 \to$ Negative).

    $$
    M_{43} = det \begin{bmatrix} 1 & 4 & 2 \\ -1 & 2 & 3 \\ 0 & 1 & -1 \end{bmatrix} = -11
    $$

    $A_{43} = -(-11) = \mathbf{11}$

**Final Result:** $1(17) + 5(11) = 17 + 55 = \mathbf{72}$.

---

## Topic 4: Gaussian Method (Row Operations)

### Step 1: The Concept

Transform the matrix into an **Upper Triangular Form** (zeros below diagonal) using row operations. The determinant is then just the **product of the diagonal elements**.

**Rules:**
1.  **Add row to row:** Determinant **does not change** (Best operation!).
2.  **Swap rows:** Determinant is **negated** ($\times -1$).
3.  **Scale row:** Determinant is multiplied by scalar $k$.

### Step 2: Example Calculation

Compute $det(A)$:

$$
A = \begin{bmatrix} 1 & 2 & 0 & 1 \\ 2 & 5 & 1 & 3 \\ -1 & 1 & 2 & 1 \\ 0 & 2 & 1 & 1 \end{bmatrix}
$$

1.  **Clear Col 1:** $R_2 \to R_2 - 2R_1$ and $R_3 \to R_3 + R_1$.

    $$
    \begin{bmatrix} 1 & 2 & 0 & 1 \\ 0 & 1 & 1 & 1 \\ 0 & 3 & 2 & 2 \\ 0 & 2 & 1 & 1 \end{bmatrix}
    $$

2.  **Clear Col 2:** $R_3 \to R_3 - 3R_2$ and $R_4 \to R_4 - 2R_2$.

    $$
    \begin{bmatrix} 1 & 2 & 0 & 1 \\ 0 & 1 & 1 & 1 \\ 0 & 0 & -1 & -1 \\ 0 & 0 & -1 & -1 \end{bmatrix}
    $$

3.  **Clear Col 3:** $R_4 \to R_4 - R_3$.

    $$
    \begin{bmatrix} 1 & 2 & 0 & 1 \\ 0 & 1 & 1 & 1 \\ 0 & 0 & -1 & -1 \\ 0 & 0 & 0 & 0 \end{bmatrix}
    $$

**Result:** Diagonal product $\rightarrow 1 \times 1 \times (-1) \times 0 = \mathbf{0}$.

---

## Topic 5: Applications & Review

### Cramer's Rule (Solving Systems)

Used to solve $Ax = b$. Each variable is a ratio of determinants:

$$
x_i = \frac{det(A_i)}{det(A)}
$$

**Example System:**
$3x + y = 9$
$2x + 4y = 8$

1.  **$det(A)$:**

    $$
    \begin{vmatrix} 3 & 1 \\ 2 & 4 \end{vmatrix} = 10
    $$

2.  **$det(A_x)$** (Replace col 1 with constants):

    $$
    \begin{vmatrix} 9 & 1 \\ 8 & 4 \end{vmatrix} = 28 \implies x = 28/10 = \mathbf{2.8}
    $$

3.  **$det(A_y)$** (Replace col 2 with constants):

    $$
    \begin{vmatrix} 3 & 9 \\ 2 & 8 \end{vmatrix} = 6 \implies y = 6/10 = \mathbf{0.6}
    $$

### Python Implementation

How to compute a determinant in Python using NumPy:

```python
import numpy as np

# Define matrix
B = np.array([
    [2, -1, 0],
    [1, 3, 1],
    [4, 0, 5]
])

# Compute Determinant
det = np.linalg.det(B)

print(f"Determinant: {det}")
# Output: 31.0