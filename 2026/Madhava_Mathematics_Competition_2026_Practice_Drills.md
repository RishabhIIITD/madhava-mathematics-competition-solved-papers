# Madhava Mathematics Competition — 2026
## Twin & Drill Practice Problem Set: Master Competition Techniques

**Companion Booklet to the 2026 Examination**  
**Organized by:** Bhaskaracharya Pratishthana, Pune & NBHM  
**Target Audience:** Undergraduate Students & Mathematics Olympiad Aspirants  

---

### Why This Problem Set Exists
Reading a mathematical solution often creates an **illusion of competence**: the proof looks intuitive and obvious in hindsight. Real mastery occurs only when you apply the exact same mathematical principles (such as *Rouché's Theorem*, *p-adic valuations*, *auxiliary Rolle's kernels*, or *infinite descent*) to completely fresh, unseen problems.

### How to Use This Booklet
1. **Section A (Problems):** Work through each problem independently with a pen and blank paper. Do not look at the hints until you have spent at least 15–20 minutes attempting the problem.
2. **Section B (Tiered Hints):** 
   - **Hint 1:** Gives the primary theorem, invariant, or strategic direction.
   - **Hint 2:** Gives the explicit algebraic substitution or critical intermediate milestone.
3. **Section C (Detailed Solutions):** Read the full solutions to benchmark your rigor, notation, and clarity against examiner expectations.

---

# Section A: The Problem Set

---

### Problem 1 (Diophantine Progressions)
Let $u < v < w$ be three positive integers forming a geometric progression whose common ratio $r$ is an integer. If the arithmetic mean of $u, v, w$ exceeds the middle term by $18$, determine all possible values of the first term $u$.

---

### Problem 2 (Combinatorics on Polygons)
The 16 vertices of a regular 16-gon are connected in all possible triples to form triangles.
1. How many such triangles share **exactly one side** with the 16-gon?
2. How many such triangles share **no sides** with the 16-gon?

---

### Problem 3 (Piecewise Continuity & Optimization)
Let $g: \mathbb{R} \to \mathbb{R}$ be defined by:
$$g(x) = \begin{cases} mx + c & \text{if } x < -2 \\ x^3 + 4 & \text{if } -2 \le x < 2 \\ 5x + 2 & \text{if } x \ge 2 \end{cases}$$
If $g$ is continuous everywhere on $\mathbb{R}$, determine the minimum possible value of the product $mc$.

---

### Problem 4 (Connectedness & Functional Constraints)
Let $f: [0, 4] \to \mathbb{R}$ be a continuous function such that:
$$(f(x))^3 - 4(f(x))^2 - f(x) + 4 = 0 \quad \text{for all } x \in [0, 4]$$
If $f(1) = 4$, evaluate the definite integral $\int_0^4 f(x) dx$.

---

### Problem 5 (Fixed Points & Inverse Functions)
Let $h: [-2, \infty) \to [-2, \infty)$ be defined by $h(x) = (x + 2)^3 - 2$. Find all real solutions to the equation:
$$h(x) = h^{-1}(x)$$

---

### Problem 6 (Exponential Diophantine Equations)
Find the number of real solutions to the equation:
$$2 + |e^x - 2| = e^x(e^x - 3)$$

---

### Problem 7 (Subset Parity & Binomial Coefficients)
Let $S = \{1, 2, 3, \dots, 2026\}$. Find the number of subsets of $S$ whose cardinality is congruent to $1 \pmod 2$.

---

### Problem 8 (Differential Equations of Geometric Families)
Find the ordinary differential equation satisfied by the family of all circles in the $xy$-plane that are tangent to the $x$-axis at the origin $(0, 0)$.

---

### Problem 9 (Uniform Convergence of Function Series)
Prove that the series:
$$\sum_{n=1}^\infty \frac{x \sin(n^2 x)}{1 + n^4 x^2}$$
converges uniformly on all of $\mathbb{R}$.

---

### Problem 10 (Roots of Unity Sums)
Let $1, \zeta_1, \zeta_2, \dots, \zeta_{n-1}$ be the $n$-th roots of unity for $n \ge 3$. Prove that:
$$\sum_{k=1}^{n-1} \frac{1}{(1 - \zeta_k)^2} = -\frac{(n - 1)(n - 5)}{12}$$

---

### Problem 11 (Auxiliary Functions for Rolle's Theorem)
Let $f: [0, 1] \to \mathbb{R}$ be a continuous function such that $\int_0^1 x(1 - x)^2 f(x) dx = 0$. Prove that there exists a number $c \in (0, 1)$ such that:
$$\int_0^c x^2 f(x) dx = c \int_0^c x f(x) dx$$

---

### Problem 12 (Integer GCD of Polynomials)
Let $P(n) = 2n^2 + 5n + 2$ and $Q(n) = 3n + 1$. Determine all possible values of $\gcd(P(n), Q(n))$ as $n$ ranges over the integers.

