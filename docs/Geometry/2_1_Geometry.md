# 2.1 Geometry: Cartesian Space & Vectors

This section introduces the language of geometry: points, vectors, and the coordinate systems we use to measure them.

## Topic 1: Cartesian Space and Vectors

### Step 1: The Coordinate System
* **2D Space ($x, y$):** Two perpendicular axes crossing at the origin $(0,0)$.
* **3D Space ($x, y, z$):** A third axis ($z$) is added to describe depth/height.

### Step 2: Point vs. Vector (The Treasure Map Analogy)
* **Point ($P$):** A fixed **location**.
    * *Analogy:* The "X" on a map.
    * *Notation:* $P = (4, 3)$.
* **Vector ($\vec{v}$):** An **instruction** or displacement. It has no fixed position.
    * *Analogy:* "Walk 4 steps East, 3 steps North".
    * *Notation:* $\vec{v} = [4, 3]$.

**Properties of a Vector:**
1.  **Magnitude:** Length of the arrow.
2.  **Direction:** The line it travels along (e.g., Northeast).
3.  **Sense:** The specific way it points (Northeast vs. Southwest).

### Step 3: Computing a Vector from Points
To find the vector $\vec{AB}$ that goes **from** point $A$ **to** point $B$:
$$
\vec{AB} = B - A = [x_B - x_A, \ y_B - y_A]
$$

**Example:**
From $A=(1, 2)$ to $B=(5, 5)$.
$$
\vec{AB} = [5-1, \ 5-2] = [4, 3]
$$
*Meaning:* Move 4 units right and 3 units up.

### Step 4: Mini-Quiz
1.  **Concept:** What is the difference between $P=(2,5)$ and $\vec{v}=[2,5]$?
    * *Answer:* $P$ is a spot in space; $\vec{v}$ is a movement instruction.
2.  **Calculation:** Find vector $\vec{PQ}$ from $P(3,1)$ to $Q(1,4)$.
    * *Answer:* $[1-3, \ 4-1] = [-2, \ 3]$.
3.  **True/False:** Vector from $(0,0)$ to $(3,4)$ is the same as vector from $(5,5)$ to $(8,9)$.
    * *Answer:* **True**. Both represent the movement $[3, 4]$.

---

## Topic 2: Vector Operations

### Step 1: Algebraic Methods
If $\vec{u} = [1, 3]$ and $\vec{v} = [4, 1]$:

* **Addition:** Add components.
    $$
    \vec{u} + \vec{v} = [1+4, \ 3+1] = [5, 4]
    $$
* **Subtraction:** Subtract components.
    $$
    \vec{u} - \vec{v} = [1-4, \ 3-1] = [-3, 2]
    $$

### Step 2: Geometric Interpretation
* **Triangle Method (Addition):** Draw $\vec{v}$ starting from the tip of $\vec{u}$. The result is the arrow from the start of $\vec{u}$ to the end of $\vec{v}$.
* **Parallelogram Method:** Start both from the same point. The diagonal is the sum.

### Step 3: Scalar Multiplication
Scaling a vector by a number $k$ changes its length (and sometimes direction).
Given $\vec{u} = [2, 3]$:

* **$k = 2$ (Stretch):** $2\vec{u} = [4, 6]$. Same direction, double length.
* **$k = -1$ (Reverse):** $-1\vec{u} = [-2, -3]$. Opposite direction, same length.
* **$k = 0.5$ (Shrink):** $0.5\vec{u} = [1, 1.5]$. Same direction, half length.

### Step 4: Practice Calculation
Compute $\vec{w} = 2\vec{u} - \vec{v}$ for $\vec{u}=[1, 2, 3]$ and $\vec{v}=[4, 5, 6]$.

1.  **$2\vec{u}$:** $[2, 4, 6]$
2.  **Subtract $\vec{v}$:** $[2-4, \ 4-5, \ 6-6]$
3.  **Result:** $[-2, -1, 0]$

---

## Topic 3: Length & Unit Vectors

### Step 1: Length (Magnitude)
The length of a vector $\|\vec{v}\|$ is calculated using the Pythagorean Theorem.

* **2D:** $\|\vec{v}\| = \sqrt{x^2 + y^2}$
* **3D:** $\|\vec{v}\| = \sqrt{x^2 + y^2 + z^2}$

**Example:** For $\vec{v} = [3, 4]$:
$$
\|\vec{v}\| = \sqrt{3^2 + 4^2} = \sqrt{9+16} = \sqrt{25} = 5
$$

### Step 2: Unit Vector (Normalization)
A **Unit Vector** ($\hat{v}$) has a length of exactly 1. It represents pure direction.
To find it, divide the vector by its own length:
$$
\hat{v} = \frac{\vec{v}}{\|\vec{v}\|}
$$

**Example:** Normalize $\vec{v} = [3, 4]$ (Length is 5).
$$
\hat{v} = \left[ \frac{3}{5}, \frac{4}{5} \right] = [0.6, \ 0.8]
$$
*Check:* $\sqrt{0.6^2 + 0.8^2} = \sqrt{0.36 + 0.64} = \sqrt{1} = 1$.

---

## Finale: Comprehensive Test

**Given:**
* Points: $A(2, -1, 0)$, $B(0, 2, 4)$
* Vectors: $\vec{u} = [1, 1, -2]$, $\vec{v} = [3, 0, 4]$

**Tasks:**

1.  **Coordinates:** Find vector $\vec{AB}$.
    * *Solution:* $[0-2, \ 2-(-1), \ 4-0] = [-2, 3, 4]$
2.  **Operations:** Find $3\vec{u} - 2\vec{v}$.
    * *Solution:* $[3, 3, -6] - [6, 0, 8] = [-3, 3, -14]$
3.  **Length:** Find $\|\vec{v}\|$.
    * *Solution:* $\sqrt{3^2 + 0^2 + 4^2} = \sqrt{25} = 5$
4.  **Normalization:** Find unit vector $\hat{u}$.
    * *Solution:* Length $\|\vec{u}\| = \sqrt{1+1+4} = \sqrt{6}$.
    * Result: $[\frac{1}{\sqrt{6}}, \frac{1}{\sqrt{6}}, \frac{-2}{\sqrt{6}}]$.

---

## Why learn this? (Applications)

* **Physics:** Forces are vectors. If you push a box East ($10N$) and North ($5N$), the resultant force vector is $[10, 5]$.
* **Game Development:**
    * **Position:** Where the player is ($P$).
    * **Velocity:** Where the player is moving ($\vec{v}$).
    * **Lighting:** Calculated using Unit Vectors (normals) to determine how light bounces off surfaces.

**Next Step:** The **Dot Product** (multiplying vectors to find angles).