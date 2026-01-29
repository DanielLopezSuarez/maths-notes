# 3.4 Calculus: Integrals

This section introduces **Integration**, the reverse process of differentiation. It is used to calculate **areas**, **volumes**, and total accumulated quantities.

## Topic 1: Indefinite Integral (Antiderivative)

### Step 1: Definition

An **Antiderivative** of a function is another function whose derivative equals the original. Because the derivative of a constant is zero, we always add a Constant of Integration.

We look for $F(x)$ such that:

$$
F'(x) = f(x)
$$

**Formula:**

$$
\int f(x) \, dx = F(x) + C
$$

### Step 2: Basic Formulas Table

| Function | Integral | Note |
| :--- | :--- | :--- |
| Power ($x^n$) | `x^(n+1) / (n+1)` | Power Rule ($n \neq -1$) |
| Reciprocal ($1/x$) | `ln|x| + C` | Log Rule |
| Exponential ($e^x$) | `e^x + C` | Unchangeable |
| Cosine ($\cos x$) | `sin(x) + C` | Positive sine |
| Sine ($\sin x$) | `-cos(x) + C` | Negative cosine |

### Step 3: Practice Calculation

Find the integral of the following function:

$$
f(x) = 2x
$$

1.  **Identify Rule:** Power rule (using exponent 1).

2.  **Integrate:**

    $$
    2 \cdot \frac{x^{1+1}}{1+1} = 2 \cdot \frac{x^2}{2} = x^2
    $$

3.  **Add C:**

    $$
    x^2 + C
    $$

---

## Topic 2: Definite Integral (Area)

### Step 1: Geometric Interpretation

The definite integral calculates the **Net Area** between the curve and the x-axis defined by the bounds.

$$
\text{Area} = \int_a^b f(x) \, dx
$$

### Step 2: Fundamental Theorem of Calculus

This theorem connects Area (Geometry) with Antiderivatives (Algebra).

$$
\int_a^b f(x) \, dx = F(b) - F(a)
$$

*(Where $F$ is the antiderivative)*.

### Step 3: Practice (Area Calculation)

Compute area under this function from $x=0$ to $x=3$:

$$
f(x) = 2x
$$

1.  **Antiderivative:**

    $$
    F(x) = x^2
    $$

2.  **Apply Bounds:**

    $$
    F(3) - F(0) = 3^2 - 0^2 = 9 - 0 = \mathbf{9}
    $$

---

## Topic 3: Integration Methods

### 1. Substitution (Reverse Chain Rule)
Used when you see a function and its derivative inside the integral.

**Example:**

$$
\int 2x \cos(x^2) \, dx
$$

* Let $u = x^2$. Then the derivative is $du = 2x \, dx$.
* Substitute and integrate:

    $$
    \int \cos(u) \, du = \sin(u) + C
    $$

* Back-Substitute:

    $$
    \sin(x^2) + C
    $$

### 2. Integration by Parts (Reverse Product Rule)

**Formula:**

$$
\int u \, dv = uv - \int v \, du
$$

**Example:**

$$
\int x e^x \, dx
$$

* Choose parts: Let $u=x$ and $dv=e^x dx$.
* Calculate derivatives/integrals: $du=dx$ and $v=e^x$.
* Apply formula:

    $$
    x e^x - \int e^x \, dx
    $$

* Result:

    $$
    xe^x - e^x + C
    $$

---

## Topic 4: Applications (Volumes)

### Volume of Revolution (Disk Method)
If you rotate a curve $f(x)$ around the x-axis, it creates a 3D solid. The volume is the sum of infinite thin disks.

**Formula:**

$$
V = \pi \int_a^b [f(x)]^2 \, dx
$$

**Example: Sphere Volume**
Rotate the following semicircle from $-R$ to $R$:

$$
y = \sqrt{R^2 - x^2}
$$

**Calculation:**

$$
V = \pi \int_{-R}^{R} (R^2 - x^2) \, dx = \frac{4}{3}\pi R^3
$$

---

## Finale: Comprehensive Test

**Task 1: Definite Integral**
Calculate:

$$
\int_0^1 (4x^3 + 2) \, dx
$$

* Antiderivative: $x^4 + 2x$.
* Evaluate: $(1+2) - (0) = \mathbf{3}$.

**Task 2: Integration by Parts**
Calculate:

$$
\int x \ln(x) \, dx
$$

* Parts: $u=\ln(x), dv=x dx$.
* Result:

    $$
    \frac{x^2}{2}\ln(x) - \frac{x^2}{4} + C
    $$

**Task 3: Substitution**
Calculate:

$$
\int \sin^4(x) \cos(x) \, dx
$$

* Substitution: $u=\sin(x) \implies du=\cos(x)dx$.
* Integral becomes $\int u^4 du$.
* Result:

    $$
    \frac{\sin^5(x)}{5} + C
    $$

---

## What Comes Next?

**Differential Equations:**
Now that you know Derivatives (Rate of Change) and Integrals (Accumulation), you can solve equations that describe the physical universe.