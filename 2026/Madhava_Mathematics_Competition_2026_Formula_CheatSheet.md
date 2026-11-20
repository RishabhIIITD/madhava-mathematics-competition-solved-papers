# Madhava Mathematics Competition — 2026
## Official Formula, Identity & Quick-Revision Cheat Sheet

**Exam Date:** 11/01/2026 | **Organized by:** Bhaskaracharya Pratishthana, Pune & NBHM  
**Purpose:** Rapid 1-to-2 page high-yield reference card for last-minute review and formula memorization.

---

### ⚡ 1. Part I Quick Answer Key & Result Summary

| Q# | Topic | Key Formula / Technique | Correct Choice | Value / Result |
| :---: | :--- | :--- | :---: | :---: |
| **Q1** | Diophantine GP/AM | $a(r - 1)^2 = 6 \implies (r-1)^2 = 1$ | **(C)** | $a = 6$ |
| **Q2** | Polygon Combinatorics | $N_0 = \frac{n(n-4)(n-5)}{6}$ with $n = 12$ | **(D)** | $112$ |
| **Q3** | Piecewise Continuity | $b = a + 2 \implies ab = (a+1)^2 - 1 \ge -1$ | **(A)** | Never $-3$ |
| **Q4** | Connected Topology | $f([1, 3]) \subseteq \mathbb{Q}$ is connected $\implies$ constant | **(B)** | $f(1.5) = 10$ |
| **Q5** | Fixed Points / Inverse | Strictly increasing $f \implies f(x) = f^{-1}(x) \iff f(x) = x$ | **(D)** | $\{-1, 0\}$ |
| **Q6** | Exponential Equations | $u = e^x > 0 \implies 1 + \|u-1\| = u(u-2)$ | **(A)** | $1$ real root ($x = \ln 3$) |
| **Q7** | Subset Parity | $\sum_{k \text{ odd}} \binom{n}{k} = \frac{1}{2}(2^n) = 2^{n-1}$ | **(A)** | $2^{n-1}$ |
| **Q8** | Differential Equations | $(x-a)^2 + y^2 = a^2 \implies a = x + yy'$ | **(B)** | $2xy \frac{dy}{dx} + x^2 - y^2 = 0$ |
| **Q9** | Uniform Convergence | $\|u_n(x)\| \le \frac{3}{1+n^2} = M_n$ (Weierstrass M-Test) | **(C)** | Uniformly on $\mathbb{R}$ |
| **Q10**| Roots of Unity | $\sum_{k=1}^{n-1} \frac{1}{1-a_k} = \frac{P'(1)}{P(1)} = \frac{n-1}{2}$ | **(B)** | $\frac{n-1}{2}$ |

---

### 📐 2. Combinatorics & Geometry on Polygons

For a regular $n$-sided polygon ($n \ge 6$):
* **Total triangles from vertices:** $\binom{n}{3} = \frac{n(n-1)(n-2)}{6}$
* **Triangles sharing exactly 2 edges:** $N_2 = n$
* **Triangles sharing exactly 1 edge:** $N_1 = n(n - 4)$
* **Triangles sharing 0 edges:**
  $$N_0 = \binom{n}{3} - n(n-4) - n = \frac{n(n-4)(n-5)}{6}$$
* **Total diagonals in an $n$-gon:** $D = \binom{n}{2} - n = \frac{n(n-3)}{2}$
* **Subset Parity Identity:**
  $$\sum_{k \text{ odd}} \binom{n}{k} = \sum_{k \text{ even}} \binom{n}{k} = 2^{n-1} \quad (n \ge 1)$$

---

### 🔢 3. Number Theory & Algebra Cheat Sheet

* **Diophantine GP Condition:**
  If $a < ar < ar^2$ in GP with AM $= ar + k$, then:
  $$a(r - 1)^2 = 3k \implies (r-1)^2 \mid 3k$$
* **Polynomial GCD Bound (Bezout Remainder):**
  If polynomials $A(x), B(x) \in \mathbb{Z}[x]$ satisfy $A(x)f(x) + B(x)g(x) = C \in \mathbb{Z} \setminus \{0\}$, then:
  $$\gcd(f(n), g(n)) \mid C \quad \forall n \in \mathbb{Z}$$
* **$p$-adic Valuations ($v_p(x)$):**
  - **Multiplication:** $v_p(ab) = v_p(a) + v_p(b)$
  - **Ultrametric Inequality:** $v_p(a + b) \ge \min(v_p(a), v_p(b))$
  - **Strict Dominance:** If $v_p(a) < v_p(b)$, then $v_p(a + b) = v_p(a)$.
  - **Non-linear Recurrence Valuation:** For $a_n = \alpha^{2^n} + \beta^{2^n}$ where $x^2 + bx + c = 0$ with $p \mid b, v_p(c) = 1, p > 2$:
    $$v_p\left(\alpha^{2^n} + \beta^{2^n}\right) = 2^{n-1} \quad \forall n \ge 1$$
* **Parity & Infinite Descent Template:**
  If removing any $x_k$ leaves an even partition, then $S - x_k = 2A_k \implies x_k \equiv S \pmod 2$.
  - If $n$ is even, all $x_i$ must be even. Setting $y_i = x_i / 2$ forces $x_i \equiv 0 \pmod{2^m} \implies x_i = 0$.
  - If $n$ is odd, $x_1 = \dots = x_n = 1$ is a valid counterexample.

---

### 📈 4. Real Analysis & Calculus Fast Formulas

* **Connected Image Principle:**
  If $X$ is connected (e.g. $[a, b]$) and $f: X \to Y$ is continuous:
  - If $Y \subseteq \mathbb{Q}$, then $f(x) \equiv c$ (constant).
  - If $Y$ is discrete, then $f(x) \equiv c$.
* **Rolle's Theorem Auxiliary Kernel:**
  To show $\int_0^c x^2 f(x)dx = c \int_0^c x f(x)dx$ given $\int_0^1 x(x-1)^2 f(x)dx = 0$:
  $$g(x) = \int_0^x t(t-x)^2 f(t)dt \implies g'(x) = 2x \int_0^x t f(t)dt - 2 \int_0^x t^2 f(t)dt$$
  $$g(0) = g(1) = 0 \implies g'(c) = 0 \text{ by Rolle's Theorem.}$$
