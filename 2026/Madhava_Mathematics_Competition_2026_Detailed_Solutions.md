# Madhava Mathematics Competition — 2026
## Detailed Solutions & Problem-Solving Guide

**Organized by:** Bhaskaracharya Pratishthana, Pune  
**Date of Examination:** 11/01/2026  
**Target Audience:** Undergraduate Students & Mathematics Olympiad / Competition Aspirants  
**Total Marks:** 100 | **Duration:** 3 hours  

---

### Structure of the Paper
* **Part I:** 10 Multiple-Choice Questions (2 marks each = 20 marks)
* **Part II:** 5 Short-Answer / Proof Questions (6 marks each = 30 marks)
* **Part III:** 4 In-Depth Proof & Analysis Questions (50 marks total)

---

# Part I (Questions 1 to 10)
*Each question carries 2 marks.*

---

### Question 1
Let $a < b < c$ be three positive integers in geometric progression whose common ratio is also an integer. If the arithmetic mean of $a, b, c$ is $b + 2$, then the value of $a$ is:
- **(A)** $24$
- **(B)** $12$
- **(C)** $6$
- **(D)** $4$

#### **Correct Answer:** **(C) 6**

#### **Detailed Solution:**
1. **Setting up variables:**  
   Let $r$ be the common ratio of the geometric progression. Since $a, b, c$ are integers and $a < b < c$, $r$ must be an integer strictly greater than $1$ ($r \ge 2$).
   We can express $b$ and $c$ in terms of $a$ and $r$:
   $$b = ar, \quad c = ar^2$$

2. **Using the Arithmetic Mean condition:**  
   The arithmetic mean of $a, b, c$ is given as $b + 2$:
   $$\frac{a + b + c}{3} = b + 2$$
   Substitute $b = ar$ and $c = ar^2$:
   $$\frac{a + ar + ar^2}{3} = ar + 2$$
   Multiply both sides by $3$:
   $$a + ar + ar^2 = 3ar + 6$$
   Rearrange all terms involving $a$ to the left-hand side:
   $$a(1 - 2r + r^2) = 6 \implies a(r - 1)^2 = 6$$

3. **Analyzing divisibility and integer constraints:**  
   Since $a$ and $r$ are positive integers, $(r - 1)^2$ must be a perfect square dividing $6$.  
   The divisors of $6$ are $1, 2, 3, 6$. The only perfect square among these is $1$.  
   Therefore:
   $$(r - 1)^2 = 1 \implies r - 1 = 1 \implies r = 2$$
   Substituting $(r - 1)^2 = 1$ back into $a(r - 1)^2 = 6$:
   $$a(1) = 6 \implies a = 6$$

4. **Verification:**  
   With $a = 6$ and $r = 2$:
   $$b = 12, \quad c = 24$$
   Arithmetic mean:
   $$\frac{6 + 12 + 24}{3} = \frac{42}{3} = 14$$
   Notice that $b + 2 = 12 + 2 = 14$, which matches perfectly.

> [!TIP]
> **Competition Strategy:** In Diophantine problems with geometric or arithmetic progressions, factorizing terms into forms like $A \cdot (\text{integer})^2 = K$ drastically restricts candidate values because few integers have square factors.

---

### Question 2
Triangles are formed by joining the vertices of a regular polygon of $12$ sides. The number of triangles having no side in common with the polygon is:
- **(A)** $124$
- **(B)** $220$
- **(C)** $96$
- **(D)** $112$

#### **Correct Answer:** **(D) 112**

#### **Detailed Solution:**

#### **Approach 1: Complementary Counting (Standard & Reliable)**
1. **Total Triangles:**  
   Any choice of 3 vertices from the 12 vertices of the 12-gon forms a triangle:
   $$\text{Total triangles} = \binom{12}{3} = \frac{12 \times 11 \times 10}{3 \times 2 \times 1} = 220$$

2. **Triangles sharing exactly 2 sides with the polygon:**  
   A triangle shares 2 sides with the polygon if and only if its 3 vertices are 3 consecutive vertices of the polygon ($v_i, v_{i+1}, v_{i+2}$).  
   Since there are 12 vertices, there are exactly $12$ such sets of consecutive triples:
   $$N_2 = 12$$

3. **Triangles sharing exactly 1 side with the polygon:**  
   - First, select one side of the 12-gon: there are $12$ choices ($e_1, e_2, \dots, e_{12}$).
   - Let the chosen side connect vertices $v_1$ and $v_2$. To ensure the triangle shares *only* this side and no other side, the third vertex $v_k$ cannot be:
     - $v_1$ or $v_2$ (the endpoints of the chosen side),
     - $v_{12}$ (adjacent to $v_1$, which would give a 2-side triangle),
     - $v_3$ (adjacent to $v_2$, which would give a 2-side triangle).
   - Hence, out of 12 vertices, $4$ vertices are forbidden. The remaining $12 - 4 = 8$ vertices can each be chosen as the third vertex.
   - Total triangles sharing exactly 1 side:
     $$N_1 = 12 \times 8 = 96$$

4. **Triangles sharing NO sides:**  
   $$\text{Result} = \text{Total} - N_1 - N_2 = 220 - 96 - 12 = 220 - 108 = 112$$

#### **Approach 2: Direct Closed-Form Formula**
For any $n$-sided regular polygon ($n \ge 6$), the number of triangles having no side in common with the polygon is given by:
$$T(n) = \frac{n(n - 4)(n - 5)}{6}$$
Plugging in $n = 12$:
$$T(12) = \frac{12 \times (12 - 4) \times (12 - 5)}{6} = \frac{12 \times 8 \times 7}{6} = 2 \times 56 = 112$$

> [!TIP]
> **Generalization to Remember:** For an $n$-gon:
> - Triangles with 2 sides common: $n$
> - Triangles with 1 side common: $n(n - 4)$
> - Triangles with 0 sides common: $\frac{n(n - 4)(n - 5)}{6}$

---

### Question 3
If 
$$f(x) = \begin{cases} ax + b & \text{if } x < -1 \\ x^2 + 1 & \text{if } -1 \le x < 1 \\ 3x - 1 & \text{if } x \ge 1 \end{cases}$$
is continuous everywhere, then which of the following values can $ab$ never take?
- **(A)** $-3$
- **(B)** $-1$
- **(C)** $0$
- **(D)** $3$

#### **Correct Answer:** **(A) -3**

#### **Detailed Solution:**
1. **Check continuity at $x = 1$:**  
   - Left-hand limit: $\lim_{x \to 1^-} f(x) = \lim_{x \to 1^-} (x^2 + 1) = 1^2 + 1 = 2$
   - Right-hand limit / value: $f(1) = 3(1) - 1 = 2$  
   Thus, $f$ is automatically continuous at $x = 1$ regardless of $a$ and $b$.

2. **Enforce continuity at $x = -1$:**  
   - Value / Right-hand limit: $f(-1) = (-1)^2 + 1 = 2$
   - Left-hand limit: $\lim_{x \to -1^-} f(x) = \lim_{x \to -1^-} (ax + b) = -a + b$  
   For continuity at $x = -1$, we require:
   $$-a + b = 2 \implies b = a + 2$$

3. **Examine the product $ab$:**  
   Substitute $b = a + 2$:
   $$ab = a(a + 2) = a^2 + 2a = (a + 1)^2 - 1$$
   Since $a \in \mathbb{R}$, $(a + 1)^2 \ge 0$.  
   Therefore:
   $$ab \ge -1$$
   The minimum possible value of $ab$ is $-1$ (attained when $a = -1, b = 1$).  
   Hence, $ab$ can **never** be less than $-1$. Among the choices, $-3 < -1$, so $ab$ can never take the value $-3$.

---

### Question 4
Let $f : [1, 3] \to \mathbb{R}$ be a continuous function. If $f$ takes rational values for all $x$ and $f(2) = 10$, then $f(1.5) =$
- **(A)** $7.5$
- **(B)** $10$
- **(C)** $1.5$
- **(D)** $5$

#### **Correct Answer:** **(B) 10**

