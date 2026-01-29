# 3.1 Calculus: Functions & Relations

This section lays the groundwork for Calculus. Before we can study how things change (Derivatives) or accumulate (Integrals), we must rigorously define the objects we are studying: **Functions**.

## Topic 1: Relations and Functions

### Step 1: Building Intuition

**What is a Relation?**
A relation is simply a connection between elements of two sets.
* *Example:* Set A (People) and Set B (Fruit). If John likes Apples and Bananas, there is a relation connecting John to both.

**What is a Function?**
A function is a **strict** type of relation.
> **The Golden Rule:** For every valid input, there is **exactly one** output.

**The Machine Analogy:**
Imagine a function as a machine.
1.  **Input ($x$):** You drop a raw material into the funnel.
2.  **Process:** The machine performs a specific task (e.g., "multiply by 2").
3.  **Output ($f(x)$):** The machine spits out the finished product.

* *Function:* You press "Cola", you get 1 can of Cola.
* *Not a Function:* You press "Cola", and sometimes you get Cola, sometimes Sprite.

### Step 2: Definitions (Domain, Codomain, Range)

* **Domain:** The set of all allowed inputs (what you *can* put in).
* **Codomain:** The set of all possible theoretical outputs (the type of result, e.g., "Real Numbers").
* **Range (Image):** The set of actual outputs the function produces.

**Example:**
Mapping Reals to Reals ($f: \mathbb{R} \to \mathbb{R}$) for the function:

$$
f(x) = x^2
$$

* **Domain:** $\mathbb{R}$ (You can square any number).
* **Codomain:** $\mathbb{R}$ (We expect real numbers).
* **Range:** $[0, \infty)$ (Non-negative numbers).
    * *Why?* Because $x^2$ is never negative. Even though $-5$ is in the Codomain, it is not in the Range.

### Step 3: Practice Exercise

Determine if the following relations are functions:

1.  **Relation A:** Input is a Person $\to$ Output is their biological Date of Birth.
2.  **Relation B:** The unit circle equation below with Input $x=0$.

    $$
    x^2 + y^2 = 1
    $$

3.  **Relation C:** Input $1 \to 5$, Input $2 \to 6$, Input $1 \to 7$.

**Answers:**
1.  **Yes:** Every person has exactly one birth date.
2.  **No:** If $x=0$, $y$ could be $1$ OR $-1$. (Two outputs).
3.  **No:** The input "1" gives two different results (5 and 7).

### Step 4: Mini-quiz

1.  **True/False:** The Range is always the same size or smaller than the Codomain.
    * **Answer:** **True**. It is a subset of the Codomain.

2.  **True/False:** A vertical line can cross a function's graph at two points.
    * **Answer:** **False**. This is the "Vertical Line Test". If it crosses twice, one $x$ has two $y$'s (not a function).

3.  **True/False:** If $f(2)=5$ and $f(2)=5$, it might still be a function.
    * **Answer:** **True**. Listing the same valid pair twice doesn't break the rules.

---

## Topic 2: Real Functions & Graphs

### Step 1: Visualizing Functions

We use the Cartesian Plane ($x, y$).
* **X-axis:** Inputs (Domain).
* **Y-axis:** Outputs (Values).
* **Graph:** The collection of points $(x, y)$ where $y = f(x)$.

**Key Properties:**
* **Roots (Zeros):** Inputs where $f(x) = 0$. Visually, where the graph hits the X-axis.
* **Increasing:** As $x$ goes right, $y$ goes up.
* **Decreasing:** As $x$ goes right, $y$ goes down.
* **Constant:** Horizontal line.

### Step 2: Practice (Graph Reading)

Consider the function:

$$
f(x) = x - 2
$$

* **Zero:** $x = 2$ (Since $2-2=0$).
* **Domain:** $\mathbb{R}$ (All real numbers).
* **Monotonicity:** Increasing everywhere (Line goes up).

### Step 3: Piecewise Functions

A function can change its rule based on the input.

**Example $g(x)$:**

$$
g(x) = \begin{cases} -2 & \text{if } x < 0 \\ x & \text{if } x \geq 0 \end{cases}
$$

**Questions:**
1.  **Find $g(-5)$:** Since $-5 < 0$, we use the top rule. Result: **-2**.
2.  **Find the Zero:** The graph touches $y=0$ at $x=0$.
3.  **Monotonicity on $(-\infty, 0)$:** It is **Constant** (stays at -2).

---

## Topic 3: Sequences (Discrete Functions)

### Step 1: Definition

A sequence is a function where the Domain is restricted to **Natural Numbers** ($\mathbb{N} = \{1, 2, 3...\}$).
Instead of $f(x)$, we write $a_n$ (the $n$-th term).

### Step 2: General Term ($a_n$)

The formula that tells you how to calculate the value at position $n$.

**Example:** $a_n = 2n + 1$.
* $n=1 \to 2(1)+1 = 3$
* $n=2 \to 2(2)+1 = 5$
* $n=3 \to 2(3)+1 = 7$
* Sequence: $3, 5, 7...$

### Step 3: Calculation Practice

Calculate the first 5 terms of:

$$
a_n = n^2 - 1
$$

**Results:**
1.  $1^2 - 1 = \mathbf{0}$
2.  $2^2 - 1 = \mathbf{3}$
3.  $3^2 - 1 = \mathbf{8}$
4.  $4^2 - 1 = \mathbf{15}$
5.  $5^2 - 1 = \mathbf{24}$

---

## Finale: Comprehensive Test

**Task 1: Relation Check**
Set $A=\{2, 4\}$, Set $B=\{1, 3, 5\}$. Pairs: $\{(2, 1), (2, 3), (4, 5)\}$.
* **Answer:** Not a function. Input "2" has two outputs (1 and 3).

**Task 2: Graph Properties**
Consider $y = x^2 - 4$ (Parabola shifted down).
* **Roots:** $x=2$ and $x=-2$.
* **Minimum:** $y=-4$ (at $x=0$).

**Task 3: Sequence Math**
Find the 3rd term of the sequence below:

$$
a_n = \frac{n}{n+1}
$$

* **Answer:** $a_3 = \frac{3}{3+1} = \frac{3}{4} = 0.75$.

---

## Why learn this? (Applications)

* **Physics (Gravity):** Height is a function of time.

    $$
    h(t) = h_0 - 4.9t^2
    $$

* **Economics:** Currency conversion is a linear function.

    $$
    E(d) = 0.92d
    $$

* **Biology:** Drug concentration is an exponential decay function.

    $$
    C(t) = C_0 \cdot e^{-kt}
    $$

**Next Step:** Limits (approaching infinity and division by zero).