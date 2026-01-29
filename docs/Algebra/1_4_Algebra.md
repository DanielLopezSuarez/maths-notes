# 1.4 Algebra: Systems of Linear Equations

This final algebra section connects everything we have learned. We will use matrices ($A$), vectors ($x, b$), determinants, and inverses to solve systems of linear equations.

## Topic 1: Systems in Matrix Form

### Step 1: The Translation

Any system of linear equations can be written as a single matrix equation:

$$
A \cdot x = b
$$

**Components:**
1.  **$A$ (Coefficient Matrix):** Contains the numbers multiplying the variables.
2.  **$x$ (Unknown Vector):** Contains the variables ($x, y, z$).
3.  **$b$ (Result Vector):** Contains the constants on the right side.

**Example:**

Consider this system:

$$
\begin{cases} 
2x + y - z = 8 \\ 
-3x - y + 2z = -11 \\ 
-2x + y + 2z = -3 
\end{cases}
$$

**Converted to Matrix Form:**

$$
\begin{pmatrix} 2 & 1 & -1 \\ -3 & -1 & 2 \\ -2 & 1 & 2 \end{pmatrix} \cdot \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 8 \\ -11 \\ -3 \end{pmatrix}
$$

### Step 2: Why do this?
* **Algebraic Power:** We can solve for $x$ symbolically: $x = A^{-1}b$.
* **Computers:** Software solves $Ax=b$ much faster than humans can use substitution.
* **Insight:** The determinant $\det(A)$ tells us immediately if a unique solution exists.

---

## Topic 2: Solution Methods

We have three main tools to solve $Ax=b$.

### Method 1: The Inverse Matrix Method

**Formula:** $x = A^{-1} \cdot b$
**Condition:** $\det(A) \neq 0$ (Matrix must be invertible).

**Example (2x2):**
System:

$$
\begin{cases} 5x + 2y = 4 \\ 7x + 3y = 5 \end{cases}
$$

1.  Calculate Determinant:
    $A = \begin{pmatrix} 5 & 2 \\ 7 & 3 \end{pmatrix}, \det(A) = 15 - 14 = 1$.

2.  Calculate Inverse:

    $$
    A^{-1} = \frac{1}{1} \begin{pmatrix} 3 & -2 \\ -7 & 5 \end{pmatrix}
    $$

3.  Solve:

    $$
    x = \begin{pmatrix} 3 & -2 \\ -7 & 5 \end{pmatrix} \begin{pmatrix} 4 \\ 5 \end{pmatrix} = \begin{pmatrix} 12-10 \\ -28+25 \end{pmatrix} = \begin{pmatrix} 2 \\ -3 \end{pmatrix}
    $$

**Solution:** $x=2, y=-3$.

### Method 2: Cramer’s Rule

**Formula:** $x_i = \frac{\det(A_i)}{\det(A)}$
**Condition:** $\det(A) \neq 0$.

**Example (Same 2x2):**

1.  **Main Determinant ($W$):**

    $$
    \det \begin{pmatrix} 5 & 2 \\ 7 & 3 \end{pmatrix} = 1
    $$

2.  **$W_x$ (Swap col 1 with $b$):**

    $$
    \det \begin{pmatrix} \mathbf{4} & 2 \\ \mathbf{5} & 3 \end{pmatrix} = 12 - 10 = 2
    $$

3.  **$W_y$ (Swap col 2 with $b$):**

    $$
    \det \begin{pmatrix} 5 & \mathbf{4} \\ 7 & \mathbf{5} \end{pmatrix} = 25 - 28 = -3
    $$

**Solution:** $x = \frac{2}{1} = 2, \quad y = \frac{-3}{1} = -3$.

### Method 3: Gaussian Elimination (The Universal Tool)

**Concept:** Form an **Augmented Matrix** $[A|b]$ and use row operations to create a "staircase" of zeros. Then use back-substitution.
**Condition:** Works for **ALL** systems (even if determinant is 0 or matrix is not square).

**Example (3x3):**
System:

$$
\begin{cases} x + y + 2z = 9 \\ 2x + 4y - 3z = 1 \\ 3x + 6y - 5z = 0 \end{cases}
$$

**1. Augmented Matrix:**

$$
\left(\begin{array}{ccc|c} 1 & 1 & 2 & 9 \\ 2 & 4 & -3 & 1 \\ 3 & 6 & -5 & 0 \end{array}\right)
$$

**2. Row Reduction:**

* $R_2 \to R_2 - 2R_1$
* $R_3 \to R_3 - 3R_1$

$$
\left(\begin{array}{ccc|c} 1 & 1 & 2 & 9 \\ 0 & 2 & -7 & -17 \\ 0 & 3 & -11 & -27 \end{array}\right)
$$

* ... (After simplifying) ...

$$
\left(\begin{array}{ccc|c} 1 & 1 & 2 & 9 \\ 0 & 1 & -3.5 & -8.5 \\ 0 & 0 & 1 & 3 \end{array}\right)
$$

**3. Back Substitution:**
* From $R_3$: **$z = 3$**
* From $R_2$: $y - 3.5(3) = -8.5 \implies$ **$y = 2$**
* From $R_1$: $x + 2 + 2(3) = 9 \implies$ **$x = 1$**

---

## Topic 3: Comparing the Methods

| Method | Best For... | Non-Square Systems? | No/Infinite Solutions? |
| :--- | :--- | :--- | :--- |
| **Cramer's Rule** | Simple 2x2 or 3x3 systems by hand. | No | Fails (Div by 0) |
| **Inverse Matrix** | Solving $Ax=b$ for many different $b$ vectors. | No | Fails (Div by 0) |
| **Gaussian Elim.** | **Everything.** Large systems, computers, complex cases. | **Yes** | **Yes** (Detects them) |

**Diagnostics with Gauss:**
* **Inconsistent (No Solution):** You get a row like $[0 \ 0 \ 0 \ | \ 5]$ ($0=5$, impossible).
* **Underdetermined (Infinite Solutions):** You get a row like $[0 \ 0 \ 0 \ | \ 0]$ (Useless info, fewer equations than variables).

---

## Finale: Comprehensive Test

**Task 1: Cramer's Rule**
Solve:

$$
\begin{cases} 4x - 3y = 1 \\ 2x + y = 3 \end{cases}
$$

* $W = 10, W_x = 10, W_y = 10$.
* **Result:** $x=1, y=1$.

**Task 2: Inverse Matrix**
Solve:

$$
\begin{cases} 2x + 9y = 1 \\ x + 5y = 0 \end{cases}
$$

* Inverse:

$$
A^{-1} = \begin{pmatrix} 5 & -9 \\ -1 & 2 \end{pmatrix}
$$

* **Result:** $x=5, y=-1$.

**Task 3: Gaussian Elimination**
Solve:

$$
\begin{cases} x + 2y + 2z = 3 \\ 2x + 5y + 7z = 1 \\ -x - y + 2z = 8 \end{cases}
$$

* After reduction: $z=16 \to y=-53 \to x=77$.
* **Result:** $x=77, y=-53, z=16$.

---

## Applications & Code

**Real Life: Feed Mixing**
A farmer needs a mix with specific protein and vitamins.
* Feed A: 2 protein, 4 vitamin.
* Feed B: 5 protein, 3 vitamin.
* Target: 24 protein, 26 vitamin.

System:

$$
\begin{cases} 2x + 5y = 24 \\ 4x + 3y = 26 \end{cases}
$$

Solution: $x \approx 4.14$ kg (Feed A), $y \approx 3.14$ kg (Feed B).

**Python Implementation:**
Solving a system using NumPy is the standard way engineers do this daily.

```python
import numpy as np

# Define A (Coefficients) and b (Results)
A = np.array([
    [1, 1, 2],
    [2, 4, -3],
    [3, 6, -5]
])
b = np.array([9, 1, 0])

# Solve
try:
    x = np.linalg.solve(A, b)
    print(f"Solution: {x}") 
    # Output: [1. 2. 3.]
except np.linalg.LinAlgError:
    print("System has no unique solution")