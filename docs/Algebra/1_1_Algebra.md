# 1.1 Algebra: Fundamentals of Matrices

This section covers the foundational concepts of matrices, including definitions, types, and basic arithmetic operations.

## Topic 1: What is a matrix? Definitions and basics

### Step 1: Building intuition

**Analogy:**
A matrix is essentially an organized grid of information. Think of a **Digital Image**: an image is a matrix where each "entry" is a pixel. The rows and columns tell the computer exactly where that pixel is located, and the number inside tells it what color to display.

**Basic Definitions:**

* **Row:** The horizontal arrangement of numbers.
* **Column:** The vertical arrangement of numbers.
* **Entry (Element):** An individual number at a specific intersection.
* **Dimension:** Expressed as $m \times n$ ($rows \times columns$).

**Example Matrix $A$ ($2 \times 3$):**

$$
A = \begin{bmatrix} 1 & 5 & 9 \\ 7 & 3 & 2 \end{bmatrix}
$$

* **Dimension:** $2 \times 3$ (2 rows, 3 columns).
* **Entry $a_{12}$:** The number in the 1st row, 2nd column is **5**.

### Step 2: Practice Exercise

Consider the following matrix $A$:

$$
A = \begin{bmatrix} 12 & 7 & 1 & 19 \\ 8 & 3 & 4 & 22 \\ 15 & 6 & 0 & 11 \end{bmatrix}
$$

* **Task 1:** Find entry $a_{23}$ (2nd row, 3rd column).
    * *Solution:* **4**
* **Task 2:** Find entry $a_{14}$ (1st row, 4th column).
    * *Solution:* **19**

### Step 3: Mini-quiz

1.  **True/False:** A $4 \times 1$ matrix is a single column.
    * *Answer:* **True** (4 rows, 1 column).
2.  **Calculation:** How many entries are in a $10 \times 2$ matrix?
    * *Answer:* **20** entries.
3.  **Identification:** In the matrix $\begin{bmatrix} 9 & 8 \\ 7 & 6 \end{bmatrix}$, what is the entry in the first row, second column?
    * *Answer:* **8**.

---

## Topic 2: Special Matrices

### Step 1: Building intuition

* **Square Matrix:** Rows = Columns (e.g., $2 \times 2$).
* **Zero Matrix:** All entries are $0$.
* **Diagonal Matrix:** A square matrix where all entries are $0$ except those on the main diagonal.
* **Identity Matrix ($I$):** A diagonal matrix where all diagonal entries are $1$.
* **Transpose ($A^T$):** Formed by swapping rows with columns.

**Visualizing Transpose:**
Start with $A$ ($3 \times 2$):

$$
A = \begin{bmatrix} a & b \\ c & d \\ e & f \end{bmatrix}
$$

To transpose ($A^T$):
1. Take Row 1 $[a, b]$ $\rightarrow$ becomes Column 1.
2. Take Row 2 $[c, d]$ $\rightarrow$ becomes Column 2.
3. Take Row 3 $[e, f]$ $\rightarrow$ becomes Column 3.

Result $A^T$ ($2 \times 3$):

$$
A^T = \begin{bmatrix} a & c & e \\ b & d & f \end{bmatrix}
$$

### Step 2: Practice Exercises

**Exercise 1:** Transpose Matrix $B$.

$$
B = \begin{bmatrix} 1 & 2 & 3 & 4 \\ 0 & 1 & 0 & 1 \\ 5 & 5 & 5 & 5 \\ 2 & 4 & 6 & 8 \end{bmatrix}
$$

* *Solution ($B^T$):*
    $$
    B^T = \begin{bmatrix} 1 & 0 & 5 & 2 \\ 2 & 1 & 5 & 4 \\ 3 & 0 & 5 & 6 \\ 4 & 1 & 5 & 8 \end{bmatrix}
    $$

**Exercise 2:** Identify the matrix type.

$$
M = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}
$$

* *Solution:* This is an **Identity Matrix** (It is also technically a diagonal and square matrix).

### Step 3: Mini-quiz

Identify the type of the following matrices:

1.  $\begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}$ $\rightarrow$ **Zero Matrix**
2.  $\begin{bmatrix} 7 & 0 & 0 \\ 0 & 8 & 0 \\ 0 & 0 & 9 \end{bmatrix}$ $\rightarrow$ **Diagonal Matrix**
3.  $\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$ $\rightarrow$ **Identity Matrix**
4.  $\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$ $\rightarrow$ **Square Matrix**

---

## Topic 3: Addition, Subtraction & Scalar Multiplication

### Step 1: Rules

**Addition/Subtraction:**
* **Condition:** Matrices must have the **exact same dimensions**.
* **Action:** Add or subtract corresponding entries.
* *Example:* $\begin{bmatrix} 1 & 2 \end{bmatrix} + \begin{bmatrix} 3 & 4 \end{bmatrix} = \begin{bmatrix} 4 & 6 \end{bmatrix}$.

**Scalar Multiplication:**
Multiplying a matrix by a number (scalar) means multiplying **every single element** by that number.

$$
5 \times \begin{bmatrix} 2 & 4 \\ 1 & 0 \end{bmatrix} = \begin{bmatrix} 10 & 20 \\ 5 & 0 \end{bmatrix}
$$

### Step 2: Practice Calculation