---

### Problem 13 (Hilbert Kernel & Quadratic Forms)
Let $c_1, c_2, \dots, c_n$ be real numbers. Prove that:
$$\sum_{1 \le i, j \le n} \frac{c_i c_j}{i + j + 1} \ge 0$$
and determine the necessary and sufficient condition under which equality holds.

---

### Problem 14 (Parity Invariants & Infinite Descent)
Suppose 8 integers $a_1, a_2, \dots, a_8$ have the property that whenever any one of them is removed, the remaining 7 integers can be split into two subsets with equal sums. Prove that $a_1 = a_2 = \dots = a_8 = 0$.

---

### Problem 15 ($p$-adic Valuations in Non-linear Recurrences)
Let $\alpha, \beta$ be the roots of $x^2 - 6x + 21 = 0$. Let $p = 3$.
1. Find the largest power of $3$ dividing $\alpha^2 + \beta^2$.
2. Find the largest power of $3$ dividing $\alpha^4 + \beta^4$.
3. For every integer $m \ge 1$, find the largest power of $3$ dividing $\alpha^{2^m} + \beta^{2^m}$.

---

### Problem 16 (Root Localization & Rouché's Theorem)
Consider the polynomial equation $z^7 - 7z^6 + 1 = 0$.
1. Prove that it has a unique root $x_0$ in the real interval $(0, 1)$.
2. Prove that every non-real complex root $z$ satisfies $|z| \le x_0$.

---

### Problem 17 (Matrix Commutators & Nilpotency)
Let $A, B \in M_n(\mathbb{C})$ satisfy the commutator relation:
$$AB^3 - B^3 A = B^2$$
1. Prove that $B$ must be a nilpotent matrix.
2. If $B = \begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{pmatrix}$, does there exist an $n \times n$ matrix $A$ satisfying the relation? Justify.

---

### Problem 18 (Extremal Geometric Products & Maximum Modulus)
Let $A, B, C$ be the vertices of an equilateral triangle inscribed in the unit circle centered at $O$. Let $P$ be any point in the interior of $\triangle ABC$. Prove that:
$$|PA||PB||PC| < 1$$

---

# Section B: Tiered Hints

---

#### Hints for Problem 1
- **Hint 1:** Express $v = ur$ and $w = ur^2$. Set up $\frac{u + ur + ur^2}{3} = ur + 18$ and clear fractions.
- **Hint 2:** Factor the relation into $u(r - 1)^2 = 54$. Find all positive square divisors of $54$.

#### Hints for Problem 2
- **Hint 3:** For (1), choose an edge in $16$ ways, then identify how many vertices are forbidden from being the third vertex to avoid 2 shared edges.
- **Hint 4:** For (2), use complementary counting $N_0 = \binom{16}{3} - N_1 - N_2$, or apply $N_0 = \frac{n(n-4)(n-5)}{6}$ with $n = 16$.

#### Hints for Problem 3
- **Hint 1:** Check continuity at $x = 2$ first. Does continuity at $x = 2$ impose any restrictions on $m$ and $c$? Then examine $x = -2$.
- **Hint 2:** Continuity at $x = -2$ gives $-2m + c = (-2)^3 + 4 = -4 \implies c = 2m - 4$. Express $mc = 2m^2 - 4m$ and complete the square.

#### Hints for Problem 4
- **Hint 1:** Factor the cubic polynomial $t^3 - 4t^2 - t + 4 = 0$.
- **Hint 2:** The factors are $(t - 1)(t + 1)(t - 4) = 0$. Use the fact that the continuous image of the connected interval $[0, 4]$ must be connected.

#### Hints for Problem 5
- **Hint 1:** Differentiate $h(x)$ to check whether $h$ is strictly monotonic on $[-2, \infty)$.
- **Hint 2:** Since $h'(x) > 0$ for $x > -2$, $h$ is strictly increasing. Use the theorem that $h(x) = h^{-1}(x) \iff h(x) = x$.

#### Hints for Problem 6
- **Hint 1:** Substitute $u = e^x > 0$. Split into two cases: $u \ge 2$ and $0 < u < 2$.
- **Hint 2:** In each case, solve the resulting quadratic equation and verify whether the roots lie in the respective domain.

#### Hints for Problem 7
- **Hint 1:** Summing over odd sizes is $\sum_{k \text{ odd}} \binom{n}{k}$.
- **Hint 2:** Consider the binomial expansion of $(1 + 1)^n - (1 - 1)^n$.

#### Hints for Problem 8
- **Hint 1:** A circle tangent to the $x$-axis at the origin has center $(0, b)$ and radius $|b|$. Write its equation: $x^2 + (y - b)^2 = b^2$.
- **Hint 2:** Differentiate implicitly with respect to $x$ to find $b$ in terms of $x, y, y'$, then substitute $b$ back.

