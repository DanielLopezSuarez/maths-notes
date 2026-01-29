# 3.5 Calculus: Differential Equations

This section introduces **Differential Equations (DEs)**. These are equations that relate a function to its derivatives (its rate of change). They are the language of physics, biology, and engineering.

## Topic 1: Introduction

### Step 1: Building Intuition

**What is a Differential Equation?**
* **Standard Equation:** Like a photo. It tells you where something is ($x = 5$).
* **Differential Equation:** Like a video. It tells you how something is **moving** or changing.

**The Recipe Analogy:**
A normal recipe tells you the final amount of flour. A differential recipe tells you the **rate** at which you must pour: "Pour at 100g per minute."

**Physics Example (Uniform Motion):**
Your velocity ($v$) is constant. The equation is:

$$
\frac{dx}{dt} = v
$$

To find your position ($x$), you must find the function whose derivative is $v$.

### Step 2: Order and Solutions

* **Order:** The highest derivative in the equation.
    * $y'$ is 1st order.
    * $y''$ is 2nd order.
* **General Solution:** Includes an arbitrary constant $+ C$. It represents every possible curve that follows the rule.
* **Particular Solution:** When you use a specific starting point (initial condition) to find the exact value of $C$.

### Step 3: Practice Task

**Exercise:** Solve $y' = 2x$. Then find the particular solution for $y(0) = 5$.

1.  **Integrate:**

    $$
    \int y' \, dx = \int 2x \, dx
    $$

2.  **General Solution:**

    $$
    y = x^2 + C
    $$

3.  **Apply Condition:**
    Plug in $x=0$ and $y=5$.
    $5 = (0)^2 + C \implies C = 5$.

4.  **Particular Solution:**

    $$
    y = x^2 + 5
    $$

### Step 4: Mini-Quiz

Determine the order of these equations:

1.  $y' + 5y = 0$ $\to$ **First-order** (highest is $y'$).
2.  $y'' + 3y' + 2y = 0$ $\to$ **Second-order** (highest is $y''$).
3.  $y''' = \cos(x)$ $\to$ **Third-order** (highest is $y'''$).

---

## Topic 2: First-Order Equations

### Step 1: Separation of Variables

Method used when you can group all $y$'s on one side and all $x$'s on the other.

**Example:** Solve $y' = y \cdot x$.

1.  **Rewrite:**

    $$
    \frac{dy}{dx} = yx
    $$

2.  **Separate:**

    $$
    \frac{1}{y} dy = x \, dx
    $$

3.  **Integrate:**

    $$
    \ln|y| = \frac{1}{2}x^2 + C
    $$

4.  **Solve for y:**

    $$
    y = e^{\frac{1}{2}x^2 + C} = e^C \cdot e^{\frac{1}{2}x^2}
    $$

    *(We rename $e^C$ as a new constant $A$)*.
    **Result:**

    $$
    y = A e^{\frac{1}{2}x^2}
    $$

### Step 2: Interactive Task (Radioactive Decay)

**Exercise:** Solve $y' = -2y$.

1.  **Separate:**

    $$
    \frac{dy}{y} = -2 \, dx
    $$

2.  **Integrate:**

    $$
    \ln|y| = -2x + C
    $$

3.  **Exponentiate:**

    $$
    y = Ce^{-2x}
    $$

**Phenomenon:** This models **Radioactive Decay**. The substance decreases exponentially over time.

### Step 3: Mini-Quiz

**Exercise:** Find the general solution for $y' = \frac{x}{y}$.

1.  **Separate:**

    $$
    y \, dy = x \, dx
    $$

2.  **Integrate:**

    $$
    \frac{1}{2}y^2 = \frac{1}{2}x^2 + C
    $$

3.  **Simplify:**

    $$
    y^2 = x^2 + 2C
    $$

    *(Let $2C = K$)*.
    **Result:**

    $$
    y = \sqrt{x^2 + K}
    $$

---

## Topic 3: Second-Order Linear Equations

### Step 1: The Characteristic Equation

To solve $ay'' + by' + cy = 0$, we assume a solution $y = e^{rx}$. This gives us the quadratic equation:

$$
ar^2 + br + c = 0
$$

### Step 2: Roots and Solutions

The solution depends on the roots of the quadratic ($r$):

* **Two Real Roots ($r_1, r_2$):**

    $$
    y = C_1e^{r_1x} + C_2e^{r_2x}
    $$

* **One Repeated Root ($r$):**

    $$
    y = C_1e^{rx} + C_2xe^{rx}
    $$

* **Complex Roots ($\alpha \pm \beta i$):**

    $$
    y = e^{\alpha x}(C_1 \cos(\beta x) + C_2 \sin(\beta x))
    $$

### Step 3: Interactive Task

**Exercise:** Solve $y'' + 5y' + 4y = 0$.

1.  **Characteristic Equation:**

    $$
    r^2 + 5r + 4 = 0
    $$

2.  **Factor:**
    $(r+4)(r+1) = 0 \implies r = -4, \ r = -1$.

3.  **General Solution:**

    $$
    y = C_1e^{-4x} + C_2e^{-x}
    $$

### Step 4: Mini-Quiz

**Exercise:** Solve $y'' - 6y' + 9y = 0$.

1.  **Characteristic Equation:**

    $$
    r^2 - 6r + 9 = 0
    $$

2.  **Factor:**
    $(r-3)^2 = 0 \implies r = 3$ (Repeated).

3.  **General Solution:**

    $$
    y = C_1e^{3x} + C_2xe^{3x}
    $$

---

## Topic 4: Applications

### 1. Harmonic Oscillator (Springs)
Equation: $y'' + \omega^2y = 0$.
Describes a mass on a spring bouncing back and forth.
* **Amplitude:** How far it stretches.
* **Frequency ($\omega$):** How fast it bounces.

### 2. Bacterial Growth
Equation: Rate of growth is proportional to current size.

$$
\frac{dP}{dt} = kP
$$

**Solution:**

$$
P(t) = P_0e^{kt}
$$

This is **Exponential Growth**.

---

## Finale: Comprehensive Test

**Problem 1: First-Order**
Solve $y' = 3x^2y$.

* **Separate:** $\frac{dy}{y} = 3x^2 dx$.
* **Integrate:** $\ln|y| = x^3 + C$.
* **Result:**

    $$
    y = Ce^{x^3}
    $$

**Problem 2: Second-Order**
Solve $y'' - 2y' - 8y = 0$.

* **Characteristic Eq:** $r^2 - 2r - 8 = 0$.
* **Factor:** $(r-4)(r+2) = 0 \implies r=4, \ r=-2$.
* **Result:**

    $$
    y = C_1e^{4x} + C_2e^{-2x}
    $$

---

## Course Summary

We have built a complete mathematical toolkit:
1.  **Algebra:** Provides the structure (Matrices, Systems).
2.  **Geometry:** Provides visualization (Vectors, Lines, Planes).
3.  **Calculus:** Provides the engine (Limits, Derivatives, Integrals).

**Final Physics Connection:**
Solving $F=ma$ is literally solving a differential equation where acceleration ($a$) is the second derivative of position ($x''$). You are now speaking the language of the universe!