#### **Detailed Solution:**
1. **Intermediate Value Theorem (IVT) / Connectedness:**  
   The domain $[1, 3]$ is a closed, connected interval in $\mathbb{R}$.  
   The continuous image of a connected set is connected. Therefore, the range $f([1, 3])$ must be a connected subset of $\mathbb{R}$.

2. **Connected Subsets of Rationals:**  
   The only connected subsets of $\mathbb{R}$ are single points and intervals.  
   However, any interval $[u, v]$ with $u < v$ contains infinitely many irrational numbers (since $\mathbb{R} \setminus \mathbb{Q}$ is dense in $\mathbb{R}$).  
   Since $f(x) \in \mathbb{Q}$ for all $x \in [1, 3]$, the range $f([1, 3])$ cannot contain any non-trivial interval.  
   Therefore, the range must be a single point (singleton):
   $$f([1, 3]) = \{c\} \quad \text{for some constant } c \in \mathbb{Q}$$

3. **Finding the value:**  
   Since $f(2) = 10$, we must have $c = 10$.  
   Hence $f(x) = 10$ for all $x \in [1, 3]$, which implies:
   $$f(1.5) = 10$$

> [!NOTE]
> **Key Topological Principle:** If $X$ is connected, $Y$ is equipped with the subspace topology having totally disconnected subsets (like $\mathbb{Q}$ in $\mathbb{R}$), then every continuous map $f: X \to Y$ is constant.

---

### Question 5
If $f(x) = (x + 1)^2 - 1, x \ge -1$, then the set $\{x : f(x) = f^{-1}(x)\}$ is:
- **(A)** $\phi$
- **(B)** $\{-1, 1\}$
- **(C)** $\{0, 1\}$
- **(D)** $\{-1, 0\}$

#### **Correct Answer:** **(D) \{-1, 0\}**

#### **Detailed Solution:**
1. **Monotonicity of $f$:**  
   For $x \ge -1$, $f'(x) = 2(x + 1) \ge 0$.  
   Since $f'(x) > 0$ for $x > -1$, $f$ is strictly increasing on $[-1, \infty)$.

2. **Key Property of Strictly Increasing Functions:**  
   If $f$ is strictly increasing, then the solutions to $f(x) = f^{-1}(x)$ are precisely the fixed points of $f$, i.e., solutions to $f(x) = x$.  
   *Proof:*  
   - If $f(x) > x$, then because $f$ is strictly increasing, applying $f$ yields $f(f(x)) > f(x) > x \implies f(f(x)) \ne x$, so $f^{-1}(x) \ne f(x)$.
   - If $f(x) < x$, applying $f$ yields $f(f(x)) < f(x) < x \implies f(f(x)) \ne x$.
   - Thus, $f(x) = f^{-1}(x) \iff f(x) = x$.

3. **Solving $f(x) = x$:**  
   $$(x + 1)^2 - 1 = x \implies x^2 + 2x + 1 - 1 = x \implies x^2 + x = 0$$
   $$x(x + 1) = 0 \implies x = 0 \quad \text{or} \quad x = -1$$
   Both $x = 0$ and $x = -1$ satisfy the domain condition $x \ge -1$.  
   Therefore, the solution set is $\{-1, 0\}$.

---

### Question 6
The number of real solutions of $1 + |e^x - 1| = e^x(e^x - 2)$ is:
- **(A)** $1$
- **(B)** $2$
- **(C)** $0$
- **(D)** $3$

#### **Correct Answer:** **(A) 1**

#### **Detailed Solution:**
Substitute $u = e^x$. Since $x \in \mathbb{R}$, we must have $u > 0$.  
The equation becomes:
$$1 + |u - 1| = u(u - 2) = u^2 - 2u$$

We partition into two cases based on the absolute value:

- **Case 1: $u \ge 1$ (i.e., $x \ge 0$):**  
  Here $|u - 1| = u - 1$. The equation becomes:
  $$1 + (u - 1) = u^2 - 2u \implies u = u^2 - 2u \implies u^2 - 3u = 0$$
  $$u(u - 3) = 0$$
  Since $u > 0$, we have $u = 3$.  
  Since $3 \ge 1$, this is a valid solution:
  $$e^x = 3 \implies x = \ln 3 > 0 \quad \text{(1 real solution)}$$

- **Case 2: $0 < u < 1$ (i.e., $x < 0$):**  
  Here $|u - 1| = -(u - 1) = 1 - u$. The equation becomes:
  $$1 + (1 - u) = u^2 - 2u \implies 2 - u = u^2 - 2u \implies u^2 - u - 2 = 0$$
  $$(u - 2)(u + 1) = 0 \implies u = 2 \quad \text{or} \quad u = -1$$
  Neither $2$ nor $-1$ lies in the interval $(0, 1)$. Thus, no solutions exist in this case.

Combining both cases, there is exactly **$1$ real solution** ($x = \ln 3$).

---

### Question 7
In how many ways can you choose an odd number of objects from $n$ objects?
- **(A)** $2^{n-1}$
- **(B)** $2^n$
- **(C)** $2^n - 1$
- **(D)** $n$

#### **Correct Answer:** **(A) $2^{n-1}$**

#### **Detailed Solution:**
We need to evaluate the sum:
$$S_{\text{odd}} = \binom{n}{1} + \binom{n}{3} + \binom{n}{5} + \dots$$
Recall the binomial expansions:
$$(1 + 1)^n = \binom{n}{0} + \binom{n}{1} + \binom{n}{2} + \dots + \binom{n}{n} = 2^n$$
$$(1 - 1)^n = \binom{n}{0} - \binom{n}{1} + \binom{n}{2} - \dots + (-1)^n \binom{n}{n} = 0 \quad (\text{for } n \ge 1)$$
Subtracting the second equation from the first:
$$(1 + 1)^n - (1 - 1)^n = 2 \left[ \binom{n}{1} + \binom{n}{3} + \binom{n}{5} + \dots \right] = 2^n - 0 = 2^n$$
Dividing by $2$:
$$S_{\text{odd}} = \frac{2^n}{2} = 2^{n-1}$$

> [!TIP]
> **Combinatorial Interpretation:** Choose any subset of the first $n-1$ elements in $2^{n-1}$ ways. The parity of this subset is either even or odd. The $n$-th element is uniquely forced (included if the subset is even, omitted if odd) to make the total number of chosen objects odd. Hence, there is a bijection with all subsets of $\{1, 2, \dots, n-1\}$, giving $2^{n-1}$.

---

### Question 8
The family of circles with center $(a, 0)$ and radius $a$ satisfies the differential equation:
- **(A)** $\frac{dy}{dx} + x^2 - y^2 = 0$
- **(B)** $2xy \frac{dy}{dx} + x^2 - y^2 = 0$
- **(C)** $2xy \frac{dy}{dx} + x - y = 0$
- **(D)** $2xy \frac{dy}{dx} + x^2 + y^2 = 0$

#### **Correct Answer:** **(B) $2xy \frac{dy}{dx} + x^2 - y^2 = 0$**

#### **Detailed Solution:**
1. **Equation of the family of circles:**  
   $$(x - a)^2 + (y - 0)^2 = a^2 \implies x^2 - 2ax + a^2 + y^2 = a^2$$
   $$x^2 + y^2 - 2ax = 0 \implies 2a = \frac{x^2 + y^2}{x}$$

2. **Differentiating implicitly with respect to $x$:**  
   Differentiating $x^2 + y^2 - 2ax = 0$:
   $$2x + 2y \frac{dy}{dx} - 2a = 0 \implies a = x + y \frac{dy}{dx}$$

3. **Eliminating the arbitrary parameter $a$:**  
   Substitute $a = x + y y'$ into $x^2 + y^2 - 2ax = 0$:
   $$x^2 + y^2 - 2x \left(x + y \frac{dy}{dx}\right) = 0$$
   $$x^2 + y^2 - 2x^2 - 2xy \frac{dy}{dx} = 0$$
   $$y^2 - x^2 - 2xy \frac{dy}{dx} = 0 \implies 2xy \frac{dy}{dx} + x^2 - y^2 = 0$$