#### Hints for Problem 9
- **Hint 1:** Apply the AM-GM inequality to the denominator $1 + n^4 x^2$.
- **Hint 2:** $1 + n^4 x^2 \ge 2\sqrt{n^4 x^2} = 2n^2 |x|$. Bound the numerator using $|\sin| \le 1$ to apply the Weierstrass M-Test.

#### Hints for Problem 10
- **Hint 1:** Recall the polynomial $P(x) = \frac{x^n - 1}{x - 1} = \prod_{k=1}^{n-1} (x - \zeta_k)$. Its logarithmic derivative is $\frac{P'(x)}{P(x)} = \sum_{k=1}^{n-1} \frac{1}{x - \zeta_k}$.
- **Hint 2:** Differentiate $\frac{P'(x)}{P(x)}$ with respect to $x$: $\frac{d}{dx}\left[\frac{P'(x)}{P(x)}\right] = \frac{P''(x)P(x) - [P'(x)]^2}{[P(x)]^2} = -\sum_{k=1}^{n-1} \frac{1}{(x - \zeta_k)^2}$. Compute $P(1), P'(1), P''(1)$ carefully.

#### Hints for Problem 11
- **Hint 1:** Define the auxiliary function $g(x) = \int_0^x t(t - x)^2 f(t) dt$.
- **Hint 2:** Verify $g(0) = 0$ and $g(1) = 0$. Differentiate using Leibniz's rule and apply Rolle's Theorem.

#### Hints for Problem 12
- **Hint 1:** Multiply $P(n)$ by 9 to eliminate $n$ through division by $3n + 1$.
- **Hint 2:** $9P(n) = (3n + 1)(6n + 13) + 5$. Show that the gcd must divide 5, then check if both 1 and 5 can be achieved.

#### Hints for Problem 13
- **Hint 1:** Express $\frac{1}{i + j + 1}$ as an integral $\int_0^1 x^{i+j} dx = \int_0^1 x^i x^j dx$.
- **Hint 2:** Interchange the finite sum and integral to obtain $\int_0^1 \left(\sum c_i x^i\right)^2 dx$. When can the integral of a squared polynomial vanish?

#### Hints for Problem 14
- **Hint 1:** Let $S = \sum_{i=1}^8 a_i$. The condition implies $S - a_k = 2 A_k$, so $a_k \equiv S \pmod 2$.
- **Hint 2:** If all $a_i$ are odd, what is the parity of $S$? What is the parity of $S - a_k$? Apply the Method of Infinite Descent.

#### Hints for Problem 15
- **Hint 1:** Vieta's formulas give $\alpha + \beta = 6$ and $\alpha\beta = 21$. Note $v_3(6) = 1$ and $v_3(21) = 1$.
- **Hint 2:** Use $a_m = \alpha^{2^m} + \beta^{2^m}$ with $a_{m+1} = a_m^2 - 2(21)^{2^m}$. Use mathematical induction to prove $a_m \equiv 2(21)^{2^{m-1}} \pmod{3^{2^{m-1}+1}}$.

#### Hints for Problem 16
- **Hint 1:** For (1), compute $f(0)$ and $f(1)$, and check the derivative $f'(x)$ on $(0, 1)$.
- **Hint 2:** For (2), choose the circle $|z| = R$ with $x_0 < R < 1$. Show that $|z^7 + 1| < |-7z^6|$ on this circle and apply Rouché's Theorem.

#### Hints for Problem 17
- **Hint 1:** Derive a recurrence for $[A, B^{3 \cdot 2^k}]$ by multiplying on the right by $B^{3 \cdot 2^k}$ and substituting.
- **Hint 2:** Take matrix norms to find an inequality of the form $2^k \le C$. For part (2), compute $B^3$.

#### Hints for Problem 18
- **Hint 1:** Place the vertices in the complex plane: $1, e^{i 2\pi/3}, e^{i 4\pi/3}$. Notice $(z - 1)(z - \omega)(z - \omega^2) = z^3 - 1$.
- **Hint 2:** Apply the Maximum Modulus Principle to $F(z) = z^3 - 1$ on the compact region $\triangle ABC$. Check the value of $|F(w)|$ on the boundary edges.

---

# Section C: Detailed Step-by-Step Solutions

---

### Solution 1 (Diophantine Progressions)
Let the terms be $u, v = ur, w = ur^2$ with $r \in \mathbb{Z}, r \ge 2$, and $u \in \mathbb{Z}^+$.
$$\frac{u + ur + ur^2}{3} = ur + 18$$
Multiply by 3:
$$u(1 + r + r^2) = 3ur + 54 \implies u(r^2 - 2r + 1) = 54 \implies u(r - 1)^2 = 54$$
Since $u$ and $r$ are positive integers, $(r - 1)^2$ must be a perfect square dividing $54$.  
The prime factorization of $54$ is $2 \times 3^3$.  
The positive square divisors of $54$ are $1^2 = 1$ and $3^2 = 9$.

- **Case 1:** $(r - 1)^2 = 1 \implies r - 1 = 1 \implies r = 2$.  
  Then $u = \frac{54}{1} = 54$.  
  *Check:* $u = 54, v = 108, w = 216$. AM $= \frac{54+108+216}{3} = 126 = 108 + 18$. Valid!

- **Case 2:** $(r - 1)^2 = 9 \implies r - 1 = 3 \implies r = 4$.  
  Then $u = \frac{54}{9} = 6$.  
  *Check:* $u = 6, v = 24, w = 96$. AM $= \frac{6+24+96}{3} = 42 = 24 + 18$. Valid!

**Final Answer:** The possible values of $u$ are **$6$** and **$54$**.

---

### Solution 2 (Combinatorics on Polygons)
Let $n = 16$.
1. **Triangles sharing exactly 1 side:**  
   - Choose 1 edge of the 16-gon: $16$ choices.
   - For an edge $(v_1, v_2)$, the third vertex cannot be $v_1, v_2$ (endpoints), nor $v_{16}, v_3$ (which would create a 2-edge triangle).  
   - This excludes $4$ vertices out of $16$, leaving $16 - 4 = 12$ choices for the third vertex.
   $$N_1 = 16 \times 12 = 192$$

2. **Triangles sharing NO sides:**  
   - Total triangles: $\binom{16}{3} = \frac{16 \times 15 \times 14}{6} = 560$.
   - Triangles sharing 2 sides: $N_2 = 16$ (consecutive vertex triples).
   - Triangles sharing no sides:
     $$N_0 = \text{Total} - N_1 - N_2 = 560 - 192 - 16 = 352$$
   - *Alternative formula check:*
     $$N_0 = \frac{n(n-4)(n-5)}{6} = \frac{16 \times 12 \times 11}{6} = 16 \times 2 \times 11 = 352$$

**Final Answer:** (1) **192 triangles** share exactly 1 side. (2) **352 triangles** share no sides.

---

### Solution 3 (Piecewise Continuity & Optimization)
1. **Continuity at $x = 2$:**  
   $$\lim_{x \to 2^-} g(x) = 2^3 + 4 = 12, \quad \lim_{x \to 2^+} g(x) = 5(2) + 2 = 12$$
   Since both one-sided limits equal $g(2) = 12$, $g$ is automatically continuous at $x = 2$ for all $m, c$.

2. **Continuity at $x = -2$:**  
   $$\lim_{x \to -2^+} g(x) = (-2)^3 + 4 = -8 + 4 = -4$$
   $$\lim_{x \to -2^-} g(x) = m(-2) + c = -2m + c$$
   For continuity:
   $$-2m + c = -4 \implies c = 2m - 4$$

3. **Optimizing the product $mc$:**  
   $$mc = m(2m - 4) = 2m^2 - 4m = 2(m^2 - 2m + 1) - 2 = 2(m - 1)^2 - 2$$
   Since $m \in \mathbb{R}$, $(m - 1)^2 \ge 0$.  
   The minimum occurs when $m = 1$, giving $c = 2(1) - 4 = -2$.  
   $$\min(mc) = -2$$

**Final Answer:** The minimum possible value of $mc$ is **$-2$**.

---

### Solution 4 (Connectedness & Functional Constraints)
1. Factor the cubic algebraic condition:
   $$t^3 - 4t^2 - t + 4 = t^2(t - 4) - 1(t - 4) = (t^2 - 1)(t - 4) = (t - 1)(t + 1)(t - 4) = 0$$
2. Thus, for each $x \in [0, 4]$, $f(x) \in \{-1, 1, 4\}$.
3. The set $\{-1, 1, 4\}$ is a discrete three-point space.
4. The interval $[0, 4]$ is connected, and $f$ is continuous, so the image $f([0, 4])$ must be connected.
5. The only connected subsets of $\{-1, 1, 4\}$ are single points.
6. Since $f(1) = 4$, we must have $f(x) = 4$ for all $x \in [0, 4]$.
7. The integral evaluates to:
   $$\int_0^4 f(x) dx = \int_0^4 4 dx = 4 \times 4 = 16$$

**Final Answer:** $\int_0^4 f(x) dx = \mathbf{16}$.

---

### Solution 5 (Fixed Points & Inverse Functions)
1. Differentiate $h(x) = (x + 2)^3 - 2$:
   $$h'(x) = 3(x + 2)^2 \ge 0 \quad \text{for all } x \ge -2$$
   Since $h'(x) > 0$ for $x > -2$, $h$ is strictly increasing on $[-2, \infty)$.
2. For any strictly increasing function, the solutions to $h(x) = h^{-1}(x)$ are precisely the solutions to $h(x) = x$:
   $$(x + 2)^3 - 2 = x \implies x^3 + 6x^2 + 12x + 8 - 2 = x$$
   $$x^3 + 6x^2 + 11x + 6 = 0$$
3. Factoring the cubic polynomial:
   $$(x + 1)(x + 2)(x + 3) = 0$$
   The roots are $x = -1, x = -2, x = -3$.
4. Check the domain constraint $x \ge -2$:
   - $x = -1 \ge -2$ (Valid)
   - $x = -2 \ge -2$ (Valid)
   - $x = -3 < -2$ (Outside domain, rejected)

**Final Answer:** The solution set is **$\{-2, -1\}$**.

---

### Solution 6 (Exponential Diophantine Equations)
Let $u = e^x > 0$. The equation becomes:
$$2 + |u - 2| = u(u - 3) = u^2 - 3u$$

- **Case 1: $u \ge 2$ ($x \ge \ln 2$):**  
  $|u - 2| = u - 2$.
  $$2 + u - 2 = u^2 - 3u \implies u = u^2 - 3u \implies u^2 - 4u = 0$$
  $$u(u - 4) = 0$$
  Since $u > 0$, $u = 4$.  
  Since $4 \ge 2$, $x = \ln 4 = 2\ln 2$ is a valid real solution.

- **Case 2: $0 < u < 2$ ($x < \ln 2$):**  
  $|u - 2| = 2 - u$.
  $$2 + 2 - u = u^2 - 3u \implies 4 - u = u^2 - 3u \implies u^2 - 2u - 4 = 0$$
  $$u = \frac{2 \pm \sqrt{4 + 16}}{2} = 1 \pm \sqrt{5}$$
  Since $u > 0$, we consider $u = 1 + \sqrt{5} \approx 3.236$.  
  However, $1 + \sqrt{5} > 2$, which does not lie in $(0, 2)$. The negative root $1 - \sqrt{5} < 0$ is rejected.  
  Hence, no solutions in Case 2.

**Final Answer:** There is exactly **$1$ real solution** ($x = \ln 4$).

---

### Solution 7 (Subset Parity & Binomial Coefficients)
Let $|S| = n = 2026$.  
The number of subsets with odd cardinality is:
$$N_{\text{odd}} = \sum_{k \text{ odd}} \binom{n}{k} = \binom{n}{1} + \binom{n}{3} + \binom{n}{5} + \dots + \binom{n}{2025}$$
From the binomial theorem:
$$(1 + 1)^n - (1 - 1)^n = 2^n - 0 = 2 \sum_{k \text{ odd}} \binom{n}{k}$$
$$N_{\text{odd}} = \frac{2^n}{2} = 2^{n - 1} = 2^{2025}$$

**Final Answer:** **$2^{2025}$ subsets**.

---

### Solution 8 (Differential Equations of Geometric Families)
1. A circle tangent to the $x$-axis at $(0, 0)$ has center $(0, b)$ and radius $|b|$ ($b \ne 0$).  
   Its equation is:
   $$x^2 + (y - b)^2 = b^2 \implies x^2 + y^2 - 2by = 0 \implies 2b = \frac{x^2 + y^2}{y}$$
2. Differentiate implicitly with respect to $x$:
   $$2x + 2y y' - 2b y' = 0 \implies 2b y' = 2x + 2y y' \implies 2b = \frac{2x + 2yy'}{y'}$$
3. Equating the two expressions for $2b$:
   $$\frac{x^2 + y^2}{y} = \frac{2x + 2yy'}{y'}$$
   $$(x^2 + y^2)y' = 2xy + 2y^2 y'$$
   $$(x^2 - y^2)y' - 2xy = 0 \implies (x^2 - y^2)\frac{dy}{dx} - 2xy = 0$$

**Final Answer:** $(x^2 - y^2)\frac{dy}{dx} - 2xy = 0$.

---

### Solution 9 (Uniform Convergence of Function Series)
Let $u_n(x) = \frac{x \sin(n^2 x)}{1 + n^4 x^2}$.
1. Bounding the numerator: $|\sin(n^2 x)| \le 1$ for all $x \in \mathbb{R}$.
2. For the denominator, apply the AM-GM inequality:
   $$1 + n^4 x^2 \ge 2\sqrt{1 \cdot n^4 x^2} = 2n^2 |x|$$
3. For all $x \ne 0$:
   $$|u_n(x)| \le \frac{|x| \cdot 1}{2n^2 |x|} = \frac{1}{2n^2}$$
   For $x = 0$, $u_n(0) = 0 \le \frac{1}{2n^2}$.
4. Thus, for all $x \in \mathbb{R}$ and $n \ge 1$:
   $$|u_n(x)| \le M_n = \frac{1}{2n^2}$$
5. The scalar series $\sum_{n=1}^\infty M_n = \frac{1}{2} \sum_{n=1}^\infty \frac{1}{n^2} = \frac{\pi^2}{12} < \infty$ converges.
6. By the **Weierstrass M-Test**, the series converges uniformly and absolutely on all of $\mathbb{R}$. $\blacksquare$

---

### Solution 10 (Roots of Unity Sums)
Let $P(x) = \frac{x^n - 1}{x - 1} = \prod_{k=1}^{n-1} (x - \zeta_k)$.
1. Taking the logarithmic derivative:
   $$\frac{P'(x)}{P(x)} = \sum_{k=1}^{n-1} \frac{1}{x - \zeta_k}$$
2. Differentiating both sides with respect to $x$:
   $$\frac{d}{dx}\left[\frac{P'(x)}{P(x)}\right] = \frac{P''(x)P(x) - [P'(x)]^2}{[P(x)]^2} = -\sum_{k=1}^{n-1} \frac{1}{(x - \zeta_k)^2}$$
3. Thus:
   $$\sum_{k=1}^{n-1} \frac{1}{(1 - \zeta_k)^2} = \frac{[P'(1)]^2 - P''(1)P(1)}{[P(1)]^2}$$
4. Compute the values at $x = 1$:
   - $P(x) = x^{n-1} + x^{n-2} + \dots + 1 \implies P(1) = n$
   - $P'(x) = \sum_{j=1}^{n-1} j x^{j-1} \implies P'(1) = \frac{n(n-1)}{2}$
   - $P''(x) = \sum_{j=2}^{n-1} j(j-1) x^{j-2} \implies P''(1) = \frac{(n-1)(n)(n-2)}{3}$
5. Substitute these into the formula:
   $$\frac{[P'(1)]^2 - P''(1)P(1)}{[P(1)]^2} = \frac{\frac{n^2 (n-1)^2}{4} - \frac{n^2 (n-1)(n-2)}{3}}{n^2}$$
   $$= \frac{(n-1)^2}{4} - \frac{(n-1)(n-2)}{3} = \frac{n-1}{12} \left[ 3(n-1) - 4(n-2) \right]$$
   $$= \frac{n-1}{12} [3n - 3 - 4n + 8] = \frac{(n-1)(5 - n)}{12} = -\frac{(n-1)(n-5)}{12} \quad \blacksquare$$

---

### Solution 11 (Auxiliary Functions for Rolle's Theorem)
1. Define $g: [0, 1] \to \mathbb{R}$ by:
   $$g(x) = \int_0^x t(t - x)^2 f(t) dt$$
2. Boundary values:
   - $g(0) = \int_0^0 = 0$.
   - $g(1) = \int_0^1 t(t - 1)^2 f(t) dt = \int_0^1 x(1 - x)^2 f(x) dx = 0$ (given).
   - Since $f$ is continuous, $g$ is differentiable on $(0, 1)$ and continuous on $[0, 1]$.
3. Differentiating $g(x)$:
   $$g(x) = \int_0^x (t^3 - 2xt^2 + x^2 t)f(t) dt = \int_0^x t^3 f(t) dt - 2x \int_0^x t^2 f(t) dt + x^2 \int_0^x t f(t) dt$$
   $$g'(x) = x^3 f(x) - \left[2 \int_0^x t^2 f(t) dt + 2x^3 f(x)\right] + \left[2x \int_0^x t f(t) dt + x^3 f(x)\right]$$
   $$g'(x) = 2x \int_0^x t f(t) dt - 2 \int_0^x t^2 f(t) dt$$
4. By Rolle's Theorem, there exists $c \in (0, 1)$ such that $g'(c) = 0$:
   $$2c \int_0^c t f(t) dt - 2 \int_0^c t^2 f(t) dt = 0 \implies \int_0^c x^2 f(x) dx = c \int_0^c x f(x) dx \quad \blacksquare$$

---

### Solution 12 (Integer GCD of Polynomials)
1. Multiply $P(n) = 2n^2 + 5n + 2$ by $9$:
   $$9P(n) = 18n^2 + 45n + 18$$
2. Divide by $Q(n) = 3n + 1$:
   $$18n^2 + 45n + 18 = (3n + 1)(6n + 13) + 5$$
   $$9P(n) - (6n + 13)Q(n) = 5$$
3. Let $d = \gcd(P(n), Q(n))$. Since $d \mid P(n)$ and $d \mid Q(n)$, $d$ must divide $5$.
   Thus $d \in \{1, 5\}$.
4. Achievability:
   - For $n = 0$: $P(0) = 2, Q(0) = 1 \implies \gcd(2, 1) = 1$.
   - For $n = 3$: $Q(3) = 10$, $P(3) = 18 + 15 + 2 = 35 \implies \gcd(35, 10) = 5$.

**Final Answer:** $\gcd(P(n), Q(n)) \in \{\mathbf{1, 5}\}$.

---

### Solution 13 (Hilbert Kernel & Quadratic Forms)
1. Recognize the integral identity for the coefficients:
   $$\frac{1}{i + j + 1} = \int_0^1 x^{i + j} dx = \int_0^1 x^i x^j dx$$
2. Substitute into the quadratic form:
   $$\sum_{1 \le i, j \le n} \frac{c_i c_j}{i + j + 1} = \sum_{i=1}^n \sum_{j=1}^n c_i c_j \int_0^1 x^i x^j dx = \int_0^1 \left(\sum_{i=1}^n c_i x^i\right) \left(\sum_{j=1}^n c_j x^j\right) dx$$
   $$= \int_0^1 \left(\sum_{i=1}^n c_i x^i\right)^2 dx$$
3. Let $Q(x) = \sum_{i=1}^n c_i x^i$. Since $c_i \in \mathbb{R}$, $[Q(x)]^2 \ge 0$ for all $x \in [0, 1]$.
   Since the integrand is non-negative and continuous:
   $$\int_0^1 [Q(x)]^2 dx \ge 0$$
4. Equality holds if and only if $Q(x) \equiv 0$ on $[0, 1]$. Since a non-zero polynomial has only finitely many roots, $Q(x) \equiv 0 \iff c_1 = c_2 = \dots = c_n = 0$. $\blacksquare$

---

### Solution 14 (Parity Invariants & Infinite Descent)
1. Let $S = \sum_{i=1}^8 a_i$. When $a_k$ is removed, the remaining 7 integers partition into two equal sums:
   $$S - a_k = 2 A_k \implies a_k \equiv S \pmod 2 \quad \text{for all } k \in \{1, \dots, 8\}$$
   All 8 integers must have the same parity.
2. Suppose all $a_i$ are odd:
   $S$ is the sum of 8 odd integers, so $S$ is even.
   Then $S - a_k = \text{even} - \text{odd} = \text{odd}$.
   However, $S - a_k = 2 A_k$ is even $\implies$ Contradiction!
3. Therefore, all $a_i$ must be even.
4. Let $a_i^{(1)} = a_i / 2$. The new set $\{a_1^{(1)}, \dots, a_8^{(1)}\}$ satisfies the identical partition property.
5. By the Method of Infinite Descent, each $a_i$ is divisible by $2^m$ for every $m \ge 1$.
   The only integer divisible by arbitrarily large powers of 2 is $0$.
   Hence $a_1 = a_2 = \dots = a_8 = 0$. $\blacksquare$

---

### Solution 15 ($p$-adic Valuations in Non-linear Recurrences)
Given $x^2 - 6x + 21 = 0$, $\alpha + \beta = 6$, $\alpha\beta = 21$, prime $p = 3$.
$v_3(6) = 1$, $v_3(21) = 1$, $v_3(2) = 0$.
Define $a_m = \alpha^{2^m} + \beta^{2^m}$.

1. **Part (1): $\alpha^2 + \beta^2$:**
   $$a_1 = (\alpha + \beta)^2 - 2\alpha\beta = 6^2 - 2(21) = 36 - 42 = -6$$
   $v_3(-6) = 1$. The largest power of 3 dividing $\alpha^2 + \beta^2$ is **$3^1$**.

2. **Part (2): $\alpha^4 + \beta^4$:**
   $$a_2 = a_1^2 - 2(\alpha\beta)^2 = (-6)^2 - 2(21)^2 = 36 - 2(441) = 36 - 882 = -846$$
   $v_3(-846) = 2$ (since $-846 = 9 \times (-94)$, and $3 \nmid -94$).
   The largest power of 3 dividing $\alpha^4 + \beta^4$ is **$3^2 = 9$**.

3. **Part (3): General $m \ge 1$:**
   **Induction Claim:** For all $m \ge 2$, $a_m = 3^{2^{m-1} + 1} k_m + 2(21)^{2^{m-1}}$.
   - Base case $m = 2$: $a_2 = -846 = 27(-32) + 2(21)^2 = -864 + 882 = 18 = -846$ (mod 27 holds).
   - Inductive step: $a_{m+1} = a_m^2 - 2(21)^{2^m}$.
     Squaring $a_m$ propagates terms divisible by $3^{2^m + 1}$, leaving the dominant term $2(21)^{2^m}$.
   - Since $v_3(21) = 1$ and $3 \nmid 2$, $v_3\left(2(21)^{2^{m-1}}\right) = 2^{m-1}$.
   - Since $2^{m-1} < 2^{m-1} + 1$, the valuation is strictly:
     $$v_3\left(\alpha^{2^m} + \beta^{2^m}\right) = 2^{m-1}$$

**Final Answer:** (1) **$3^1$**; (2) **$3^2$**; (3) **$3^{2^{m-1}}$**.

---

### Solution 16 (Root Localization & Rouché's Theorem)
Let $f(z) = z^7 - 7z^6 + 1$.
1. **Uniqueness in $(0, 1)$:**
   - $f(0) = 1 > 0$, $f(1) = 1 - 7 + 1 = -5 < 0$. By IVT, there is at least one root $x_0 \in (0, 1)$.
   - $f'(x) = 7x^6 - 42x^5 = 7x^5(x - 6)$. For $x \in (0, 1)$, $7x^5 > 0$ and $x - 6 < 0$, so $f'(x) < 0$.
   - $f$ is strictly decreasing on $(0, 1)$, so $x_0$ is unique.

2. **Bounding Complex Roots via Rouché's Theorem:**
   - Notice $f(6) = 6^7 - 7(6^6) + 1 = 6^6(6 - 7) + 1 = -6^6 + 1 < 0$, and $f(7) = 1 > 0$. There is a positive root $x_1 \in (6, 7)$.
   - For any real $R$ with $x_0 < R < 1$, $f(R) = R^7 - 7R^6 + 1 < 0 \implies R^7 + 1 < 7R^6$.
   - On the circle $|z| = R$:
     $$|z^7 + 1| \le |z|^7 + 1 = R^7 + 1 < 7R^6 = |-7z^6|$$
   - Let $P(z) = -7z^6$ and $Q(z) = z^7 + 1$. Since $|Q(z)| < |P(z)|$ on $|z| = R$, by Rouché's Theorem, $P(z) + Q(z) = z^7 - 7z^6 + 1$ has the same number of roots inside $|z| < R$ as $P(z) = -7z^6$, which is **6 roots**.
   - Since the polynomial has degree 7 and the 7th root is $x_1 > 6 > R$, all other 6 roots (including $x_0$ and the non-real roots) lie in $|z| < R$.
   - Taking $R \to x_0^+$ establishes $|z| \le x_0$ for every non-real complex root. $\blacksquare$

---

### Solution 17 (Matrix Commutators & Nilpotency)
1. **Proof of Nilpotency:**
   Given $[A, B^3] = B^2$. By induction, for all $k \ge 1$:
   $$[A, B^{3 \cdot 2^k}] = 2^k B^{3 \cdot 2^k - 1}$$
   Taking any matrix norm:
   $$2^k \|B^{3 \cdot 2^k - 1}\| = \|[A, B^{3 \cdot 2^k}]\| \le 2\|A\| \|B\| \|B^{3 \cdot 2^k - 1}\|$$
   If $B$ were not nilpotent, $\|B^{3 \cdot 2^k - 1}\| > 0$ for all $k$, implying $2^k \le 2\|A\|\|B\|$ for all $k \ge 1$, which is impossible as $2^k \to \infty$.  
   Thus $B$ is nilpotent.

2. **Counterexample:**
   For $B = \begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{pmatrix}$, $B^2 = \begin{pmatrix} 0 & 0 & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix} \ne 0$, but $B^3 = 0$.  
   Then for ANY matrix $A$:
   $$AB^3 - B^3 A = A(0) - (0)A = 0 \ne B^2$$
   Hence, no such matrix $A$ can exist. $\blacksquare$

---

### Solution 18 (Extremal Geometric Products & Maximum Modulus)
1. In the complex plane, let the vertices of the equilateral triangle be $1, \omega = e^{i 2\pi/3}, \omega^2 = e^{i 4\pi/3}$.
2. The distance product from point $P$ represented by $z \in \operatorname{int}(\triangle ABC)$ is:
   $$|PA||PB||PC| = |z - 1||z - \omega||z - \omega^2| = |z^3 - 1|$$
3. Define $F(z) = z^3 - 1$, which is holomorphic everywhere.
4. By the **Maximum Modulus Principle**, $|F(z)|$ on the compact closed triangle $K = \triangle ABC$ must achieve its maximum on the boundary $\partial K$:
   $$|F(z)| < \max_{w \in \partial K} |F(w)| \quad \forall z \in \operatorname{int}(K)$$
5. On the boundary edges, the distance to the origin $|w| \le 1$ with $|w| < 1$ except at the vertices $A, B, C$.
   - At the vertices: $|F(1)| = |1 - 1| = 0$.
   - On any edge, by the triangle inequality: $|F(w)| = |w^3 - 1| \le |w|^3 + 1$.
   - In fact, on the segment between $\omega$ and $\omega^2$, $w = -\frac{1}{2} + i y$ with $|y| \le \frac{\sqrt{3}}{2}$, so $\operatorname{Re}(w^3) > 0$, giving $|w^3 - 1| \le 1$.
   - Thus $\max_{w \in \partial K} |F(w)| = 1$.
6. Since $P$ is in the interior:
   $$|PA||PB||PC| < 1 \quad \blacksquare$$