Compute $2A - B$ given:
$A = \begin{bmatrix} 1 & 1 & 1 \\ 2 & 2 & 2 \\ 3 & 3 & 3 \end{bmatrix}, \quad B = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$

1.  Calculate $2A$: $\begin{bmatrix} 2 & 2 & 2 \\ 4 & 4 & 4 \\ 6 & 6 & 6 \end{bmatrix}$
2.  Subtract $B$:
    $$
    \begin{bmatrix} 2-1 & 2-0 & 2-0 \\ 4-0 & 4-1 & 4-0 \\ 6-0 & 6-0 & 6-1 \end{bmatrix}
    $$
3.  **Final Answer:**
    $$
    \begin{bmatrix} 1 & 2 & 2 \\ 4 & 3 & 4 \\ 6 & 6 & 5 \end{bmatrix}
    $$

### Step 3: Mini-quiz (Spot the error)

1.  $10 \times \begin{bmatrix} 0.5 & 1 \end{bmatrix} = \begin{bmatrix} 5 & 10 \end{bmatrix}$ (Correct)
2.  $\begin{bmatrix} 5 & 5 \end{bmatrix} - \begin{bmatrix} 2 & 1 \end{bmatrix} = \begin{bmatrix} 3 & 4 \end{bmatrix}$ (Correct)
3.  $\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} + \begin{bmatrix} 1 & 2 \end{bmatrix}$ $\rightarrow$ **Impossible**. Dimensions ($2 \times 2$ vs $1 \times 2$) do not match.

### Step 4: Geometric Intuition
Imagine a square defined by vertices $(0,0), (1,0), (1,1), (0,1)$. The matrix of vertices is:
$$V = \begin{bmatrix} 0 & 1 & 1 & 0 \\ 0 & 0 & 1 & 1 \end{bmatrix}$$

* **Multiply by 2:** The square expands; side lengths double. Vertices become $(0,0), (2,0), (2,2), (0,2)$.
* **Multiply by 0.5:** The square shrinks; side lengths are halved.

---

## Topic 4: Matrix Multiplication

### Step 1: The Golden Rule

To multiply matrix $A$ by matrix $B$:
> **Columns of A must equal Rows of B.**

If $A$ is $(m \times \mathbf{n})$ and $B$ is $(\mathbf{n} \times q)$, the result is $(m \times q)$.

**Is it commutative? NO.**
Generally, $AB \neq BA$.
*Example:*
$A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}, B = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} \implies AB = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}, \text{ but } BA = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}$.

### Step 2: Calculation Walkthrough

Compute $A \times B$:
$A = \begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix}, \quad B = \begin{bmatrix} 2 & 0 \\ 1 & 3 \end{bmatrix}$

* **Entry $c_{11}$:** (Row 1 of A) $\cdot$ (Col 1 of B) $\rightarrow (1 \times 2) + (2 \times 1) = \mathbf{4}$
* **Entry $c_{12}$:** (Row 1 of A) $\cdot$ (Col 2 of B) $\rightarrow (1 \times 0) + (2 \times 3) = \mathbf{6}$
* **Entry $c_{21}$:** (Row 2 of A) $\cdot$ (Col 1 of B) $\rightarrow (0 \times 2) + (1 \times 1) = \mathbf{1}$
* **Entry $c_{22}$:** (Row 2 of A) $\cdot$ (Col 2 of B) $\rightarrow (0 \times 0) + (1 \times 3) = \mathbf{3}$

**Result:**
$$
\begin{bmatrix} 4 & 6 \\ 1 & 3 \end{bmatrix}
$$

### Step 3: Common Pitfalls
1.  **Dimensions:** Forgetting that columns of $A$ must match rows of $B$.
2.  **Order:** Assuming $AB = BA$.
3.  **Element-wise:** Multiplying elements in the same position (wrong!) instead of doing the "row-by-column" dot product.

---

## Finale: Comprehensive Test

**1. Identify Dimension:**
$\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}$
* *Answer:* $2 \times 3$

**2. Identify Type:**
$\begin{bmatrix} 5 & 0 \\ 0 & 5 \end{bmatrix}$
* *Answer:* Diagonal / Scalar / Square Matrix

**3. Scalar Multiplication:**
$4 \times \begin{bmatrix} 1 & 0 \\ 0 & 2 \end{bmatrix}$
* *Answer:* $\begin{bmatrix} 4 & 0 \\ 0 & 8 \end{bmatrix}$

**4. Matrix Multiplication Step-by-Step:**
Multiply $A=[2 \quad 3]$ ($1 \times 2$) and $B=\begin{bmatrix} 1 \\ 4 \end{bmatrix}$ ($2 \times 1$).
* *Calculation:* $(2 \times 1) + (3 \times 4) = 2 + 12 = 14$.
* *Result:* $[14]$ ($1 \times 1$ matrix).

---

## Why learn this? (Applications)

* **Computer Science:** Matrices are used to rotate 3D objects in video games.
* **Data Science:** Algorithms like Google Search use matrix math (Eigenvectors) to rank websites.
* **Coding (Python):**
    ```python
    import numpy as np
    A = np.array([[1, 2], [3, 4]])
    B = np.array([[5, 6], [7, 8]])
    result = A @ B  # Matrix multiplication symbol
    print(result)
    ```

**Next Step:** Determinants.