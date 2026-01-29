# 2.2 Geometry: Vector Products

This section covers the three ways to multiply vectors: the **Dot Product** (for angles), the **Cross Product** (for perpendiculars), and the **Triple Product** (for volumes).

## Topic 1: The Dot Product ($\cdot$)

### Step 1: Definition
The dot product takes two vectors and returns a **scalar** (a single number).

* **Algebraic Formula:** Multiply corresponding components and sum them.

$$
\vec{u} \cdot \vec{v} = u_1v_1 + u_2v_2 + u_3v_3
$$

* **Geometric Formula:** Using the angle $\theta$ between them.

$$
\vec{u} \cdot \vec{v} = \|\vec{u}\| \|\vec{v}\| \cos(\theta)
$$

### Step 2: Interpreting the Result
* **Positive:** Acute angle ($< 90^\circ$).
* **Negative:** Obtuse angle ($> 90^\circ$).
* **Zero:** **Perpendicular** ($90^\circ$). This is the most important property!

### Step 3: Calculation Example
Find the dot product and angle between $\vec{u}=[1, 2, 3]$ and $\vec{v}=[-2, 1, 0]$.

1.  **Dot Product:**

    $$
    (1)(-2) + (2)(1) + (3)(0) = -2 + 2 + 0 = \mathbf{0}
    $$

2.  **Conclusion:** Since the result is 0, the vectors are **Perpendicular** ($\theta = 90^\circ$).

---

## Topic 2: The Cross Product ($\times$)

### Step 1: Definition (3D Only)
The cross product takes two vectors and returns a **new vector** that is **perpendicular** to both originals.

* **Direction:** Determined by the Right-Hand Rule.
* **Magnitude:** Equals the **Area** of the parallelogram spanned by the vectors.

### Step 2: Formula (Determinant)
To compute $\vec{u} \times \vec{v}$, use a symbolic determinant with $\mathbf{i}, \mathbf{j}, \mathbf{k}$:

$$
\vec{u} \times \vec{v} = \det \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ u_1 & u_2 & u_3 \\ v_1 & v_2 & v_3 \end{vmatrix}
$$

### Step 3: Calculation Example
Compute $\vec{u} \times \vec{v}$ for $\vec{u}=[1, 0, 0]$ and $\vec{v}=[0, 1, 0]$.

$$
\det \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{vmatrix}
$$

* $\mathbf{i}$-term: $(0)(0) - (0)(1) = 0$
* $\mathbf{j}$-term: $-( (1)(0) - (0)(0) ) = 0$
* $\mathbf{k}$-term: $(1)(1) - (0)(0) = 1$

**Result:** $[0, 0, 1]$ (Vector pointing straight up the Z-axis).

**Area:** Magnitude is $\sqrt{0+0+1} = 1$.

---

## Topic 3: The Scalar Triple Product

### Step 1: Definition
Combines three vectors ($\vec{u}, \vec{v}, \vec{w}$) to find a scalar.

$$
\text{Triple Product} = \vec{u} \cdot (\vec{v} \times \vec{w}) = \det \begin{vmatrix} u_1 & u_2 & u_3 \\ v_1 & v_2 & v_3 \\ w_1 & w_2 & w_3 \end{vmatrix}
$$

### Step 2: Geometric Meaning (Volume)
* The absolute value of the result is the **Volume** of the parallelepiped (3D box) formed by the three vectors.
* **If Result = 0:** The volume is zero, meaning the vectors are **Coplanar** (flat on the same plane).

### Step 3: Calculation Example
Check if $\vec{u}=[1, 2, 3]$, $\vec{v}=[4, 5, 6]$, and $\vec{w}=[7, 8, 9]$ are coplanar.

$$
\det \begin{vmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{vmatrix} = 0
$$

*(Calculation: $1(45-48) - 2(36-42) + 3(32-35) = -3 + 12 - 9 = 0$)*

**Conclusion:** The result is 0, so they are **Coplanar**.

---

## Finale: Comprehensive Test

**Task 1: Angle (Dot Product)**
Vectors: $\vec{a}=[2, 2, 0]$, $\vec{b}=[0, 3, 0]$.
* **Calculation:** $\vec{a} \cdot \vec{b} = 6$.
* **Lengths:** $\|\vec{a}\| = \sqrt{8}$, $\|\vec{b}\| = 3$.
* **Result:**

$$
\cos \theta = \frac{6}{3\sqrt{8}} = \frac{1}{\sqrt{2}} \implies \theta = 45^\circ
$$

**Task 2: Perpendicular Vector (Cross Product)**
Vectors: $\vec{u}=[1, 0, 0]$, $\vec{v}=[1, 1, 0]$.
* **Result:** $\vec{u} \times \vec{v} = [0, 0, 1]$.

**Task 3: Coplanarity (Triple Product)**
Vectors: $\vec{a}=[1, 0, 0]$, $\vec{b}=[0, 1, 0]$, $\vec{c}=[1, 1, 1]$.
* **Determinant:** $1$.
* **Result:** Not 0 $\to$ **Not Coplanar**. Volume = 1.

---

## Applications

* **Physics (Torque):** Torque is a cross product:

$$
\tau = \vec{r} \times \vec{F}
$$

* **Physics (Work):** Work is a dot product:

$$
W = \vec{F} \cdot \vec{d}
$$

* **Computer Graphics (Lighting):** The brightness of a pixel is calculated using the **Dot Product** between the light ray vector and the surface normal vector.

**Next Step:** Lines and Planes in 3D Space.