---

### Question 9
The series 
$$\sum_{n=0}^\infty \frac{\cos(x^{2n}) + \sin(x^{2n+1}) - e^{-|x|n}}{1 + n^2}$$
- **(A)** converges pointwise everywhere on $\mathbb{R}$, but not uniformly
- **(B)** does not converge at any point
- **(C)** converges uniformly on $\mathbb{R}$
- **(D)** converges only at $0$

#### **Correct Answer:** **(C) converges uniformly on $\mathbb{R}$**

#### **Detailed Solution:**
Let $u_n(x)$ denote the general term of the series:
$$u_n(x) = \frac{\cos(x^{2n}) + \sin(x^{2n+1}) - e^{-|x|n}}{1 + n^2}$$
We bound the numerator for any $x \in \mathbb{R}$ using the triangle inequality:
- $|\cos(x^{2n})| \le 1$
- $|\sin(x^{2n+1})| \le 1$
- Since $|x| \ge 0$ and $n \ge 0$, $-|x|n \le 0$, which gives $0 < e^{-|x|n} \le 1$, so $|-e^{-|x|n}| \le 1$.

Hence:
$$|\cos(x^{2n}) + \sin(x^{2n+1}) - e^{-|x|n}| \le |\cos(x^{2n})| + |\sin(x^{2n+1})| + |e^{-|x|n}| \le 1 + 1 + 1 = 3$$
Consequently, for all $x \in \mathbb{R}$:
$$|u_n(x)| \le \frac{3}{1 + n^2} = M_n$$
Now examine the scalar numerical series $\sum_{n=0}^\infty M_n$:
$$\sum_{n=0}^\infty \frac{3}{1 + n^2} \le 3 + \sum_{n=1}^\infty \frac{3}{n^2} = 3 + 3 \left(\frac{\pi^2}{6}\right) < \infty$$
Since $\sum M_n$ converges, by the **Weierstrass M-Test**, the given series converges **uniformly on all of $\mathbb{R}$**.

---

### Question 10
If $1, a_1, a_2, \dots, a_{n-1}$ are the $n^{\text{th}}$ ($n \ge 2$) roots of unity, then 
$$\frac{1}{1 - a_1} + \frac{1}{1 - a_2} + \dots + \frac{1}{1 - a_{n-1}} =$$
- **(A)** $\frac{n}{2}$
- **(B)** $\frac{n-1}{2}$
- **(C)** $\frac{1}{2}$
- **(D)** $\frac{n(n-1)}{2}$

#### **Correct Answer:** **(B) $\frac{n-1}{2}$**

#### **Detailed Solution:**

#### **Approach 1: Logarithmic Differentiation of Polynomials**
1. The $n$ roots of unity satisfy $x^n - 1 = 0$. Since $1$ is a root:
   $$x^n - 1 = (x - 1)(x - a_1)(x - a_2)\cdots(x - a_{n-1})$$
2. Dividing both sides by $x - 1$, we define $P(x)$:
   $$P(x) = \frac{x^n - 1}{x - 1} = x^{n-1} + x^{n-2} + \dots + x + 1 = \prod_{k=1}^{n-1} (x - a_k)$$
