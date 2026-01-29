# 2.3 Geometry: Lines & Planes in Space

This section connects Algebra and Geometry. We use vectors to write equations for lines and planes, allowing us to model the 3D world mathematically.

## Topic 1: The Equation of a Line

### Step 1: Defining a Line (Point + Vector)

In 3D, we define a line using an **Anchor Point** ($P_0$) and a **Direction Vector** ($\vec{v}$).
Imagine standing at $P_0$ and walking in the direction of $\vec{v}$ for time $t$.

**The Vector Equation:**

$$
P = P_0 + t\vec{v}
$$

### Step 2: Parametric Equation

Breaking this down into coordinates ($x, y, z$).
Given $P_0(x_0, y_0, z_0)$ and $\vec{v}=[a, b, c]$:

$$
\begin{cases} 
x = x_0 + a \cdot t \\ 
y = y_0 + b \cdot t \\ 
z = z_0 + c \cdot t 
\end{cases}
$$


### Step 3: Example Calculation

Find the line passing through $P(1, 2, 3)$ parallel to $\vec{v}=[4, 5, 6]$.

**Equation:**

$$
\begin{cases} 
x = 1 + 4t \\ 
y = 2 + 5t \\ 
z = 3 + 6t 
\end{cases}
$$

**Find a point at $t=2$:**
* $x = 1 + 8 = 9$
* $y = 2 + 10 = 12$
* $z = 3 + 12 = 15$
* **Result:** Point $Q(9, 12, 15)$.

---

## Topic 2: The Equation of a Plane

### Step 1: Defining a Plane (Point + Normal)

To lock a plane in 3D, we need an **Anchor Point** ($P_0$) and a **Normal Vector** ($\vec{n}$) that stands perpendicular ($90^\circ$) to the surface.

**The General Equation:**

$$
A(x-x_0) + B(y-y_0) + C(z-z_0) = 0
$$

**Simplifies to:**

$$
Ax + By + Cz + D = 0
$$

*(Where $[A, B, C]$ is the Normal Vector $\vec{n}$)*.

### Step 2: Plane from 3 Points

If you have 3 points ($A, B, C$), you can find the plane by:
1.  Creating two vectors: $\vec{u} = \vec{AB}$ and $\vec{v} = \vec{AC}$.
2.  Finding the Normal via Cross Product: $\vec{n} = \vec{u} \times \vec{v}$.
3.  Plugging $\vec{n}$ and point $A$ into the formula above.


### Step 3: Example Calculation

Find the plane through $P(1, 2, 0)$ perpendicular to $\vec{n}=[3, 4, 5]$.

**Substitute:**

$$
3(x-1) + 4(y-2) + 5(z-0) = 0
$$

**Simplify:**

$$
3x - 3 + 4y - 8 + 5z = 0 \implies 3x + 4y + 5z - 11 = 0
$$

---

## Topic 3: Mutual Positions (Intersections)

### 1. Line and Plane

Given a line (direction $\vec{v}$) and a plane (normal $\vec{n}$):
* **Parallel:** If $\vec{v} \cdot \vec{n} = 0$ (The line runs along the plane, never hitting the normal).
* **Intersection:** Substitute the line's $x(t), y(t), z(t)$ into the plane's equation and solve for $t$.

**Example:**
Plane: $2x + 3y - z = 6$
Line: $x=1+t, \ y=2+t, \ z=3+5t$

**Substitute:**

$$
2(1+t) + 3(2+t) - (3+5t) = 6
$$

$$
2 + 2t + 6 + 3t - 3 - 5t = 6
$$

$$
5 = 6
$$

**Conclusion:** Impossible. The line is **Parallel** to the plane (No intersection).

### 2. Two Lines in 3D

* **Parallel:** Direction vectors are proportional.
* **Intersecting:** They meet at a specific point.
* **Skew:** They are not parallel but **never** meet (like a bridge over a road).

---

## Finale: Comprehensive Test

**Task 1: Line from 2 Points**
Line through $A(1, 2, 3)$ and $B(4, 4, 4)$.
* **Vector:** $\vec{v} = B - A = [3, 2, 1]$.
* **Result:**

$$
x=1+3t, \ y=2+2t, \ z=3+t
$$

**Task 2: Plane from Point & Normal**
Point $P(5, 5, 5)$, Normal $\vec{n}=[1, 0, -2]$.
* **Substitute:** $1(x-5) + 0(y-5) - 2(z-5) = 0$.
* **Result:**

$$
x - 2z + 5 = 0
$$

**Task 3: Intersection**
Line $x=t, y=t, z=t$ and Plane $x+y+z=9$.
* **Solve:** $t + t + t = 9 \implies 3t=9 \implies t=3$.
* **Result:** Point $(3, 3, 3)$.

---

## Applications

* **Computer Graphics (Frustum Culling):** A camera's view is defined by 6 planes. The math checks if an object is "inside" these planes to decide if it should be drawn.
* **Robotics (Collision):** A robot arm moves along a parametric line. The software constantly checks for intersections with planes (walls/tables) to avoid crashes.

**Next Module:** Calculus (The study of continuous change).