# 3.3 Calculus: Derivatives

This section introduces the **Derivative**, the mathematical tool for measuring **change** and **speed**.

## Topic 1: Definition & Interpretation

### Step 1: Building Intuition

**The Secant (Average Rate):**
Slope between two points ($A$ and $B$) separated by distance $h$.
$$Slope = \frac{f(x+h) - f(x)}{h}$$

**The Tangent (Instantaneous Rate):**
We drag point $B$ closer to $A$ until $h \to 0$. The secant becomes a **Tangent Line**.

**Definition of the Derivative ($f'$):**
$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

### Step 2: Geometric Interpretation

The derivative $f'(x)$ is the **Slope of the Tangent Line**.

* **$f'(x) > 0$:** Tangent points UP (Function is Increasing).
* **$f'(x) < 0$:** Tangent points DOWN (Function is Decreasing).
* **$f'(x) = 0$:** Tangent is FLAT (Function is at a peak or valley).

### Step 3: Practice (Definition)

Compute derivative of $f(x)=x^2$ at $x=3$.

1.  **Setup:**
    $$\lim_{h \to 0} \frac{(3+h)^2 - 3^2}{h}$$

2.  **Expand:**
    $$\frac{9 + 6h + h^2 - 9}{h} = \frac{6h + h^2}{h}$$

3.  **Cancel $h$:**
    $$6 + h$$

4.  **Limit:**
    As $h \to 0$, result is **6**.

---

## Topic 2: Formulas & Rules

### Step 1: Basic Formulas Table

| Function $f(x)$ | Derivative $f'(x)$ | Note |
| :--- | :--- | :--- |
| **$c$** (Constant) | **$0$** | No change |
| **$x^n$** (Power) | **$n \cdot x^{n-1}$** | Power Rule |
| **$\sin(x)$** | **$\cos(x)$** | Cycle starts |
| **$\cos(x)$** | **$-\sin(x)$** | Negative sign! |
| **$e^x$** | **$e^x$** | Unchangeable |
| **$\ln(x)$** | **$1/x$** | Log rule |

### Step 2: Differentiation Rules

**Product Rule:**
$$(f \cdot g)' = f \cdot g' + g \cdot f'$$

**Quotient Rule:**
$$\left(\frac{f}{g}\right)' = \frac{g \cdot f' - f \cdot g'}{g^2}$$

**Chain Rule (The Onion Rule):**
For functions inside functions (e.g., $\sin(x^2)$). Differentiate Outer, keep Inner, multiply by Derivative of Inner.
$$(f(g(x)))' = f'(g(x)) \cdot g'(x)$$

### Step 3: Practice (Rules)

**Product Rule:** $f(x) = x^2 \sin(x)$
* $f' = (x^2)(\cos x) + (\sin x)(2x) = x^2 \cos x + 2x \sin x$.

**Chain Rule:** $f(x) = e^{3x}$
* Outer ($e^{\dots}$) $\to$ $e^{3x}$.
* Inner ($3x$) $\to$ $3$.
* Result: $3e^{3x}$.

---

## Topic 3: Applications (Optimization)

### Step 1: Second Derivative ($f''$)

The derivative of the derivative. It measures **Curvature** (Concavity).

* **$f'' > 0$:** Smile (Concave Up). Holds water.
* **$f'' < 0$:** Frown (Concave Down). Spills water.

### Step 2: Finding Maxima & Minima

1.  **Find Critical Points:** Solve $f'(x) = 0$.
2.  **Test Concavity:** Plug point into $f''(x)$.
    * If **Positive ($+$)** $\to$ Minimum (Valley).
    * If **Negative ($-$)** $\to$ Maximum (Hill).

### Step 3: Full Analysis Example

Analyze $f(x) = x^3 - 3x$.

1.  **$f'(x)$:** $3x^2 - 3$.
2.  **Roots:** $3(x^2-1) = 0 \implies x=1, x=-1$.
3.  **$f''(x)$:** $6x$.
4.  **Test $x=-1$:** $f''(-1) = -6$ (Negative) $\to$ **Maximum**.
5.  **Test $x=1$:** $f''(1) = 6$ (Positive) $\to$ **Minimum**.

---

## Finale: Comprehensive Test

**Task 1: Differentiate**
$f(x) = \sin(x) \cdot e^{2x}$.
* **Answer:** $e^{2x} \cos(x) + 2e^{2x} \sin(x)$.

**Task 2: Monotonicity**
Where is $f(x) = 2x^3 - 6x$ decreasing?
* $f' = 6x^2 - 6$. Negative between $-1$ and $1$.
* **Answer:** Interval $(-1, 1)$.

**Task 3: Optimization**
Find local max of $f(x) = -x^2 + 4x$.
* $f' = -2x + 4 \to x=2$.
* $f'' = -2$ (Frown).
* **Answer:** Max at $x=2$.

---

## Why learn this? (Physics & Engineering)

**Motion:**
* **Position:** $s(t)$
* **Velocity:** $v(t) = s'(t)$ (How fast position changes).
* **Acceleration:** $a(t) = v'(t) = s''(t)$ (How fast velocity changes).

**Optimization:**
We use derivatives to find the "best" solution: Maximum profit, Minimum cost, Maximum strength, Minimum material.

**Next Step:** Integrals (Reversing the process to find areas).