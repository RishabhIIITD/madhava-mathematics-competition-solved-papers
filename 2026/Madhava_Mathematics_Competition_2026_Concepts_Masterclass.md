# Madhava Mathematics Competition
## Comprehensive Concept Guide & Undergraduate Competition Masterclass

**Author:** Solved Papers Archive Initiative  
**Target Audience:** Undergraduate Students, Olympiad Aspirants (Madhava, Putnam, IMC, TIFR, NBHM, JAM)  
**Objective:** A self-contained, rigorous, and beginner-friendly conceptual treatise. Master every concept, theorem, proof technique, and problem-solving heuristic required to achieve full marks on the competition paper.

---

# Table of Contents
1. [Foundational Algebra & Number Theory](#1-foundational-algebra--number-theory)
   - 1.1 [Progressions with Integer Constraints & Diophantine Factoring](#11-progressions-with-integer-constraints--diophantine-factoring)
   - 1.2 [Polynomial Division & GCD of Integer Sequences](#12-polynomial-division--gcd-of-integer-sequences)
   - 1.3 [$p$-adic Valuations & Non-linear Recurrences](#13-p-adic-valuations--non-linear-recurrences)
   - 1.4 [Parity Invariants & Fermat's Method of Infinite Descent](#14-parity-invariants--fermats-method-of-infinite-descent)
2. [Combinatorics & Polygons](#2-combinatorics--polygons)
   - 2.1 [Polygon Triangulations & Complementary Counting](#21-polygon-triangulations--complementary-counting)
   - 2.2 [Subset Parity & Binomial Sieve Techniques](#22-subset-parity--binomial-sieve-techniques)
3. [Real Analysis & Calculus](#3-real-analysis--calculus)
   - 3.1 [Connectedness, Totally Disconnected Spaces, & Continuity](#31-connectedness-totally-disconnected-spaces--continuity)
   - 3.2 [Reverse-Engineering Auxiliary Functions for Rolle's Theorem](#32-reverse-engineering-auxiliary-functions-for-rolles-theorem)
   - 3.3 [Uniform Convergence & The Weierstrass M-Test](#33-uniform-convergence--the-weierstrass-m-test)
   - 3.4 [Monotonicity, Fixed Points, & Inverse Function Symmetry](#34-monotonicity-fixed-points--inverse-function-symmetry)
   - 3.5 [Constructing Pathological Functions via Dirichlet & Thomae Methods](#35-constructing-pathological-functions-via-dirichlet--thomae-methods)
4. [Complex Analysis & Polynomial Roots](#4-complex-analysis--polynomial-roots)
   - 4.1 [Roots of Unity & Logarithmic Differentiation](#41-roots-of-unity--logarithmic-differentiation)
   - 4.2 [Root Localization: Descartes' Rule of Signs & Rouché's Theorem](#42-root-localization-descartes-rule-of-signs--rouch%C3%A9s-theorem)
   - 4.3 [The Maximum Modulus Principle & Geometric Extremal Products](#43-the-maximum-modulus-principle--geometric-extremal-products)
5. [Linear Algebra & Matrix Theory](#5-linear-algebra--matrix-theory)
   - 5.1 [Matrix Commutators, Lie Brackets, & Nilpotency](#51-matrix-commutators-lie-brackets--nilpotency)
   - 5.2 [Quadratic Forms, $L^2$ Inner Products, & The Hilbert Matrix](#52-quadratic-forms-l2-inner-products--the-hilbert-matrix)
6. [Differential Equations](#6-differential-equations)
   - 6.1 [Forming Differential Equations for Geometric Families of Curves](#61-forming-differential-equations-for-geometric-families-of-curves)
7. [Comprehensive Problem-Solving Checklist](#7-comprehensive-problem-solving-checklist)

---

# 1. Foundational Algebra & Number Theory

---

## 1.1 Progressions with Integer Constraints & Diophantine Factoring

### The Core Concept
In algebra competitions, conditions relating the terms of a geometric progression (GP) and an arithmetic progression (AP) often look unconstrained at first glance. However, the condition that the variables and the common ratio are **integers** transforms a continuous algebraic equation into a rigid **Diophantine equation**.

### The Technique
Let $a, b, c$ be in geometric progression with common ratio $r \in \mathbb{Z}$:
$$b = ar, \quad c = ar^2$$
When substituting into linear or arithmetic mean equations (such as $\frac{a+b+c}{3} = b + k$), always clear denominators and **isolate the primary variable** $a$:
$$a(1 - 2r + r^2) = 3k \implies a(r - 1)^2 = 3k$$

Because $(r - 1)^2$ must be a perfect square dividing the constant $3k$:
1. Find the prime factorization of $3k$.
2. List all square divisors of $3k$.
3. Since squares grow rapidly ($1, 4, 9, 16, \dots$), only a tiny finite set of candidates for $r - 1$ exist.

### Worked Example (Distinct from the Exam)
**Problem:** Let $x < y < z$ be positive integers in geometric progression with an integer common ratio $r$. If the arithmetic mean of $x, y, z$ exceeds $y$ by $8$, find the value of $x$.

**Step-by-step Solution:**
1. Express $y$ and $z$ in terms of $x$ and $r$:
   $$y = xr, \quad z = xr^2 \quad (r \in \mathbb{Z}, r \ge 2)$$
2. Set up the arithmetic mean condition:
   $$\frac{x + xr + xr^2}{3} = xr + 8$$
   $$x(1 + r + r^2) = 3xr + 24$$
   $$x(r^2 - 2r + 1) = 24 \implies x(r - 1)^2 = 24$$
3. Find the square divisors of $24$:
   $$24 = 2^3 \times 3$$
   The positive square divisors of $24$ are only $1^2 = 1$ and $2^2 = 4$.
   - **Case 1:** $(r - 1)^2 = 1 \implies r - 1 = 1 \implies r = 2$.  
     Then $x = \frac{24}{1} = 24$.  
     The terms are $x = 24, y = 48, z = 96$.  
     Check AM: $\frac{24 + 48 + 96}{3} = \frac{168}{3} = 56 = 48 + 8$. Valid!
   - **Case 2:** $(r - 1)^2 = 4 \implies r - 1 = 2 \implies r = 3$.  
     Then $x = \frac{24}{4} = 6$.  
     The terms are $x = 6, y = 18, z = 54$.  
     Check AM: $\frac{6 + 18 + 54}{3} = \frac{78}{3} = 26 = 18 + 8$. Valid!
4. **Takeaway:** Factoring out $(r-1)^2$ immediately reduces an infinite search space to just 2 cases.

---

## 1.2 Polynomial Division & GCD of Integer Sequences

### The Core Concept
For two polynomials $f(x), g(x) \in \mathbb{Z}[x]$, the greatest common divisor $\gcd(f(n), g(n))$ for integers $n \in \mathbb{Z}$ is fundamentally bounded by the **resultant** of the two polynomials.

### Theorem (Integer Linear Combinations of Polynomials)
If there exist polynomials $A(x), B(x) \in \mathbb{Z}[x]$ and a non-zero integer $C \in \mathbb{Z}$ such that:
$$A(x)f(x) + B(x)g(x) = C$$
then for every integer $n \in \mathbb{Z}$:
$$\gcd(f(n), g(n)) \mid C$$
Consequently, $\gcd(f(n), g(n))$ can only take values that are **positive divisors of $C$**.

### How to eliminate $n$ systematically
1. To avoid rational coefficients when dividing $f(x)$ by $g(x) = ax + b$, multiply $f(x)$ by $a^{\deg(f)}$ or an appropriate integer scalar.
2. Perform polynomial division with remainder until the remainder is a constant integer $C$.

### Worked Example (Distinct from the Exam)
**Problem:** Let $P(n) = 3n^2 + 5n + 7$ and $Q(n) = 2n + 1$. Determine all possible values that $\gcd(P(n), Q(n))$ can attain as $n$ ranges over the integers.

**Step-by-step Solution:**
1. Multiply $P(n)$ by $4$ to allow division by $2n + 1$ without fractions:
   $$4P(n) = 12n^2 + 20n + 28$$
2. Divide by $Q(n) = 2n + 1$:
   $$12n^2 + 20n + 28 = (2n + 1)(6n + 7) + 21$$
   Rearranging gives:
   $$4P(n) - (6n + 7)Q(n) = 21$$
3. Let $d = \gcd(P(n), Q(n))$. Since $d \mid P(n)$ and $d \mid Q(n)$, $d$ must divide $4P(n) - (6n+7)Q(n) = 21$.
   The positive divisors of $21$ are $\{1, 3, 7, 21\}$.
4. Can each divisor actually be achieved?
   - If $n = 0$: $P(0) = 7, Q(0) = 1 \implies \gcd(7, 1) = 1$.
   - If $n = 1$: $P(1) = 15, Q(1) = 3 \implies \gcd(15, 3) = 3$.
   - If $n = 3$: $P(3) = 27 + 15 + 7 = 49, Q(3) = 7 \implies \gcd(49, 7) = 7$.
   - If $n = 10$: $Q(10) = 21, P(10) = 300 + 50 + 7 = 357 = 21 \times 17 \implies \gcd(357, 21) = 21$.
5. **Conclusion:** The set of possible values is precisely $\{1, 3, 7, 21\}$.

---

## 1.3 $p$-adic Valuations & Non-linear Recurrences

### Definition & Axioms
Let $p$ be a prime number. The **$p$-adic valuation** of a non-zero integer $n$, denoted $v_p(n)$, is the unique integer $k \ge 0$ such that $p^k \mid n$ but $p^{k+1} \nmid n$.
We define $v_p(0) = \infty$.

### Fundamental Properties
1. **Multiplicativity:** $v_p(ab) = v_p(a) + v_p(b)$.
2. **Ultrametric Triangle Inequality:**
   $$v_p(a + b) \ge \min(v_p(a), v_p(b))$$
3. **Strict Equality Principle (The Dominant Term):**
   $$\text{If } v_p(a) \ne v_p(b), \quad \text{then } v_p(a + b) = \min(v_p(a), v_p(b))$$

> [!IMPORTANT]
> The Strict Equality Principle is one of the most powerful tools in competition number theory. If you can show that one term in a sum has a strictly smaller power of $p$ than all the others, that term **uniquely determines** the exact divisibility of the sum.

### Applying $v_p$ to Quadratic Recurrences
Consider roots $\alpha, \beta$ of $x^2 + bx + c = 0$. The sequence $a_n = \alpha^{2^n} + \beta^{2^n}$ satisfies:
$$a_{n+1} = a_n^2 - 2c^{2^n}$$
Notice the squaring structure:
If $a_n \equiv 2c^{2^{n-1}} \pmod{p^{M_n}}$, then squaring gives $a_n^2 \approx 4c^{2^n}$, and subtracting $2c^{2^n}$ leaves $2c^{2^n}$, propagating the exact valuation!

### Worked Example (Distinct from the Exam)
**Problem:** Let $\alpha, \beta$ be the roots of $x^2 - 15x + 35 = 0$. Find the highest power of $5$ dividing $\alpha^4 + \beta^4$.

**Step-by-step Solution:**
1. Identify coefficients: $b = -15, c = 35$.
   Prime of interest: $p = 5$.
   $v_5(b) = v_5(-15) = 1$.
   $v_5(c) = v_5(35) = 1$.
   Notice $p = 5 > 2$, so $v_5(2) = 0$.
2. Compute $a_1 = \alpha^2 + \beta^2$:
   $$a_1 = b^2 - 2c = (-15)^2 - 2(35) = 225 - 70 = 155$$
   $v_5(155) = 1$ (since $155 = 5 \times 31$).
3. Compute $a_2 = \alpha^4 + \beta^4$:
   $$a_2 = a_1^2 - 2c^2 = (155)^2 - 2(35)^2$$
   Notice that $155 = 5 \times 31$, so $(155)^2 = 25 \times 961$.
   $2(35)^2 = 2 \times 1225 = 2450 = 25 \times 98$.
   $$a_2 = 25(961 - 98) = 25 \times 863$$
   Is $863$ divisible by $5$? $863 \equiv 3 \pmod 5$, so $5 \nmid 863$.
   Therefore:
   $$v_5(a_2) = v_5(25) + v_5(863) = 2 + 0 = 2$$
   The largest power of $5$ dividing $\alpha^4 + \beta^4$ is $5^2 = 25$.

---

## 1.4 Parity Invariants & Fermat's Method of Infinite Descent

### The Strategy
When a condition holds symmetrically after removing any single element from a collection of integers $x_1, \dots, x_n$:
1. **Express the total sum:** Let $S = \sum_{i=1}^n x_i$.
2. **Translate the partition condition:** The remaining sum $S - x_k$ can be split into two equal integer halves, so:
   $$S - x_k = 2 A_k \implies x_k \equiv S \pmod 2 \quad \forall k$$
   This proves all elements must share the **exact same parity**.
3. **Use the count $n$ to create a parity clash:**
   If all $x_i$ were odd and $n$ is even, $S = \sum x_i$ is the sum of an even number of odds, which is **even**.
   Then $S - x_k = \text{even} - \text{odd} = \text{odd}$, contradicting $2 A_k$ being even!
4. **Infinite Descent:** Once all $x_i$ are forced to be even, replace each $x_i$ with $x_i / 2$. Since this division preserves the problem's hypothesis, the integers must be divisible by $2^m$ for every $m \in \mathbb{N}$, forcing $x_i = 0$.

### Worked Example (Distinct from the Exam)
**Problem:** A set of 6 non-negative integers has the property that whenever any one integer is removed, the remaining 5 integers can be balanced on a two-pan scale so that each pan contains the same total weight. Prove that all 6 integers must be 0.

**Step-by-step Solution:**
1. Let the integers be $w_1, w_2, \dots, w_6 \ge 0$, and let $W = \sum_{i=1}^6 w_i$.
2. For each $k \in \{1, \dots, 6\}$, removing $w_k$ leaves total weight $W - w_k = 2 P_k$, where $P_k$ is the weight in each pan.
3. Thus $w_k \equiv W \pmod 2$ for all $k$.
   Either all 6 weights are even, or all 6 weights are odd.
4. If all 6 weights were odd:
   $W$ is the sum of 6 odd numbers $\implies W$ is even.
   Then $W - w_k = \text{even} - \text{odd} = \text{odd}$.
   But $2 P_k$ is even $\implies$ Contradiction!
5. Hence all weights must be even: $w_i = 2 w_i'$.
   The new set $w_1', \dots, w_6'$ still satisfies the exact same balance property.
6. By Infinite Descent, $w_i$ is divisible by $2^m$ for all $m \ge 1$. Since $w_i \in \mathbb{Z}_{\ge 0}$, $w_i = 0$ for all $i$.

---

# 2. Combinatorics & Polygons

---

## 2.1 Polygon Triangulations & Complementary Counting

### Problem Statement
Given a regular $n$-gon ($n \ge 6$), how many triangles formed by choosing 3 of its vertices share **no edges** with the polygon?

```
Regular n-gon Vertices: v_1, v_2, ..., v_n
Possible Triangles:
  - 2 sides in common: [v_i, v_{i+1}, v_{i+2}] (consecutive vertices)
  - 1 side in common:  [v_i, v_{i+1}, v_k] (where v_k is non-adjacent)
  - 0 sides in common: all 3 vertices separated by at least 1 edge
```

### The Complementary Counting Breakdown
1. **Total Triangles:** $\binom{n}{3}$.
2. **Triangles sharing 2 edges ($N_2$):**  
   Any such triangle must be formed by 3 consecutive vertices $(v_i, v_{i+1}, v_{i+2})$.  
   Since there are $n$ vertices in an $n$-gon, there are exactly:
   $$N_2 = n$$
3. **Triangles sharing 1 edge ($N_1$):**  
   - Choose one edge of the $n$-gon: $n$ choices.
   - Let the edge be $(v_1, v_2)$. The third vertex cannot be $v_1$ or $v_2$ (the endpoints), nor can it be $v_n$ or $v_3$ (which would create a 2-edge triangle).
   - Thus, $4$ vertices are excluded. The remaining $n - 4$ vertices are valid.
   $$N_1 = n(n - 4)$$
4. **Triangles sharing 0 edges ($N_0$):**
   $$N_0 = \binom{n}{3} - N_1 - N_2 = \frac{n(n-1)(n-2)}{6} - n(n-4) - n$$
   Factor out $\frac{n}{6}$:
   $$N_0 = \frac{n}{6}\left[(n-1)(n-2) - 6(n-4) - 6\right] = \frac{n}{6}\left[n^2 - 3n + 2 - 6n + 24 - 6\right]$$
   $$N_0 = \frac{n}{6}\left[n^2 - 9n + 20\right] = \frac{n(n - 4)(n - 5)}{6}$$

### Worked Example (Distinct from the Exam)
**Problem:** In a regular octagon ($n = 8$), find:
1. The number of triangles with no edges in common with the octagon.
2. The number of triangles with at least one edge in common.

**Step-by-step Solution:**
1. Total triangles: $\binom{8}{3} = \frac{8 \times 7 \times 6}{6} = 56$.
2. Formula for 0 shared edges:
   $$N_0 = \frac{8(8 - 4)(8 - 5)}{6} = \frac{8 \times 4 \times 3}{6} = \frac{96}{6} = 16$$
3. Triangles with at least one shared edge:
   $$\text{Total} - N_0 = 56 - 16 = 40$$
   Check via components:
   - $N_2 = 8$
   - $N_1 = 8(8 - 4) = 32$
   - $N_1 + N_2 = 32 + 8 = 40$. Matches!

---

## 2.2 Subset Parity & Binomial Sieve Techniques

### The Core Concept
Evaluating sums of binomial coefficients over arithmetic progressions of indices (e.g. all odd indices, all even indices, or indices mod 3 or 4) is known as the **Roots of Unity Filter** (or Binomial Sieve).

### Theorem (Odd vs Even Subsets)
For any finite set of size $n \ge 1$:
$$\sum_{k \text{ odd}} \binom{n}{k} = \sum_{k \text{ even}} \binom{n}{k} = 2^{n-1}$$

### Two Standard Proof Methods
1. **Algebraic (Binomial Theorem):**
   $$(1 + 1)^n = \sum_{k=0}^n \binom{n}{k} = 2^n, \quad (1 - 1)^n = \sum_{k=0}^n (-1)^k \binom{n}{k} = 0$$
   Subtracting gives $2 \sum_{k \text{ odd}} \binom{n}{k} = 2^n \implies \sum_{k \text{ odd}} \binom{n}{k} = 2^{n-1}$.
2. **Bijective (Parity Flip):**
   Distinguish an element $x_0 \in S$. For every subset $A \subseteq S \setminus \{x_0\}$:
   - If $|A|$ is odd, pair it with $A$.
   - If $|A|$ is even, pair it with $A \cup \{x_0\}$ (which has odd size).  
   This establishes a perfect bijection between the $2^{n-1}$ subsets of $S \setminus \{x_0\}$ and all odd-sized subsets of $S$.

---

# 3. Real Analysis & Calculus

---

## 3.1 Connectedness, Totally Disconnected Spaces, & Continuity

### The Topological Core
Let $X$ and $Y$ be topological spaces, and let $f: X \to Y$ be a continuous map.
- If $X$ is **connected**, then its image $f(X)$ is a **connected subset** of $Y$.
- In the real line $\mathbb{R}$ with standard topology, a subset is connected **if and only if it is an interval or a singleton**.

### Totally Disconnected Subspaces
A space $Y$ is **totally disconnected** if its only connected subsets are single points.
The set of rational numbers $\mathbb{Q} \subset \mathbb{R}$ is totally disconnected because between any two distinct rationals $q_1 < q_2$, there exists an irrational number $\alpha \in \mathbb{R} \setminus \mathbb{Q}$.

### Key Consequence
> [!IMPORTANT]
> If $f: [a, b] \to \mathbb{Q}$ is continuous, then $f$ must be **identically constant**.
> *Proof:* $[a, b]$ is connected, so $f([a, b]) \subseteq \mathbb{Q}$ must be connected. The only connected subsets of $\mathbb{Q}$ are singletons $\{c\}$. Hence $f(x) = c$ for all $x \in [a, b]$.

### Worked Example (Distinct from the Exam)
**Problem:** Let $g: [0, 5] \to \mathbb{R}$ be a continuous function such that $(g(x))^2 - 5g(x) + 6 = 0$ for all $x \in [0, 5]$. If $g(1) = 2$, find $g(4)$.

**Step-by-step Solution:**
1. The algebraic equation factors as $(g(x) - 2)(g(x) - 3) = 0$.
2. This implies that for every $x \in [0, 5]$, $g(x) \in \{2, 3\}$.
3. The set $\{2, 3\}$ is a discrete two-point space (disconnected).
4. Since $[0, 5]$ is connected and $g$ is continuous, the image $g([0, 5])$ must be connected.
5. A connected subset of $\{2, 3\}$ can only be a single point: either $\{2\}$ or $\{3\}$.
6. Since $g(1) = 2$, the image must be $\{2\}$, which means $g(x) = 2$ everywhere.
7. Thus $g(4) = 2$.

---

## 3.2 Reverse-Engineering Auxiliary Functions for Rolle's Theorem

### The Objective
Many advanced analysis questions require proving an identity at some unknown point $c \in (a, b)$ given an integral vanishing condition $\int_a^b K(t)f(t)dt = 0$.

### The Systematic 4-Step Construction Method
To prove $\int_0^c x^2 f(x)dx = c \int_0^c x f(x)dx$:
1. **Rewrite as a null target:** $H(c) = c \int_0^c t f(t)dt - \int_0^c t^2 f(t)dt = 0$.
2. **Hypothesize an auxiliary function $g(x)$:** We need $g'(x) = \lambda(x) H(x)$ such that $g(0) = 0$ and $g(1) = 0$.
3. **Inspect the given vanishing integral:** The problem gave $\int_0^1 t(t - 1)^2 f(t)dt = 0$.
   This strongly hints at:
   $$g(x) = \int_0^x t(t - x)^2 f(t)dt$$
   Notice that $g(0) = 0$, and $g(1) = \int_0^1 t(t - 1)^2 f(t)dt = 0$!
4. **Differentiate using Leibniz's Rule:**
   Expand inside before differentiating:
   $$g(x) = \int_0^x (t^3 - 2xt^2 + x^2 t)f(t)dt = \int_0^x t^3 f(t)dt - 2x \int_0^x t^2 f(t)dt + x^2 \int_0^x t f(t)dt$$
   $$\frac{d}{dx}\left[\int_0^x t^3 f(t)dt\right] = x^3 f(x)$$
   $$\frac{d}{dx}\left[-2x \int_0^x t^2 f(t)dt\right] = -2\int_0^x t^2 f(t)dt - 2x \cdot x^2 f(x)$$
   $$\frac{d}{dx}\left[x^2 \int_0^x t f(t)dt\right] = 2x \int_0^x t f(t)dt + x^2 \cdot x f(x)$$
   Summing the three derivatives:
   $$g'(x) = x^3 f(x) - 2x^3 f(x) + x^3 f(x) + 2x \int_0^x t f(t)dt - 2\int_0^x t^2 f(t)dt$$
   $$g'(x) = 2\left[x \int_0^x t f(t)dt - \int_0^x t^2 f(t)dt\right]$$
   The boundary evaluations cancel out to zero!
5. By Rolle's Theorem, there exists $c \in (0, 1)$ such that $g'(c) = 0$, which yields the result immediately.

---

## 3.3 Uniform Convergence & The Weierstrass M-Test

### Definition
A sequence of functions $f_n(x)$ converges **uniformly** to $f(x)$ on a set $E$ if:
$$\lim_{n \to \infty} \sup_{x \in E} |f_n(x) - f(x)| = 0$$

### The Weierstrass M-Test
Let $\sum_{n=1}^\infty u_n(x)$ be a series of functions defined on $E$.
If there exists a sequence of non-negative real numbers $M_n$ such that:
1. $|u_n(x)| \le M_n$ for all $x \in E$ and all $n \ge 1$,
2. $\sum_{n=1}^\infty M_n < \infty$,
then $\sum_{n=1}^\infty u_n(x)$ converges **uniformly and absolutely** on $E$.

### Worked Example (Distinct from the Exam)
**Problem:** Show that the series
$$\sum_{n=1}^\infty \frac{x \sin(n^3 x)}{1 + n^4 x^2}$$
converges uniformly on all of $\mathbb{R}$.

**Step-by-step Solution:**
1. We seek an upper bound for $|u_n(x)| = \frac{|x| |\sin(n^3 x)|}{1 + n^4 x^2}$ that is independent of $x$.
2. We know $|\sin(n^3 x)| \le 1$.
3. By the AM-GM inequality on the denominator:
   $$1 + n^4 x^2 \ge 2\sqrt{1 \cdot n^4 x^2} = 2n^2 |x|$$
4. Therefore, for all $x \ne 0$:
   $$|u_n(x)| \le \frac{|x|}{2n^2 |x|} = \frac{1}{2n^2}$$
   For $x = 0$, $u_n(0) = 0 \le \frac{1}{2n^2}$.
5. Thus, for all $x \in \mathbb{R}$:
   $$|u_n(x)| \le M_n = \frac{1}{2n^2}$$
6. Since $\sum_{n=1}^\infty \frac{1}{2n^2} = \frac{\pi^2}{12} < \infty$, by the Weierstrass M-Test, the series converges uniformly on $\mathbb{R}$.

---

## 3.4 Monotonicity, Fixed Points, & Inverse Function Symmetry

### Theorem (Intersection of $f$ and $f^{-1}$)
Let $f: I \to I$ be an invertible function.
1. **If $f$ is strictly increasing:** Any solution to $f(x) = f^{-1}(x)$ must satisfy:
   $$f(x) = x$$
   *(The graphs of $y = f(x)$ and $y = f^{-1}(x)$ can only intersect on the line $y = x$).*
2. **If $f$ is strictly decreasing:** Solutions to $f(x) = f^{-1}(x)$ can occur off the diagonal line $y = x$. In fact, $f(x) = f^{-1}(x) \iff f(f(x)) = x$.

```
Increasing f(x):
   y = f(x) and y = f^{-1}(x) intersect ONLY along y = x.
   Solving f(x) = f^{-1}(x) is equivalent to solving f(x) = x.

Decreasing f(x):
   Intersection points can exist in symmetric pairs (a, b) and (b, a)
   off the line y = x (e.g. f(x) = -x or f(x) = 1/x).
```

### Proof for Increasing $f$
Assume $f$ is strictly increasing, and suppose $f(x) \ne x$.
- If $f(x) > x$, then applying $f$ maintains inequality: $f(f(x)) > f(x) > x$.
  Thus $f(f(x)) \ne x$, which means $f^{-1}(x) \ne f(x)$.
- If $f(x) < x$, applying $f$ gives $f(f(x)) < f(x) < x$, so $f(f(x)) \ne x$.
Hence, $f(x) = f^{-1}(x)$ is impossible unless $f(x) = x$.

---

## 3.5 Constructing Pathological Functions via Dirichlet & Thomae Methods

### The Goal
Construct a function $f: \mathbb{R} \to \mathbb{R}$ that is continuous at a specified subset $S \subset \mathbb{R}$ and discontinuous everywhere else.

### The General Dirichlet-Modulation Template
Define:
$$f(x) = \begin{cases} h(x) & \text{if } x \in \mathbb{Q} \\ 0 & \text{if } x \in \mathbb{R} \setminus \mathbb{Q} \end{cases}$$
where $h(x)$ is a continuous function on $\mathbb{R}$.
- **At points where $h(a) = 0$:**
  $$|f(x) - f(a)| = |f(x) - 0| \le |h(x)| \to |h(a)| = 0$$
  By the Squeeze Theorem, $f$ is **continuous** at $a$.
- **At points where $h(a) \ne 0$:**
  Approaching $a$ along rationals gives limit $h(a) \ne 0$.
  Approaching $a$ along irrationals gives limit $0$.
  The limit does not exist, so $f$ is **discontinuous** at $a$.

**Conclusion:** $f(x)$ is continuous at $a$ **if and only if** $h(a) = 0$.
Thus, to make $f$ continuous precisely on a set $S$, simply construct a continuous function $h(x)$ whose zero set is exactly $S$!

---

# 4. Complex Analysis & Polynomial Roots

---

## 4.1 Roots of Unity & Logarithmic Differentiation

### The Setup
The $n$-th roots of unity are $1, \omega, \omega^2, \dots, \omega^{n-1}$, where $\omega = e^{2\pi i / n}$.
They are the roots of $x^n - 1 = 0$.
Factor out the root $1$:
$$P(x) = \frac{x^n - 1}{x - 1} = x^{n-1} + x^{n-2} + \dots + x + 1 = \prod_{k=1}^{n-1} (x - a_k)$$

### The Logarithmic Derivative Trick
For any polynomial $P(x) = c \prod_{k=1}^m (x - z_k)$, taking the natural logarithm and differentiating gives:
$$\frac{P'(x)}{P(x)} = \sum_{k=1}^m \frac{1}{x - z_k}$$
Evaluating this identity at specific values of $x$ (such as $x = 1$, $x = 0$, or $x = -1$) yields closed-form sums of reciprocal differences!

### The Geometric Real Part Invariant
For any point on the unit circle $z = e^{i\theta} \ne 1$:
$$\frac{1}{1 - e^{i\theta}} = \frac{1}{1 - \cos\theta - i\sin\theta} = \frac{(1 - \cos\theta) + i\sin\theta}{(1 - \cos\theta)^2 + \sin^2\theta}$$
Notice the denominator simplifies:
$$(1 - \cos\theta)^2 + \sin^2\theta = 1 - 2\cos\theta + \cos^2\theta + \sin^2\theta = 2(1 - \cos\theta)$$
Therefore:
$$\operatorname{Re}\left(\frac{1}{1 - e^{i\theta}}\right) = \frac{1 - \cos\theta}{2(1 - \cos\theta)} = \frac{1}{2} \quad \text{identically!}$$
This geometric constant of $\frac{1}{2}$ holds for **every non-trivial root of unity**, making sums over all $n-1$ non-unit roots equal to $\frac{n-1}{2}$ automatically!

---

## 4.2 Root Localization: Descartes' Rule of Signs & Rouché's Theorem

### Descartes' Rule of Signs
For a real polynomial $P(x) = a_n x^n + \dots + a_1 x + a_0$:
- The number of **positive real roots** is either equal to the number of sign variations between consecutive non-zero coefficients, or less than it by an even integer.
- The number of **negative real roots** is found by applying the same rule to $P(-x)$.

### Rouché's Theorem (Complex Analysis)
Let $C$ be a simple closed contour, and let $P(z)$ and $Q(z)$ be holomorphic functions inside and on $C$.
If the strict inequality:
$$|Q(z)| < |P(z)|$$
holds for all $z$ on the contour $C$, then:
$$P(z) \quad \text{and} \quad P(z) + Q(z)$$
have the **exact same number of zeros** (counting multiplicity) inside $C$.

```
     Contour C: |z| = R
     On the boundary C:
     |Q(z)| < |P(z)|  ==> Dominant term P(z) controls the number of zeros!
     
     Zeros of (P + Q) inside C = Zeros of P inside C
```

### Worked Example (Distinct from the Exam)
**Problem:** Determine the number of roots of $z^5 + 4z^2 + 1 = 0$ in the open disk $|z| < 1$.

**Step-by-step Solution:**
1. Choose the contour $C = \{z \in \mathbb{C} : |z| = 1\}$.
2. Decompose the polynomial into a dominant term $P(z)$ and a perturbation $Q(z)$:
   Let $P(z) = 4z^2$ and $Q(z) = z^5 + 1$.
3. On the circle $|z| = 1$:
   $$|P(z)| = |4z^2| = 4|z|^2 = 4(1)^2 = 4$$
   $$|Q(z)| = |z^5 + 1| \le |z|^5 + 1 = 1 + 1 = 2$$
4. Since $|Q(z)| = 2 < 4 = |P(z)|$ on $C$, the condition of Rouché's Theorem is satisfied.
5. $P(z) = 4z^2$ has a double zero at $z = 0$, so it has exactly **2 zeros** inside $|z| < 1$.
6. Therefore, $z^5 + 4z^2 + 1 = 0$ has exactly **2 zeros** inside the unit disk $|z| < 1$.

---

## 4.3 The Maximum Modulus Principle & Geometric Extremal Products

### Theorem (Maximum Modulus Principle)
If $F(z)$ is holomorphic on a bounded domain $D \subset \mathbb{C}$ and continuous on its closure $\bar{D}$, then the maximum of $|F(z)|$ on $\bar{D}$ is attained on the **boundary** $\partial D$:
$$|F(z)| < \max_{w \in \partial D} |F(w)| \quad \text{for all } z \in \operatorname{int}(D)$$
unless $F$ is a constant function.

### Application to Geometric Distance Products
Let $A_1, \dots, A_m$ be points on the unit circle. The product of distances from a variable interior point $P$ to the vertices is:
$$\prod_{k=1}^m |PA_k| = |F(z)| \quad \text{where } F(z) = \prod_{k=1}^m (z - z_{A_k})$$
Because $F(z)$ is a polynomial (hence holomorphic everywhere):
1. The maximum of $\prod |PA_k|$ over any polygon inscribed in the circle **cannot occur in the interior**.
2. It must occur on the **boundary edges**.
3. On an edge, the point is collinear with two vertices, allowing the use of the **Power of a Point (Intersecting Chords Theorem)** to bound the product!

---

# 5. Linear Algebra & Matrix Theory

---

## 5.1 Matrix Commutators, Lie Brackets, & Nilpotency

### Definitions
- **Commutator (Lie Bracket):** $[A, B] = AB - BA$.
- **Nilpotent Matrix:** A matrix $B \in M_n(\mathbb{C})$ such that $B^k = 0$ for some positive integer $k$.

### Trace Properties
Because $\operatorname{Tr}(XY) = \operatorname{Tr}(YX)$ for any matrices $X, Y$:
$$\operatorname{Tr}([A, B]) = \operatorname{Tr}(AB - BA) = 0$$
Any commutator matrix must have trace zero!

### The Power Identity Induction Technique
When given a relation like $AB^2 - B^2 A = B$, we examine higher powers:
$$AB^{2^k} - B^{2^k}A = 2^{k-1} B^{2^k - 1}$$
Taking any submultiplicative matrix norm $\|\cdot\|$:
$$2^{k-1}\|B^{2^k - 1}\| \le 2\|A\|\|B^{2^k}\| \le 2\|A\|\|B\| \|B^{2^k - 1}\|$$
If $B$ were not nilpotent, $\|B^{2^k - 1}\| > 0$ for all $k$, leading to:
$$2^{k-1} \le 2\|A\|\|B\|$$
Since $2^{k-1} \to \infty$ as $k \to \infty$, this yields a contradiction, forcing $B$ to be nilpotent!

### Worked Example (Distinct from the Exam)
**Problem:** Let $A, B \in M_n(\mathbb{C})$ satisfy the commutator relation $AB - BA = A$.
1. Prove that $A$ is a nilpotent matrix.
2. If $n = 2$, give an explicit non-zero pair of matrices $A, B$ satisfying this relation.

**Step-by-step Solution:**
1. **Proof of Nilpotency:**  
   Notice that $A = [B, -A]$. By induction on powers:
   $$A^2 = A(AB - BA) \implies A^k B - B A^k = k A^k$$
   Taking norms:
   $$k \|A^k\| = \|A^k B - B A^k\| \le 2\|B\| \|A^k\|$$
   If $A$ were not nilpotent, $\|A^k\| \ne 0$, so dividing gives $k \le 2\|B\|$ for all integers $k \ge 1$.
   Since $k$ can be arbitrarily large, this is impossible. Thus $A^k = 0$ for some $k$, so $A$ is nilpotent.
2. **Explicit Example ($n = 2$):**  
   Let $A = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}$ and $B = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$.  
   Then:
   $$AB = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}\begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$$
   $$BA = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}\begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix} = A$$
   $$AB - BA = 0 - A = -A \quad (\text{or swap signs of } B \text{ to get } AB - BA = A).$$
   Setting $B = \begin{pmatrix} 0 & 0 \\ 0 & -1 \end{pmatrix}$ gives $AB - BA = A$.

---

## 5.2 Quadratic Forms, $L^2$ Inner Products, & The Hilbert Matrix

### The Hilbert Matrix
The $n \times n$ matrix $H$ with entries:
$$H_{ij} = \frac{1}{i + j - 1}$$
is the famous **Hilbert Matrix**.

### The Integral Inner Product Representation
The entry $\frac{1}{i + j - 1}$ is the $L^2([0, 1])$ inner product of the monomial basis functions $x^{i-1}$ and $x^{j-1}$:
$$\int_0^1 x^{i-1} x^{j-1} dx = \int_0^1 x^{i+j-2} dx = \left[\frac{x^{i+j-1}}{i+j-1}\right]_0^1 = \frac{1}{i+j-1}$$

### Positive Definiteness Proof
For any real vector $\mathbf{a} = (a_1, \dots, a_n)^T \in \mathbb{R}^n$:
$$\mathbf{a}^T H \mathbf{a} = \sum_{i=1}^n \sum_{j=1}^n a_i a_j H_{ij} = \sum_{i=1}^n \sum_{j=1}^n a_i a_j \int_0^1 x^{i-1} x^{j-1} dx$$
By linearity of integration:
$$= \int_0^1 \left(\sum_{i=1}^n a_i x^{i-1}\right) \left(\sum_{j=1}^n a_j x^{j-1}\right) dx = \int_0^1 [P(x)]^2 dx$$
where $P(x) = \sum_{i=1}^n a_i x^{i-1}$.
- Because $[P(x)]^2 \ge 0$, the integral is always $\ge 0$.
- Because a non-zero polynomial has only finitely many roots, $[P(x)]^2$ cannot be identically zero on $[0, 1]$ unless all coefficients $a_i = 0$.
- Thus $\mathbf{a}^T H \mathbf{a} > 0$ for all $\mathbf{a} \ne \mathbf{0}$, proving $H$ is **strictly positive definite**.

---

# 6. Differential Equations

---

## 6.1 Forming Differential Equations for Geometric Families of Curves

### The General Procedure
A family of geometric curves with $k$ arbitrary parameters requires $k$ differentiations to eliminate all parameters:
1. Write down the Cartesian equation containing the parameter(s) $c_1, \dots, c_k$.
2. Differentiate implicitly with respect to $x$ to generate derivative equations.
3. Solve the system algebraically to eliminate the parameter(s), arriving at a relation involving only $x, y, y', y'', \dots$.

### Worked Example (Distinct from the Exam)
**Problem:** Find the differential equation of the family of all parabolas having their vertex at the origin and focus on the $y$-axis.

**Step-by-step Solution:**
1. The standard equation of such parabolas is:
   $$x^2 = 4ay$$
   where $a$ is the arbitrary parameter ($a \ne 0$).
2. Differentiate implicitly with respect to $x$:
   $$2x = 4a \frac{dy}{dx} \implies 4a = \frac{2x}{y'}$$
3. Substitute $4a = \frac{2x}{y'}$ back into $x^2 = 4ay$:
   $$x^2 = \left(\frac{2x}{y'}\right) y$$
4. Clear denominators and rearrange:
   $$x^2 y' = 2xy \implies x(x y' - 2y) = 0$$
   For $x \ne 0$:
   $$x \frac{dy}{dx} - 2y = 0$$

---

# 7. Comprehensive Problem-Solving Checklist

When entering the examination hall, keep this tactical checklist at hand:

| Trigger / Clue in Problem | Immediate Mathematical Technique to Deploy |
| :--- | :--- |
| **Integers in GP with AM condition** | Factor into $a(r-1)^2 = K$; check square divisors of $K$. |
| **Polygon triangles / diagonals** | Use complementary counting: Total $\binom{n}{3} - n(n-4) - n$. |
| **Continuous map into $\mathbb{Q}$ or discrete sets** | Connectedness of domain forces constant value. |
| **Fixed points / $f(x) = f^{-1}(x)$** | If $f$ is increasing, solve $f(x) = x$; if decreasing, check 2-cycles $f(f(x)) = x$. |
| **GCD of polynomial values $\gcd(P(n), Q(n))$** | Use Euclidean algorithm to find $A(n)P(n) + B(n)Q(n) = C \in \mathbb{Z}$. |
| **Parity of weights / sums after removing any element** | Mod 2 invariance forces all elements to have equal parity; use Infinite Descent. |
| **Integral identity at unknown point $c \in (a, b)$** | Define $g(x) = \int_0^x K(t, x)f(t)dt$ and apply Rolle's Theorem. |
| **Series of trigonometric/exponential functions** | Weierstrass M-Test: find bound $M_n$ with $\sum M_n < \infty$. |
| **Sum of reciprocal roots of unity** | Take logarithmic derivative of $\frac{x^n-1}{x-1}$ or use $\operatorname{Re}\left(\frac{1}{1-\zeta}\right) = \frac{1}{2}$. |
| **Valuation of recurrence $a_{n+1} = a_n^2 - 2c^{2^n}$** | Use induction: lower-order term $2c^{2^{n-1}}$ dominates $p$-adic valuation. |
| **Counting complex roots in a disk** | Rouché's Theorem: find dominant term on boundary circle $|z| = R$. |
| **Commutator identity $[A, B^2] = B$** | Induct on $[A, B^{2^k}] = 2^{k-1}B^{2^k-1}$; take norms to prove nilpotency. |
| **Sum of fractions $\frac{a_i a_j}{i+j-1}$** | Express as $\int_0^1 [P(x)]^2 dx \ge 0$ via Hilbert matrix inner product. |
| **Product of distances to cyclic polygon vertices** | Apply Maximum Modulus Principle to boundary, then Intersecting Chords. |