* **Weierstrass M-Test:**
  If $|u_n(x)| \le M_n$ for all $x \in E$ and $\sum_{n=1}^\infty M_n < \infty$, then $\sum u_n(x)$ converges **uniformly and absolutely** on $E$.
* **Fixed Points of Increasing / Decreasing Functions:**
  - $f$ strictly increasing $\implies f(x) = f^{-1}(x) \iff f(x) = x$.
  - $f$ strictly decreasing $\implies$ solutions to $f(x) = f^{-1}(x)$ satisfy $f(f(x)) = x$ (can lie off $y = x$).
* **Dirichlet Continuity Modulation:**
  $$f(x) = \begin{cases} h(x) & x \in \mathbb{Q} \\ 0 & x \in \mathbb{R}\setminus\mathbb{Q} \end{cases} \quad \text{is continuous at } a \iff h(a) = 0$$

---

### 🌀 5. Complex Analysis & Geometry Formulas

* **Roots of Unity Reciprocal Sum:**
  For $P(x) = \frac{x^n - 1}{x - 1} = \prod_{k=1}^{n-1} (x - a_k)$:
  $$\sum_{k=1}^{n-1} \frac{1}{1 - a_k} = \frac{P'(1)}{P(1)} = \frac{n - 1}{2}$$
* **Geometric Real Part Invariant:**
  $$\operatorname{Re}\left(\frac{1}{1 - e^{i\theta}}\right) = \frac{1}{2} \quad \text{for all } \theta \not\equiv 0 \pmod{2\pi}$$
* **Rouché's Theorem (Root Counting in Disk):**
  If $|Q(z)| < |P(z)|$ on a closed contour $C$, then $P(z)$ and $P(z) + Q(z)$ have the **same number of zeros** inside $C$.
* **Descartes' Rule of Signs:**
  $$\text{Number of positive real roots} \le \text{sign variations of } P(x) \quad (\text{differing by an even integer})$$
* **Maximum Modulus Principle:**
  A non-constant holomorphic function $F(z)$ on a compact domain $K$ satisfies:
  $$|F(z)| < \max_{w \in \partial K} |F(w)| \quad \forall z \in \operatorname{int}(K)$$
* **Intersecting Chords (Power of a Point):**
  For point $P$ at distance $x = |OP|$ from center in the unit circle:
  $$|PX||PY| = 1 - x^2 = (1 - x)(1 + x)$$
* **Extremal Geometric Product on Boundary:**
  $$\max_{x \in [0, 1]} (1 - x)(1 + x)^3 = \frac{27}{16} \quad \text{attained at } x = \frac{1}{2}$$

---

### 🧮 6. Linear Algebra & Differential Equations

* **Matrix Commutator Properties:**
  $$[A, B] = AB - BA, \quad \operatorname{Tr}([A, B]) = 0$$
* **Power Commutator Recurrence:**
  If $AB^2 - B^2 A = B$, then for all $k \ge 1$:
  $$AB^{2^k} - B^{2^k} A = 2^{k-1} B^{2^k - 1}$$
* **Nilpotency via Matrix Norm Contradiction:**
  $$2^{k-1}\|B^{2^k-1}\| \le 2\|A\|\|B\| \|B^{2^k-1}\| \implies 2^{k-1} \le 2\|A\|\|B\| \quad \text{(forces } B \text{ to be nilpotent)}$$
* **Nilpotent Counterexample:**
  If $B^2 = 0$ (e.g. $B = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}$), then $AB^2 - B^2 A \equiv 0 \ne B$.
* **Hilbert Matrix Quadratic Form:**
  $$H_{ij} = \frac{1}{i + j - 1} = \int_0^1 x^{i+j-2} dx$$
  $$\mathbf{a}^T H \mathbf{a} = \sum_{i,j} a_i a_j H_{ij} = \int_0^1 \left(\sum_{i=1}^n a_i x^{i-1}\right)^2 dx = \int_0^1 [P(x)]^2 dx \ge 0$$
  $H$ is strictly positive definite.
* **Family of Circles with Center $(a, 0)$ and Radius $a$:**
  $$x^2 + y^2 - 2ax = 0 \implies a = x + y y' \implies 2xy \frac{dy}{dx} + x^2 - y^2 = 0$$
