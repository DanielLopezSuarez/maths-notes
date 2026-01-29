# 3.2 Calculus: Limits

This section covers the concept of the **Limit**. This is the tool that allows calculus to deal with infinity, division by zero, and instantaneous change.

## Topic 1: Limits of Sequences

### Step 1: Intuition (The Archer)

**Convergence:**
Imagine an archer getting better with every shot.
* **Arrows:** The terms of the sequence ($a_1, a_2, a_3...$).
* **Bullseye:** The Limit ($L$).

Convergence means the terms get **arbitrarily close** to the target as you go further ($n \to \infty$).

**Example:** $a_n = \frac{1}{n}$
* $n=1 \to 1$
* $n=10 \to 0.1$
* $n=1,000,000 \to 0.000001$

**Conclusion:** As $n$ gets huge, the value approaches 0.
$$\lim_{n \to \infty} \frac{1}{n} = 0$$

### Step 2: Divergence

A sequence **diverges** if it does not settle on a single number.
* **To Infinity:** $2, 4, 8, 16... \to \infty$.
* **Oscillating:** $1, -1, 1, -1...$ (It never settles).

### Step 3: Practice Calculation

Consider $a_n = \frac{n+1}{n}$.

1.  **Calculate Terms:**
    * $n=1 \to 2/1 = \mathbf{2}$
    * $n=10 \to 11/10 = \mathbf{1.1}$
    * $n=100 \to 101/100 = \mathbf{1.01}$

2.  **Find the Limit:**
    Split the fraction:
    $$\lim_{n \to \infty} \left( \frac{n}{n} + \frac{1}{n} \right) = \lim_{n \to \infty} (1 + 0) = 1$$

---

## Topic 2: Limits of Functions

### Step 1: The "Hole" Analogy

**Value vs. Limit:**
* **$f(c)$ (Value):** "Is there a plank on the bridge right here?"
* **$\lim_{x \to c} f(x)$ (Limit):** "Where does the bridge *look like* it goes?"

If there is a hole in the graph at $x=c$:
* The Value is **undefined** (you fall through).
* The Limit **exists** (the path leads to the hole).

### Step 2: One-Sided Limits

* **Left-Sided ($\lim_{x \to c^-}$):** Approaching from numbers smaller than $c$.
* **Right-Sided ($\lim_{x \to c^+}$):** Approaching from numbers larger than $c$.

> **Rule:** For a general limit to exist, the Left and Right limits must be **equal**.

### Step 3: Practice (Indeterminate Forms)

Compute the limit of a function with a hole: $f(x) = \frac{x^2 - 1}{x - 1}$ at $x=1$.

1.  **Direct Substitution:**
    $$\frac{1^2 - 1}{1 - 1} = \frac{0}{0}$$
    This is an **Indeterminate Form**. It means "do more work".

2.  **Factor and Simplify:**
    $$\frac{(x-1)(x+1)}{(x-1)} = x+1$$

3.  **Compute Limit:**
    $$\lim_{x \to 1} (x+1) = 1+1 = \mathbf{2}$$

---

## Topic 3: Arithmetic Rules

If $\lim f(x) = A$ and $\lim g(x) = B$:
* **Sum:** Limit is $A + B$.
* **Product:** Limit is $A \cdot B$.
* **Quotient:** Limit is $A / B$ (if $B \neq 0$).

### Mini-Quiz: Solving Limits

**Task 1:** $\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$
* **Factor:** $(x-2)(x+2)$.
* **Simplify:** $x+2$.
* **Result:** $2+2 = \mathbf{4}$.

**Task 2:** $\lim_{x \to 3} \frac{x^2 - 2x - 3}{x - 3}$
* **Factor:** $(x-3)(x+1)$.
* **Simplify:** $x+1$.
* **Result:** $3+1 = \mathbf{4}$.

---

## Finale: Comprehensive Test

**Task 1: Sequence Limit**
Find $\lim_{n \to \infty} \frac{4n^2 + n}{2n^2}$.
* **Logic:** Divide by highest power ($n^2$).
* **Result:** $4/2 = \mathbf{2}$.

**Task 2: Function Limit**
Find $\lim_{x \to 5} \frac{x - 5}{x^2 - 25}$.
* **Factor:** Denominator is $(x-5)(x+5)$.
* **Simplify:** $1 / (x+5)$.
* **Result:** $1/10 = \mathbf{0.1}$.

**Task 3: Graph Reading**
At $x=0$, the graph approaches $y=2$ from the left and $y=-1$ from the right.
* **Question:** What is $\lim_{x \to 0^+}$ (Right-sided)?
* **Answer:** **-1**.

---

## Why learn this? (Continuity & Derivatives)

**Continuity:**
A function is continuous (unbroken) only if:
1.  The Limit exists.
2.  The Function Value exists.
3.  **Limit = Value**.

**The Derivative:**
The Derivative is literally a **limit**. It is the limit of the slope as two points get infinitely close together.

$$\text{Derivative} = \lim_{\Delta x \to 0} \frac{f(x+\Delta x) - f(x)}{\Delta x}$$

**Next Step:** Derivatives (Calculating the speed of change).