3. Taking the natural logarithm and differentiating (or using the logarithmic derivative):
   $$\frac{P'(x)}{P(x)} = \sum_{k=1}^{n-1} \frac{1}{x - a_k}$$
4. Evaluating at $x = 1$:
   - $P(1) = 1^{n-1} + 1^{n-2} + \dots + 1 = n$
   - $P'(x) = (n-1)x^{n-2} + (n-2)x^{n-3} + \dots + 2x + 1$
   - $P'(1) = (n-1) + (n-2) + \dots + 1 = \frac{(n-1)n}{2}$
5. Substituting these values:
   $$\sum_{k=1}^{n-1} \frac{1}{1 - a_k} = \frac{P'(1)}{P(1)} = \frac{\frac{n(n-1)}{2}}{n} = \frac{n - 1}{2}$$

#### **Approach 2: Geometric & Complex Symmetry (Intuitive)**
For any root of unity $a_k = e^{i\theta_k} \ne 1$:
$$\frac{1}{1 - e^{i\theta_k}} = \frac{1}{1 - \cos\theta_k - i\sin\theta_k} = \frac{2\sin^2(\theta_k/2) + i\cdot 2\sin(\theta_k/2)\cos(\theta_k/2)}{4\sin^2(\theta_k/2)} = \frac{1}{2} + \frac{i}{2}\cot\left(\frac{\theta_k}{2}\right)$$
Notice that the **real part is constantly $\frac{1}{2}$** for every single root of unity!  
Since roots of unity come in conjugate pairs $e^{i\theta_k}$ and $e^{-i\theta_k}$, the imaginary terms $\frac{i}{2}\cot(\theta_k/2)$ cancel in pairs.  
There are $n - 1$ roots, so:
$$\sum_{k=1}^{n-1} \frac{1}{1 - a_k} = \sum_{k=1}^{n-1} \frac{1}{2} = \frac{n - 1}{2}$$

---

# Part II (Questions 1 to 5)
*Each question carries 6 marks.*

---

### Question 1
Let $f : [0, 1] \to \mathbb{R}$ be a continuous function with 
$$\int_0^1 x(x - 1)^2 f(x) dx = 0$$
Prove that there is a real number $c \in (0, 1)$ such that
$$\int_0^c x^2 f(x) dx = c \int_0^c x f(x) dx$$

#### **Detailed Solution:**

1. **Constructing the auxiliary function:**  
   Motivated by the expression $x(x - 1)^2 f(x)$, define a function $g: [0, 1] \to \mathbb{R}$ by:
   $$g(x) = \int_0^x t(t - x)^2 f(t) dt$$

2. **Checking boundary conditions for Rolle's Theorem:**  
   - At $x = 0$:
     $$g(0) = \int_0^0 t(t - 0)^2 f(t) dt = 0$$
   - At $x = 1$:
     $$g(1) = \int_0^1 t(t - 1)^2 f(t) dt = 0 \quad \text{(given in problem statement)}$$
   - Since $f$ is continuous, the integrand $t(t - x)^2 f(t)$ is continuous in both $t$ and $x$. Hence $g(x)$ is continuous on $[0, 1]$ and differentiable on $(0, 1)$.

3. **Differentiating $g(x)$:**  
   Expand the square inside the integral before differentiating:
   $$t(t - x)^2 = t(t^2 - 2tx + x^2) = t^3 - 2xt^2 + x^2 t$$
   Therefore:
   $$g(x) = \int_0^x t^3 f(t) dt - 2x \int_0^x t^2 f(t) dt + x^2 \int_0^x t f(t) dt$$
   Now differentiate with respect to $x$ using the Fundamental Theorem of Calculus and the product rule:
   $$g'(x) = x^3 f(x) - \left[2 \int_0^x t^2 f(t) dt + 2x \cdot x^2 f(x)\right] + \left[2x \int_0^x t f(t) dt + x^2 \cdot x f(x)\right]$$
   Notice how the boundary evaluation terms combine:
   $$x^3 f(x) - 2x^3 f(x) + x^3 f(x) = 0$$
   Thus, the terms involving $f(x)$ cancel completely! We are left with:
   $$g'(x) = 2x \int_0^x t f(t) dt - 2 \int_0^x t^2 f(t) dt$$

4. **Applying Rolle's Theorem:**  
   Since $g(0) = g(1) = 0$, by Rolle's Theorem there exists some $c \in (0, 1)$ such that:
   $$g'(c) = 0$$
   Substituting $x = c$ into $g'(x) = 0$:
   $$2c \int_0^c t f(t) dt - 2 \int_0^c t^2 f(t) dt = 0$$
   Dividing by $2$ and rearranging:
   $$\int_0^c t^2 f(t) dt = c \int_0^c t f(t) dt$$
   Replacing the dummy variable $t$ with $x$:
   $$\int_0^c x^2 f(x) dx = c \int_0^c x f(x) dx$$
   This completes the proof. $\blacksquare$

> [!TIP]
> **Reverse-Engineering Rolle's Functions:** When asked to show an identity at an unknown point $c \in (0, 1)$, rewrite the target equation as $H(c) = 0$. Then integrate $H(x)$ to hypothesize a candidate function $g(x)$ such that $g'(x) = H(x)$ and check if $g(0) = g(1) = 0$.

---

### Question 2
Let $f(x) = x^2 + 4x + 3$ and $g(x) = 2x + 5$. Show that $\gcd(f(n), g(n)) = 1$ or $3$ as $n$ varies over integers.

#### **Detailed Solution:**

1. **Eliminating the variable $n$ using the Euclidean Algorithm / Polynomial Division:**  
   Let $d = \gcd(f(n), g(n))$ for any $n \in \mathbb{Z}$. By definition:
   $$d \mid (n^2 + 4n + 3) \quad \text{and} \quad d \mid (2n + 5)$$
   If $d$ divides two quantities, it divides any integer linear combination of them.  
   To eliminate the quadratic term $n^2$, multiply $f(n)$ by $4$:
   $$4 f(n) = 4n^2 + 16n + 12$$
   Express this in terms of $g(n) = 2n + 5$:
   $$4n^2 + 16n + 12 = (2n + 5)(2n + 3) - 3$$
   Rearranging gives:
   $$(2n + 5)(2n + 3) - 4(n^2 + 4n + 3) = 3$$
   $$(2n + 3) g(n) - 4 f(n) = 3$$

2. **Deducing possible values of the GCD:**  
   Since $d \mid g(n)$ and $d \mid f(n)$, it follows that:
   $$d \mid \left[(2n + 3)g(n) - 4f(n)\right] \implies d \mid 3$$
   The positive divisors of $3$ are only $1$ and $3$.  
   Therefore, $\gcd(f(n), g(n))$ can only be $1$ or $3$.

3. **Demonstrating that both values are achievable:**  
   - For $n = 0$:  
     $$f(0) = 3, \quad g(0) = 5 \implies \gcd(3, 5) = 1$$
   - For $n = 2$:  
     $$f(2) = 2^2 + 4(2) + 3 = 15, \quad g(2) = 2(2) + 5 = 9 \implies \gcd(15, 9) = 3$$
   Hence, $\gcd(f(n), g(n)) \in \{1, 3\}$ for all $n \in \mathbb{Z}$. $\blacksquare$

---

### Question 3
Let $a_1, a_2, \dots, a_n$ be real numbers. Prove that
$$\sum_{1 \le i, j \le n} \frac{a_i a_j}{i + j - 1} \ge 0$$

#### **Detailed Solution:**

1. **Recognizing the integral kernel:**  
   Notice that for positive integers $i, j$:
   $$\frac{1}{i + j - 1} = \int_0^1 x^{i + j - 2} dx$$
   This is because $\int_0^1 x^m dx = \left[\frac{x^{m+1}}{m+1}\right]_0^1 = \frac{1}{m+1}$ with $m = i + j - 2$.

2. **Rewriting the double sum as an integral:**  
   Substitute this integral identity into the sum:
   $$\sum_{1 \le i, j \le n} \frac{a_i a_j}{i + j - 1} = \sum_{i=1}^n \sum_{j=1}^n a_i a_j \int_0^1 x^{i+j-2} dx$$
   Since the sum is finite, we can interchange summation and integration:
   $$= \int_0^1 \left(\sum_{i=1}^n \sum_{j=1}^n a_i a_j x^{(i-1) + (j-1)}\right) dx$$
   Notice that $x^{(i-1) + (j-1)} = x^{i-1} \cdot x^{j-1}$, so the double sum factors:
   $$= \int_0^1 \left(\sum_{i=1}^n a_i x^{i-1}\right) \left(\sum_{j=1}^n a_j x^{j-1}\right) dx = \int_0^1 \left(\sum_{i=1}^n a_i x^{i-1}\right)^2 dx$$

3. **Establishing non-negativity:**  
   Define the real polynomial $P(x) = \sum_{i=1}^n a_i x^{i-1}$.  
   Since the coefficients $a_i$ are real numbers, $(P(x))^2 \ge 0$ for all $x \in [0, 1]$.  
   The integral of a continuous, non-negative function is non-negative:
   $$\int_0^1 [P(x)]^2 dx \ge 0$$
   Therefore:
   $$\sum_{1 \le i, j \le n} \frac{a_i a_j}{i + j - 1} \ge 0$$
   Moreover, since $P(x)$ has degree at most $n-1$, $(P(x))^2 = 0$ identically on $[0, 1]$ if and only if all coefficients $a_1 = a_2 = \dots = a_n = 0$. Hence, the sum is strictly positive whenever not all $a_i$ are zero. $\blacksquare$

> [!NOTE]
> **Mathematical Connection:** The matrix $H \in \mathbb{R}^{n \times n}$ with entries $H_{ij} = \frac{1}{i + j - 1}$ is the celebrated **Hilbert Matrix**. This proof demonstrates that the Hilbert matrix is **positive semi-definite** (in fact, strictly positive definite).

---

### Question 4
Suppose for $n \ge 4$, $x_1, x_2, \dots, x_n$ are non-negative integers such that after removing any one of them the remaining numbers can be partitioned into two sets with equal sums.
1. If $n$ is even, then prove that $x_i = 0$, for all $i$.
2. Does the same conclusion hold when $n$ is odd? Justify your answer.

#### **Detailed Solution:**

#### **Part (i): Proof for even $n$**
1. **Total sum and parity relation:**  
   Let $S = \sum_{i=1}^n x_i$.  
   For any chosen index $k \in \{1, 2, \dots, n\}$, when $x_k$ is removed, the remaining $n - 1$ numbers partition into two subsets with equal sum, say each with sum $A_k$.  
   Then the sum of the remaining elements is:
   $$S - x_k = 2 A_k$$
   Because $A_k$ is an integer, $2 A_k$ is an even integer:
   $$S - x_k \equiv 0 \pmod 2 \implies x_k \equiv S \pmod 2 \quad \text{for all } k \in \{1, 2, \dots, n\}$$
   This implies that **all $x_1, x_2, \dots, x_n$ must have the same parity** (all even or all odd).

2. **Parity analysis when $n$ is even:**  
   Suppose for contradiction that all $x_i$ are odd.  
   - Since $n$ is even, the sum of an even number of odd integers is **even**:
     $$S = \sum_{i=1}^n x_i \equiv n \times 1 \equiv 0 \pmod 2 \implies S \text{ is even}$$
   - But if $S$ is even and $x_k$ is odd, then:
     $$S - x_k = \text{even} - \text{odd} = \text{odd}$$
   - This contradicts $S - x_k = 2 A_k$ being even!  
   Therefore, the numbers cannot be odd. Hence, **all $x_i$ must be even**.

3. **Method of Infinite Descent:**  
   Since every $x_i$ is even, write $x_i = 2 y_i$, where $y_i \in \mathbb{Z}_{\ge 0}$.  
   Dividing the partition equations by 2:
   $$\sum_{j \ne k} y_j = A_k$$
   where the sum of each partitioned subset is $A_k / 2 \in \mathbb{Z}_{\ge 0}$.  
   Thus, the new sequence $y_1, y_2, \dots, y_n$ satisfies the exact same condition as the original sequence!  
   By the same argument, every $y_i$ must be even, so each $x_i$ is divisible by $4$.  
   Inductively, each $x_i$ must be divisible by $2^m$ for every positive integer $m \in \mathbb{N}$:
   $$x_i \equiv 0 \pmod{2^m} \quad \forall m \ge 1$$
   Since the only non-negative integer divisible by arbitrarily large powers of 2 is $0$, we conclude:
   $$x_1 = x_2 = \dots = x_n = 0 \quad \blacksquare$$

#### **Part (ii): Analysis for odd $n$**
The conclusion **does NOT hold** when $n$ is odd.  
- **Counterexample:**  
  Let $n$ be any odd integer $\ge 5$ (e.g., $n = 5$ or $n = 7$), and set:
  $$x_1 = x_2 = \dots = x_n = 1$$
  Clearly, $x_i$ are non-negative integers and not all zero.  
- **Verification:**  
  Remove any one element $x_k = 1$. The remaining $n - 1$ elements are all equal to $1$.  
  Since $n$ is odd, $n - 1$ is even. We can divide the $n - 1$ ones into two equal sets of size $\frac{n - 1}{2}$, each having sum:
  $$\frac{n - 1}{2}$$
  Thus the condition is fully satisfied, yet $x_i = 1 \ne 0$.

---

### Question 5
Give an example of a function $f : \mathbb{R} \to \mathbb{R}$, if it exists, which is continuous at $a$ if and only if $a$ is a positive integer. Justify your answer.

#### **Detailed Solution:**

#### **1. Construction:**
Define $f: \mathbb{R} \to \mathbb{R}$ by:
$$f(x) = \begin{cases} h(x) & \text{if } x \in \mathbb{Q} \\ 0 & \text{if } x \in \mathbb{R} \setminus \mathbb{Q} \end{cases}$$
where $h: \mathbb{R} \to \mathbb{R}$ is the continuous function defined piecewise as:
$$h(x) = \begin{cases} 1 & \text{if } x \le \frac{1}{2} \\ \sin(\pi x) & \text{if } x > \frac{1}{2} \end{cases}$$

#### **2. Properties of the auxiliary function $h(x)$:**
- **Continuity of $h$:**  
  At the boundary $x = 1/2$:
  $$\lim_{x \to (1/2)^-} h(x) = 1, \quad \lim_{x \to (1/2)^+} h(x) = \sin\left(\frac{\pi}{2}\right) = 1, \quad h(1/2) = 1$$
  So $h(x)$ is continuous everywhere on $\mathbb{R}$.
- **Zeros of $h(x)$:**  
  - For $x \le 1/2$, $h(x) = 1 \ne 0$.
  - For $x > 1/2$, $h(x) = \sin(\pi x) = 0 \iff \pi x = k\pi \iff x = k \in \mathbb{Z}$.  
    Since $x > 1/2$, the integer values are $k \in \{1, 2, 3, \dots\} = \mathbb{Z}^+$.  
  Therefore:
  $$h(x) = 0 \iff x \in \mathbb{Z}^+$$

#### **3. Justification of Continuity:**
- **Case 1: Let $a \in \mathbb{Z}^+$ (Positive Integer):**  
  Then $h(a) = 0$, so $f(a) = 0$.  
  For any sequence $x_n \to a$:
  $$|f(x_n) - f(a)| = |f(x_n)| \le |h(x_n)|$$
  Since $h$ is continuous, $\lim_{n \to \infty} h(x_n) = h(a) = 0$.  
  By the Squeeze Theorem:
  $$\lim_{n \to \infty} f(x_n) = 0 = f(a)$$
  Hence, $f$ is continuous at every $a \in \mathbb{Z}^+$.

- **Case 2: Let $a \notin \mathbb{Z}^+$:**  
  Then $h(a) \ne 0$.  
  By the density of $\mathbb{Q}$ and $\mathbb{R} \setminus \mathbb{Q}$ in $\mathbb{R}$:
  1. There exists a sequence of rationals $q_n \to a$, along which:
     $$\lim_{n \to \infty} f(q_n) = \lim_{n \to \infty} h(q_n) = h(a) \ne 0$$
  2. There exists a sequence of irrationals $r_n \to a$, along which:
     $$\lim_{n \to \infty} f(r_n) = \lim_{n \to \infty} 0 = 0$$
  Since $h(a) \ne 0$, the limits along the two sequences do not agree. Thus, $\lim_{x \to a} f(x)$ does not exist.  
  Hence, $f$ is discontinuous at every $a \notin \mathbb{Z}^+$.

**Conclusion:** $f$ is continuous at $a$ if and only if $a$ is a positive integer. $\blacksquare$

---

# Part III (Questions 1 to 4)
*Total marks: 50.*

---

### Question 1
Suppose $\alpha, \beta$ are roots of the polynomial $x^2 + bx + c$. Let $p > 2$ be a prime satisfying the conditions: $p$ divides $b$, $p$ divides $c$, but $p^2$ does not divide $c$.
1. Find the largest power of $p$ which divides $\alpha^4 + \beta^4$. **[2 marks]**
2. Find the largest power of $p$ which divides $\alpha^8 + \beta^8$. **[3 marks]**
3. For any positive integer $n$, find the largest power of $p$ which divides $\alpha^{2^n} + \beta^{2^n}$. **[8 marks]**

#### **Detailed Solution:**

Let $v_p(x)$ denote the $p$-adic valuation of an integer $x$ (the highest power $k$ such that $p^k \mid x$).  
Given:
- $p \mid b \implies v_p(b) \ge 1$
- $p \mid c \text{ and } p^2 \nmid c \implies v_p(c) = 1$
- $p > 2$ is an odd prime, so $p \nmid 2 \implies v_p(2) = 0$.

Define the sequence:
$$a_n = \alpha^{2^n} + \beta^{2^n} \quad \text{for } n \ge 1$$
Note that by Vieta's formulas:
$$\alpha + \beta = -b, \quad \alpha\beta = c$$
For the base case $n = 1$:
$$a_1 = \alpha^2 + \beta^2 = (\alpha + \beta)^2 - 2\alpha\beta = b^2 - 2c$$
Since $v_p(b) \ge 1$, we have $v_p(b^2) \ge 2$.  
Meanwhile, $v_p(2c) = v_p(2) + v_p(c) = 0 + 1 = 1$.  
Since the valuations of the two terms are distinct ($2 \ne 1$), by properties of valuations:
$$v_p(a_1) = \min(v_p(b^2), v_p(2c)) = 1$$
So $p^1 \mid a_1$ and $p^2 \nmid a_1$.

---

#### **Subquestion (i): Largest power dividing $\alpha^4 + \beta^4$**
$$a_2 = \alpha^4 + \beta^4 = (\alpha^2 + \beta^2)^2 - 2(\alpha\beta)^2 = a_1^2 - 2c^2$$
Substitute $a_1 = b^2 - 2c$:
$$a_2 = (b^2 - 2c)^2 - 2c^2 = b^4 - 4b^2 c + 4c^2 - 2c^2 = b^4 - 4b^2 c + 2c^2$$
Let's check the divisibility by powers of $p$:
- $v_p(b^4) \ge 4$
- $v_p(4b^2 c) \ge 2(1) + 1 = 3$
- $v_p(2c^2) = v_p(2) + 2v_p(c) = 0 + 2 = 2$

Notice that $p^3$ divides $b^4 - 4b^2 c$. Thus:
$$a_2 \equiv 2c^2 \pmod{p^3}$$
Since $v_p(2c^2) = 2$, $p^2$ divides $a_2$, but $p^3$ does not divide $a_2$.  
Therefore, the largest power of $p$ dividing $\alpha^4 + \beta^4$ is **$p^2$**.

---

#### **Subquestion (ii): Largest power dividing $\alpha^8 + \beta^8$**
$$a_3 = \alpha^8 + \beta^8 = a_2^2 - 2(\alpha\beta)^4 = a_2^2 - 2c^4$$
From (i), we know $a_2 = p^3 k + 2c^2$ for some integer $k$.  
Squaring $a_2$:
$$a_2^2 = (p^3 k + 2c^2)^2 = p^6 k^2 + 4 p^3 k c^2 + 4 c^4$$
Subtracting $2c^4$:
$$a_3 = a_2^2 - 2c^4 = p^6 k^2 + 4 p^3 k c^2 + 2c^4$$
Now analyze the powers of $p$:
- $p^5 \mid p^6 k^2$
- Since $v_p(c^2) = 2$, $v_p(4 p^3 k c^2) \ge 3 + 2 = 5$, so $p^5 \mid 4 p^3 k c^2$
- $v_p(2c^4) = v_p(2) + 4 v_p(c) = 0 + 4 = 4$

Thus:
$$a_3 \equiv 2c^4 \pmod{p^5}$$
Because $v_p(2c^4) = 4$, $p^4$ divides $a_3$, but $p^5$ does not divide $a_3$.  
Therefore, the largest power of $p$ dividing $\alpha^8 + \beta^8$ is **$p^4$**.

---

#### **Subquestion (iii): Largest power dividing $\alpha^{2^n} + \beta^{2^n}$ for general $n$**

**Claim:** For all integers $n \ge 2$, there exists an integer $k_n$ such that:
$$a_n = p^{2^{n-1} + 1} k_n + 2 c^{2^{n-1}}$$

**Proof by Mathematical Induction:**
1. **Base Case ($n = 2$):**  
   From subquestion (i):
   $$a_2 = b^4 - 4b^2 c + 2c^2$$
   Since $p^3 \mid (b^4 - 4b^2 c)$, we can write $a_2 = p^3 k_2 + 2c^2 = p^{2^{2-1} + 1} k_2 + 2c^{2^{2-1}}$.  
   The base case holds.

2. **Inductive Hypothesis:**  
   Assume the claim holds for some $n \ge 2$, i.e.:
   $$a_n = p^{2^{n-1} + 1} k_n + 2 c^{2^{n-1}}$$

3. **Inductive Step:**  
   Consider $a_{n+1}$:
   $$a_{n+1} = a_n^2 - 2(\alpha\beta)^{2^n} = a_n^2 - 2 c^{2^n}$$
   Substitute the expression for $a_n$:
   $$a_{n+1} = \left(p^{2^{n-1} + 1} k_n + 2 c^{2^{n-1}}\right)^2 - 2 c^{2^n}$$
   $$= p^{2(2^{n-1} + 1)} k_n^2 + 4 p^{2^{n-1} + 1} k_n c^{2^{n-1}} + 4 c^{2^n} - 2 c^{2^n}$$
   $$= p^{2^n + 2} k_n^2 + 4 p^{2^{n-1} + 1} k_n c^{2^{n-1}} + 2 c^{2^n}$$
   Now inspect the powers of $p$ in the first two terms:
   - First term power: $2^n + 2 \ge 2^n + 1$.
   - Second term: since $v_p(c) = 1$, $c^{2^{n-1}}$ contributes $p^{2^{n-1}}$.  
     The total power of $p$ dividing the second term is:
     $$(2^{n-1} + 1) + 2^{n-1} = 2^n + 1$$
   Thus, both of the first two terms are divisible by $p^{2^n + 1}$. Factoring out $p^{2^n + 1}$:
   $$a_{n+1} = p^{2^n + 1} k_{n+1} + 2 c^{2^n}$$
   This matches the required form for $n + 1$.  
   By induction, the claim holds for all $n \ge 2$.

**Determining the exact valuation:**  
From the claim:
$$a_n \equiv 2 c^{2^{n-1}} \pmod{p^{2^{n-1} + 1}}$$
Since $p > 2$ and $v_p(c) = 1$:
$$v_p\left(2 c^{2^{n-1}}\right) = 2^{n-1}$$
Since $2^{n-1} < 2^{n-1} + 1$, the valuation of $a_n$ is strictly determined by the lower order term:
$$v_p(a_n) = 2^{n-1}$$
Notice this also holds for $n = 1$, where $v_p(a_1) = 2^0 = 1$.  

**Final Answer:** For any positive integer $n$, the largest power of $p$ dividing $\alpha^{2^n} + \beta^{2^n}$ is **$p^{2^{n-1}}$**.

---

### Question 2
1. Show that $x^6 - 6x^5 + 1 = 0$ has a unique root in the interval $(0, 1)$. **[3 marks]**
2. Show that every complex (non-real) root $z$ of $x^6 - 6x^5 + 1 = 0$ satisfies $|z| \le x_0$, where $x_0$ is the root of this equation in $(0, 1)$. **[10 marks]**

#### **Detailed Solution:**

#### **Subquestion (i): Existence and uniqueness in $(0, 1)$**
Let $f(x) = x^6 - 6x^5 + 1$.
1. **Existence (Intermediate Value Theorem):**  
   - $f(0) = 0 - 0 + 1 = 1 > 0$
   - $f(1) = 1^6 - 6(1^5) + 1 = -4 < 0$  
   Since $f(x)$ is a polynomial, it is continuous on $[0, 1]$. By the Intermediate Value Theorem, there exists at least one root $x_0 \in (0, 1)$ such that $f(x_0) = 0$.

2. **Uniqueness (Monotonicity / First Derivative Test):**  
   Differentiating $f(x)$:
   $$f'(x) = 6x^5 - 30x^4 = 6x^4(x - 5)$$
   For any $x \in (0, 1)$:
   - $6x^4 > 0$
   - $x - 5 < 0$  
   Thus, $f'(x) < 0$ for all $x \in (0, 1)$.  
   Since $f(x)$ is strictly decreasing on $(0, 1)$, it can cross the $x$-axis at most once.  
   Therefore, $x_0$ is the **unique** root in $(0, 1)$.

*(Alternative Uniqueness via Descartes' Rule of Signs: The coefficients of $f(x) = x^6 - 6x^5 + 1$ have signs $+ , - , +$, showing $2$ sign variations. Hence $f$ has at most $2$ positive real roots. Since $f(0) > 0, f(1) < 0, f(6) = 1 > 0$, one root is in $(0, 1)$ and one is in $(1, 6)$. Thus, at most and exactly one root lies in $(0, 1)$).*

---

#### **Subquestion (ii): Proving $|z| \le x_0$ for every complex root**

Here we present two complete, rigorous proofs: the classical Complex Trigonometric method and the elegant Rouché's Theorem method.

#### **Approach 1: Complex Trigonometric / Polar Form (Official Scheme Method)**
Let $z = r e^{i\theta} = r(\cos\theta + i\sin\theta)$ be a non-real root of $f(z) = 0$, so $r > 0$ and $\theta \in (-\pi, \pi)$ with $\theta \ne 0$.  
Substituting $z$ into $z^6 - 6z^5 + 1 = 0$:
$$r^6 e^{i 6\theta} - 6 r^5 e^{i 5\theta} + 1 = 0$$
Separating real and imaginary parts:
$$\begin{aligned}
r^6 \cos(6\theta) - 6r^5 \cos(5\theta) &= -1 \quad &(1) \\
r^6 \sin(6\theta) - 6r^5 \sin(5\theta) &= 0 \quad &(2)
\end{aligned}$$

From $(2)$, since $r > 0$:
$$r \sin(6\theta) = 6 \sin(5\theta) \implies r = \frac{6 \sin(5\theta)}{\sin(6\theta)}$$
Now rewrite $(1)$ using this relation:
$$r^5 \left[ r \cos(6\theta) - 6 \cos(5\theta) \right] = -1$$
Substitute $r = \frac{6\sin(5\theta)}{\sin(6\theta)}$ inside the brackets:
$$r^5 \left[ \frac{6\sin(5\theta)\cos(6\theta) - 6\cos(5\theta)\sin(6\theta)}{\sin(6\theta)} \right] = -1$$
Using the angle subtraction identity $\sin(A - B) = \sin A \cos B - \cos A \sin B$:
$$r^5 \left[ \frac{-6\sin(6\theta - 5\theta)}{\sin(6\theta)} \right] = -1 \implies r^5 \left[ \frac{-6\sin\theta}{\sin(6\theta)} \right] = -1$$
Hence:
$$r^5 = \frac{\sin(6\theta)}{6\sin\theta} \quad \text{and} \quad r^6 = r \cdot r^5 = \frac{\sin(5\theta)}{\sin\theta} \quad (*)$$

Since $|\sin(5\theta)| \le 5|\sin\theta|$ for all $\theta$, we have $r^6 < 5$, so $r < 5^{1/6} < 5$.  
Recall that for the real polynomial, $f(x) > 0$ on $[0, x_0)$ and $f(x) < 0$ on $(x_0, 5]$ (since $f(0) = 1 > 0$, $f(x_0) = 0$, and $f'(x) < 0$ on $(0, 5)$).  
Therefore, if we can show that $f(r) > 0$, then because $r < 5$, $r$ must lie in the interval $[0, x_0)$, proving $r < x_0$!

Let's evaluate $f(r)$:
$$f(r) = r^6 - 6r^5 + 1 = \frac{\sin(5\theta)}{\sin\theta} - \frac{\sin(6\theta)}{\sin\theta} + 1 = \frac{\sin(5\theta) - \sin(6\theta) + \sin\theta}{\sin\theta}$$
Using trigonometric sum-to-product identities:
$$\sin(5\theta) + \sin\theta = 2\sin(3\theta)\cos(2\theta)$$
Rewriting the numerator gives:
$$f(r) = \frac{\cos(\theta/2) - \cos(11\theta/2)}{\cos(\theta/2)}$$
Since $\theta \in (-\pi, \pi)$, $\frac{\theta}{2} \in (-\pi/2, \pi/2)$, so $\cos(\theta/2) > 0$.  
- If $\cos(11\theta/2) \le 0$, then the numerator is positive, so $f(r) \ge 1 > 0$.
- If $\cos(11\theta/2) > 0$, we look at the product:
  $$\left(\cos\frac{\theta}{2} + \cos\frac{11\theta}{2}\right)\left(\cos\frac{\theta}{2} - \cos\frac{11\theta}{2}\right) = \frac{\cos\theta - \cos(11\theta)}{2} = \sin(5\theta)\sin(6\theta)$$
  From $(*)$, $r^5 = \frac{\sin(6\theta)}{6\sin\theta}$ and $r^6 = \frac{\sin(5\theta)}{\sin\theta}$, so $\sin(5\theta)\sin(6\theta) = 6 r^{11} \sin^2\theta > 0$.  
  Since the first factor $\left(\cos\frac{\theta}{2} + \cos\frac{11\theta}{2}\right) > 0$, the second factor must also be positive:
  $$\cos\frac{\theta}{2} - \cos\frac{11\theta}{2} > 0$$
Thus, in all cases, $f(r) > 0$.  
Since $r < 5$ and $f(r) > 0$, we conclude that $r < x_0$, which establishes:
$$|z| \le x_0 \quad \blacksquare$$

---

#### **Approach 2: Complex Analysis via Rouché's Theorem (Quick & Insightful)**
Let $x_1 \in (1, 6)$ be the other positive real root of $f$.  
For any real number $R$ satisfying $x_0 < R < 1$:
$$f(R) = R^6 - 6R^5 + 1 < 0 \implies R^6 + 1 < 6R^5$$
Consider the contour circle $C_R = \{z \in \mathbb{C} : |z| = R\}$.  
Define:
$$P(z) = -6z^5 \quad \text{and} \quad Q(z) = z^6 + 1$$
On the circle $C_R$:
$$|Q(z)| = |z^6 + 1| \le |z|^6 + 1 = R^6 + 1$$
$$|P(z)| = |-6z^5| = 6|z|^5 = 6R^5$$
Since $R^6 + 1 < 6R^5$, we have:
$$|Q(z)| < |P(z)| \quad \text{for all } z \in C_R$$
By **Rouché's Theorem**, the polynomials $P(z)$ and $P(z) + Q(z) = z^6 - 6z^5 + 1$ have the exact same number of roots inside the open disk $|z| < R$.  
The polynomial $P(z) = -6z^5$ has a root of multiplicity $5$ at the origin, so it has exactly **$5$ roots** inside $|z| < R$.  
Therefore, $z^6 - 6z^5 + 1 = 0$ has exactly $5$ roots inside $|z| < R$.

Since the total degree of the polynomial is 6, and the 6th root is the real root $x_1 > 1 > R$, all of the remaining 5 roots (which include $x_0$ and the 4 non-real complex roots) lie inside $|z| < R$ for *every* $R > x_0$.  
Taking the infimum as $R \to x_0^+$:
$$|z| \le x_0$$
for every complex root $z$. $\blacksquare$

---

### Question 3
1. Suppose $A, B$ are $n \times n$ complex matrices with $AB^2 - B^2 A = B$. Show that $B$ is a nilpotent matrix. **[9 marks]**
2. Let $B$ be an $n \times n$ complex nilpotent matrix. Does there exist an $n \times n$ matrix $A$ such that $AB^2 - B^2 A = B$? Justify your answer. **[3 marks]**

#### **Detailed Solution:**

#### **Subquestion (i): Proving $B$ is nilpotent**

1. **Deriving a recurrence for powers of $B$:**  
   We are given the commutator relation:
   $$[A, B^2] = AB^2 - B^2 A = B$$
   **Claim:** For all integers $k \ge 1$:
   $$A B^{2^k} - B^{2^k} A = 2^{k-1} B^{2^k - 1}$$
   
2. **Proof of Claim by Mathematical Induction:**  
   - **Base Case ($k = 1$):**  
     $$AB^{2^1} - B^{2^1} A = AB^2 - B^2 A = 2^0 B^{2^1 - 1} = B$$
     This matches the given condition.
   
   - **Inductive Step:**  
     Assume the claim holds for $k \ge 1$:
     $$A B^{2^k} - B^{2^k} A = 2^{k-1} B^{2^k - 1}$$
     Multiply this identity from the right by $B^{2^k}$:
     $$A B^{2^k} B^{2^k} - B^{2^k} A B^{2^k} = 2^{k-1} B^{2^k - 1} B^{2^k}$$
     $$A B^{2^{k+1}} - B^{2^k} (A B^{2^k}) = 2^{k-1} B^{2^{k+1} - 1}$$
     From the induction hypothesis, rewrite $A B^{2^k} = 2^{k-1} B^{2^k - 1} + B^{2^k} A$. Substituting this in:
     $$A B^{2^{k+1}} - B^{2^k} \left(2^{k-1} B^{2^k - 1} + B^{2^k} A\right) = 2^{k-1} B^{2^{k+1} - 1}$$
     $$A B^{2^{k+1}} - 2^{k-1} B^{2^{k+1} - 1} - B^{2^{k+1}} A = 2^{k-1} B^{2^{k+1} - 1}$$
     Moving the middle term to the right:
     $$A B^{2^{k+1}} - B^{2^{k+1}} A = 2 \cdot 2^{k-1} B^{2^{k+1} - 1} = 2^k B^{2^{k+1} - 1}$$
     The claim is established for all $k \ge 1$.

3. **Norm bounding and contradiction:**  
   Choose any submultiplicative matrix norm $\|\cdot\|$ on $M_n(\mathbb{C})$.  
   Taking norms on both sides of the identity:
   $$2^{k-1} \|B^{2^k - 1}\| = \|A B^{2^k} - B^{2^k} A\| \le \|A B^{2^k}\| + \|B^{2^k} A\| \le 2 \|A\| \|B^{2^k}\|$$
   Using submultiplicativity $\|B^{2^k}\| = \|B \cdot B^{2^k - 1}\| \le \|B\| \|B^{2^k - 1}\|$:
   $$2^{k-1} \|B^{2^k - 1}\| \le 2 \|A\| \|B\| \|B^{2^k - 1}\|$$
   Now suppose for contradiction that $B$ is **not nilpotent**.  
   Then $B^m \ne 0$ for all integers $m \ge 1$, which implies $\|B^{2^k - 1}\| > 0$.  
   Dividing both sides by $\|B^{2^k - 1}\|$:
   $$2^{k-1} \le 2 \|A\| \|B\| \quad \text{for all } k \ge 1$$
   However, as $k \to \infty$, $2^{k-1} \to \infty$, while $2\|A\|\|B\|$ is a fixed finite constant!  
   This contradiction shows that there must exist some $m$ for which $B^m = 0$.  
   Hence, $B$ is a **nilpotent matrix**. $\blacksquare$

> [!TIP]
> **Operator Theory Connection (Kleinecke-Shirokov Theorem):**  
> Consider the derivation $\mathcal{D}_C(X) = CX - XC$ with $C = B^2$. Then $\mathcal{D}_C(A) = -B$. Since $[B, C] = [B, B^2] = 0$, we have $\mathcal{D}_C^2(A) = 0$. By the celebrated **Jacobson's Lemma / Kleinecke-Shirokov Theorem**, any commutator $[A, C]$ that commutes with $C$ is necessarily nilpotent.

---

#### **Subquestion (ii): Does such an $A$ exist for ANY nilpotent $B$?**
**Answer:** **NO.**

#### **Counterexample:**
Consider $n = 2$ and the standard nilpotent Jordan block:
$$B = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}$$
Notice that:
$$B^2 = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = 0$$
Since $B^2 = 0$, for **any** $2 \times 2$ matrix $A$, we have:
$$AB^2 - B^2 A = A(0) - (0)A = 0$$
However, $B = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix} \ne 0$.  
Therefore:
$$AB^2 - B^2 A = 0 \ne B$$
Thus, no such matrix $A$ can exist.

*(General Remark: Whenever $B^2 = 0$, the expression $AB^2 - B^2 A$ vanishes identically, so any non-zero nilpotent matrix satisfying $B^2 = 0$ serves as an immediate counterexample).*

---

### Question 4
Let $A, B, C, D$ be vertices of a quadrilateral inscribed in the unit circle. Let $P$ be a point in the interior of the quadrilateral $ABCD$. Show that
$$|PA||PB||PC||PD| < \frac{27}{16}$$
where $|PX|$ is the length of the line segment $PX$.

#### **Detailed Solution:**

1. **Formulation in the Complex Plane:**  
   Identify the plane with $\mathbb{C}$. Let the unit circle be $\Gamma = \{z \in \mathbb{C} : |z| = 1\}$.  
   The vertices $A, B, C, D$ correspond to complex numbers $a, b, c, d$ with $|a| = |b| = |c| = |d| = 1$.  
   The quadrilateral region $K$ is the convex hull of $\{a, b, c, d\}$.  
   Define the complex polynomial:
   $$F(z) = (z - a)(z - b)(z - c)(z - d)$$
   For any point $P$ corresponding to $z \in \mathbb{C}$:
   $$\phi(z) = |F(z)| = |z - a||z - b||z - c||z - d| = |PA||PB||PC||PD|$$

2. **Maximum Modulus Principle:**  
   The function $F(z)$ is holomorphic (analytic) on $\mathbb{C}$.  
   By the **Maximum Modulus Principle**, the continuous real-valued function $|F(z)|$ on the compact domain $K$ cannot achieve its maximum at an interior point unless $F(z)$ is constant (which it is not).  
   Therefore, for every interior point $P \in \text{int}(K)$:
   $$\phi(P) < \max_{Q \in \partial K} \phi(Q)$$
   where $\partial K$ is the boundary of the quadrilateral (the four line segments $AB, BC, CD, DA$).

3. **Bounding the product on the boundary segments:**  
   Without loss of generality, suppose $Q \in \partial K$ lies on the edge $BC$.  
   Let $x = |OQ|$ be the distance from $Q$ to the origin $O$ (the center of the unit circle). Since $Q$ lies strictly inside or on the unit circle, $0 \le x \le 1$.

   - **Bounding $|QB||QC|$ via Intersecting Chords:**  
     $B, Q, C$ are collinear. Extend the line segment $BC$ to meet the unit circle at points $X$ and $Y$, forming a chord $XY$ passing through $Q$.  
     By the Intersecting Chords Theorem (Power of a Point):
     $$|QX||QY| = 1 - |OQ|^2 = 1 - x^2 = (1 - x)(1 + x)$$
     Since $B$ and $C$ lie on this chord, the distance product $|QB||QC|$ cannot exceed the full chord product $|QX||QY|$:
     $$|QB||QC| \le |QX||QY| = 1 - x^2$$

   - **Bounding $|QA|$ and $|QD|$ via the Triangle Inequality:**  
     For vertex $A$, applying the triangle inequality in $\triangle OAQ$:
     $$|QA| \le |OA| + |OQ| = 1 + x$$
     Similarly for vertex $D$:
     $$|QD| \le |OD| + |OQ| = 1 + x$$

4. **Combining the bounds:**  
   Multiplying these inequalities gives an upper bound on $\phi(Q)$ on the boundary:
   $$\phi(Q) = |QA||QB||QC||QD| \le (1 - x^2)(1 + x)(1 + x) = (1 - x)(1 + x)^3$$

5. **Maximizing $g(x) = (1 - x)(1 + x)^3$ on $[0, 1]$:**  
   Let $g(x) = (1 - x)(1 + x)^3$ for $x \in [0, 1]$.  
   Differentiating with respect to $x$:
   $$g'(x) = -1 \cdot (1 + x)^3 + (1 - x) \cdot 3(1 + x)^2 = (1 + x)^2 \left[ -(1 + x) + 3(1 - x) \right]$$
   $$g'(x) = (1 + x)^2 (2 - 4x)$$
   Setting $g'(x) = 0$ in $(0, 1)$:
   $$2 - 4x = 0 \implies x = \frac{1}{2}$$
   - For $x \in [0, 1/2)$, $g'(x) > 0$ (increasing).
   - For $x \in (1/2, 1]$, $g'(x) < 0$ (decreasing).  
   Thus, $g(x)$ achieves its unique maximum at $x = \frac{1}{2}$:
   $$g\left(\frac{1}{2}\right) = \left(1 - \frac{1}{2}\right)\left(1 + \frac{1}{2}\right)^3 = \frac{1}{2} \cdot \left(\frac{3}{2}\right)^3 = \frac{1}{2} \cdot \frac{27}{8} = \frac{27}{16}$$

6. **Conclusion:**  
   On the boundary $\partial K$, $\phi(Q) \le \frac{27}{16}$.  
   By the Maximum Modulus Principle, since $P$ is an interior point:
   $$|PA||PB||PC||PD| < \frac{27}{16} \quad \blacksquare$$

---

## Competition Tips & Problem-Solving Strategies Summary

| Topic / Field | Key Strategy Illustrated in this Paper |
| :--- | :--- |
| **Number Theory & Progressions** | When terms of a progression satisfy arithmetic mean conditions, factor into $a(r-1)^2 = K$ to exploit limited square divisors. |
| **Combinatorics on Polygons** | Use complementary counting: $\binom{n}{3} - (\text{triangles with 2 edges}) - (\text{triangles with 1 edge})$. |
| **Real Analysis (Continuity)** | The continuous image of a connected set is connected; connected subsets of $\mathbb{Q}$ can only be single points. |
| **Calculus / Rolle's Theorem** | Reverse engineer auxiliary functions $g(x) = \int_0^x t(t-x)^2 f(t) dt$ such that derivative cancels boundary evaluation terms. |
| **Polynomial Algebra / GCD** | Use polynomial division / Euclidean algorithm $(2n+3)g(n) - 4f(n) = 3$ to isolate pure integer divisors. |
| **Quadratic Forms & Positive Definiteness** | Transform sums of fractions $\frac{1}{i+j-1}$ into integrals of squared polynomials $\int_0^1 [P(x)]^2 dx$. |
| **Parity & Infinite Descent** | When parity forces all elements to be even, divide by 2 repeatedly ($x_i / 2^m$) to deduce all elements must be 0. |
| **$p$-adic Valuations in Recurrences** | In non-linear recurrences $a_{n+1} = a_n^2 - 2c^{2^n}$, track the dominant lower-order power of $p$ using mathematical induction. |
| **Zeros of Polynomials** | Combine Rouché's theorem $|Q(z)| < |P(z)|$ with Descartes' rule of signs and calculus to tightly trap roots in the complex plane. |
| **Matrix Commutators & Norms** | Induct on power identities $AB^{2^k} - B^{2^k}A = 2^{k-1}B^{2^k-1}$ and take norms to obtain asymptotic contradictions. |
| **Extremal Geometric Products** | Use the Maximum Modulus Principle to push interior points to the boundary, then apply Power of a Point and single-variable calculus. |
