# MADHAVA MATHEMATICS COMPETITION
### (A Mathematics Competition for Undergraduate Students)
**Organized by:** Bhaskaracharya Pratishthana, Pune  
**Date:** 11/01/2026 | **Time:** 12.00 noon to 3.00 p.m. | **Max. Marks:** 100  

## Solutions and Scheme of Marking

**N.B.:** Part I carries 20 marks, Part II carries 30 marks and Part III carries 50 marks. Solutions not mentioned here should be graded by analogous schemes.

---

## Part I
**N.B. Each question in Part I carries 2 marks.**

1. Let $a < b < c$ be three positive integers in geometric progression whose common ratio is also an integer. If the arithmetic mean of $a, b, c$ is $b + 2$, then the value of $a$ is:  
   (A) 24 (B) 12 (C) 6 (D) 4.  
   **Ans: (C)**

2. Triangles are formed by joining the vertices of a regular polygon of 12 sides. The number of triangles having no side in common with the polygon is:  
   (A) 124 (B) 220 (C) 96 (D) 112.  
   **Ans: (D)**

3. If 
   $$f(x) = \begin{cases} ax + b & \text{if } x < -1 \\ x^2 + 1 & \text{if } -1 \le x < 1 \\ 3x - 1 & \text{if } x \ge 1 \end{cases}$$
   is continuous everywhere, then which of the following values can $ab$ never take?  
   (A) $-3$ (B) $-1$ (C) 0 (D) 3.  
   **Ans: (A)**

4. Let $f : [1, 3] \to \mathbb{R}$ be a continuous function. If $f$ takes rational values for all $x$ and $f(2) = 10$, then $f(1.5) =$  
   (A) 7.5 (B) 10 (C) 1.5 (D) 5.  
   **Ans: (B)**

5. If $f(x) = (x + 1)^2 - 1, x \ge -1$ then the set $\{x : f(x) = f^{-1}(x)\}$ is:  
   (A) $\phi$ (B) $\{-1, 1\}$ (C) $\{0, 1\}$ (D) $\{-1, 0\}$.  
   **Ans: (D)**

6. The number of real solutions of $1 + |e^x - 1| = e^x(e^x - 2)$ is:  
   (A) 1 (B) 2 (C) 0 (D) 3.  
   **Ans: (A)**

7. In how many ways can you choose an odd number of objects from $n$ objects?  
   (A) $2^{n-1}$ (B) $2^n$ (C) $2^n - 1$ (D) $n$.  
   **Ans: (A)**

8. The family of circles with center $(a, 0)$ and radius $a$ satisfies the differential equation:  
   (A) $\frac{dy}{dx} + x^2 - y^2 = 0$ (B) $2xy \frac{dy}{dx} + x^2 - y^2 = 0$ (C) $2xy \frac{dy}{dx} + x - y = 0$ (D) $2xy \frac{dy}{dx} + x^2 + y^2 = 0$.  
   **Ans: (B)**

9. The series 
   $$\sum_{n=0}^\infty \frac{\cos(x^{2n}) + \sin(x^{2n+1}) - e^{-|x|n}}{1 + n^2}$$
   (A) converges pointwise everywhere on $\mathbb{R}$, but not uniformly (B) does not converge at any point (C) converges uniformly on $\mathbb{R}$ (D) converges only at 0.  
   **Ans: (C)**

10. If $1, a_1, a_2, \dots, a_{n-1}$ are the $n^{\text{th}}$ ($n \ge 2$) roots of unity, then $\frac{1}{1 - a_1} + \frac{1}{1 - a_2} + \dots + \frac{1}{1 - a_{n-1}} =$  
    (A) $\frac{n}{2}$ (B) $\frac{n - 1}{2}$ (C) $\frac{1}{2}$ (D) $\frac{n(n - 1)}{2}$.  
    **Ans: (B)**

---

## Part II
**N.B. Each question in Part II carries 6 marks.**

### Question 1
Let $f : [0, 1] \to \mathbb{R}$ be a continuous function with $\int_0^1 x(x - 1)^2 f(x) dx = 0$. Prove that there is a real number $c \in (0, 1)$ such that
$$\int_0^c x^2 f(x) dx = c \int_0^c x f(x) dx$$

**Solution:**  
Define $g(x) = \int_0^x t(t - x)^2 f(t) dt$. **[2 marks]**  
Observe that $g(0) = 0$ and by given condition, $g(1) = 0$. Therefore, by Rolle’s theorem, there exists $c \in (0, 1)$ such that $g'(c) = 0$.  

Since 
$$g(x) = \int_0^x t(t - x)^2 f(t) dt = \int_0^x t^3 f(t) dt - 2x \int_0^x t^2 f(t) dt + x^2 \int_0^x t f(t) dt,$$
we get:
$$g'(x) = x^3 f(x) - 2 \int_0^x t^2 f(t) dt - 2x(x^2 f(x)) + 2x \int_0^x t f(t) dt + x^3 f(x)$$
$$= 2x \int_0^x t f(t) dt - 2 \int_0^x t^2 f(t) dt$$
Now $g'(c) = 0$ implies:
$$\int_0^c x^2 f(x) dx = c \int_0^c x f(x) dx \quad \mathbf{[4\text{ marks}]}$$

---

### Question 2
Let $f(x) = x^2 + 4x + 3$ and $g(x) = 2x + 5$. Show that $\gcd(f(n), g(n)) = 1$ or $3$ as $n$ varies over integers.

**Solution:**  
Note that $x^2 + 4x + 3 = (2x + 5)\left(\frac{1}{2}x + \frac{3}{4}\right) - \frac{3}{4}$.  
Therefore, we get:
$$3 = (2x + 5)(2x + 3) - 4(x^2 + 4x + 3)$$
Hence $\gcd(f(n), g(n))$ divides $3$. Thus, $\gcd(f(n), g(n)) = 1$ or $3$. **[6 marks]**

---

### Question 3
Let $a_1, a_2, \dots, a_n$ be real numbers. Prove that $\sum_{1 \le i, j \le n} \frac{a_i a_j}{i + j - 1} \ge 0$.

**Solution:**  
$$0 \le \int_0^1 \left(\sum_{i=1}^n a_i x^{i-1}\right)^2 dx = \int_0^1 \sum_{1 \le i, j \le n} a_i a_j x^{i+j-2} dx$$
$$= \sum_{1 \le i, j \le n} a_i a_j \int_0^1 x^{i+j-2} dx = \sum_{1 \le i, j \le n} \frac{a_i a_j}{i + j - 1} \quad \mathbf{[6\text{ marks}]}$$

---

### Question 4
Suppose for $n \ge 4$, $x_1, x_2, \dots, x_n$ are non-negative integers such that after removing any one of them the remaining numbers can be partitioned into two sets with equal sums. (i) If $n$ is even, then prove that $x_i = 0$, for all $i$. (ii) Does the same conclusion hold when $n$ is odd? Justify your answer.

**Solution:**  
**(i)** If $n$ is even, then all $x_i$ must be even. Indeed, if any $x_i$ is odd, then there exist two cases:  
(a) Suppose the number of odd $x_i$ is odd. Then taking an even number out, the parity of the two sets will not match.  
(b) If the number of odd $x_i$ is even, then taking an odd number out, the parity of the two sets will not match.  

Let $y_i = x_i / 2$. Then the new set $y_1, y_2, \dots, y_n$ also has the same property. Hence all $y_i$ are even. Continuing this way we will reach at least one odd number in the set that gives the contradiction. Hence $x_i = 0$, for all $i$. **[4 marks]**

**(ii)** NO. A counterexample is $\{1, 1, 1, 1, 1, 1, 1\}$ OR any other counterexample. **[2 marks]**

---

### Question 5
Give an example of a function $f : \mathbb{R} \to \mathbb{R}$, if it exists, which is continuous at $a$ if and only if $a$ is a positive integer. Justify your answer.

**Solution:**  
Define a function $f : \mathbb{R} \to \mathbb{R}$, as follows:
$$f(x) = \begin{cases} h(x) & \text{if } x \text{ is a rational number} \\ 0 & \text{if } x \text{ is an irrational number} \end{cases}$$
where
$$h(x) = \begin{cases} 1 & \text{if } x \le 1/2 \\ \sin(\pi x) & \text{if } x > 1/2 \end{cases}$$
Note that $h(x) = 0$ for all positive integers $x$. Hence the function $f(x)$ is continuous at $a$ if and only if $a$ is a positive integer.  
*(OR Any other correct example.)* **[6 marks]**

---

## Part III

### Question 1
Suppose $\alpha, \beta$ are roots of the polynomial $x^2 + bx + c$. Let $p > 2$ be a prime satisfying the conditions: $p$ divides $b$, $p$ divides $c$, but $p^2$ does not divide $c$.  
(i) Find the largest power of $p$ which divides $\alpha^4 + \beta^4$. **[2]**  
(ii) Find the largest power of $p$ which divides $\alpha^8 + \beta^8$. **[3]**  
(iii) For any positive integer $n$, find the largest power of $p$ which divides $\alpha^{2^n} + \beta^{2^n}$. **[8]**

**Solution:**  
Define $a_n = \alpha^{2^n} + \beta^{2^n}$, for all $n \in \mathbb{N}$.  
Then $a_1 = \alpha^2 + \beta^2 = (\alpha + \beta)^2 - 2\alpha\beta = b^2 - 2c$. Since $p$ divides $b$ and $c$, $p$ divides $a_1$. Since $p^2$ divides $b^2$ but it does not divide $c$, $p^2$ does not divide $a_1$. Hence $p^1$ is the largest power of $p$ which divides $a_1$.

**(i)** Let $a_2 = \alpha^4 + \beta^4 = a_1^2 - 2\alpha^2\beta^2 = (b^2 - 2c)^2 - 2c^2$. This implies that $p^2$ divides $a_2$.  
*Claim:* $p^3$ does not divide $a_2$. Observe that $a_2 = (b^2 - 2c)^2 - 2c^2 = b^4 - 4b^2 c + 2c^2$. Since $p^3$ does not divide $c^2$, but it divides other terms, we have $p^3$ does not divide $a_2$. Hence $p^2$ is the largest power of $p$ which divides $a_2$. **[2 marks]**

**(ii)** Let $a_3 = \alpha^8 + \beta^8 = a_2^2 - 2\alpha^4\beta^4 = a_2^2 - 2c^4 = (b^4 - 4b^2 c + 2c^2)^2 - 2c^4 = b^8 - 8b^6 c + 20b^4 c^2 - 16b^2 c^3 + 2c^4$.  
Now by case (i), $p^4$ divides $a_3$. Since $p^5$ divides all other terms but it does not divide $c^4$, we get $p^5$ does not divide $a_3$. Hence $p^4$ is the largest power of $p$ which divides $a_3$. **[3 marks]**

**(iii)** *Claim:* For all $n \ge 2$, there exists an integer $b_n$ such that $a_n = p^{2^{n-1}+1}b_n + 2c^{2^{n-1}}$.  
*Proof:* Proof of the claim is by induction on $n$. For $n = 2$, we have $a_2 = p^3 b_2 + 2c^2$. Assume that the result is true for some positive integer $n$. Therefore $a_n = p^{2^{n-1}+1}b_n + 2c^{2^{n-1}}$.  
Now $a_{n+1} = a_n^2 - 2\alpha^{2^n}\beta^{2^n} = a_n^2 - 2c^{2^n} = (p^{2^{n-1}+1}b_n + 2c^{2^{n-1}})^2 - 2c^{2^n} = p^{2^n+1}b_{n+1} + 2c^{2^n}$.  
Hence the claim is true for $n + 1$. Thus, the claim is true for all $n \ge 2$.  
Since $p^{2^{n-1}}$ divides $c^{2^{n-1}}$, we have $p^{2^{n-1}}$ divides $a_n$. Since $p^{2^{n-1}+1}$ does not divide $c^{2^{n-1}}$, we get $p^{2^{n-1}+1}$ does not divide $a_n$. Hence $p^{2^{n-1}}$ is the largest power of $p$ which divides $a_n$. **[8 marks]**

---

### Question 2
(i) Show that $x^6 - 6x^5 + 1 = 0$ has a unique root in the interval $(0, 1)$. **[3]**  
(ii) Show that every complex (non-real) root $z$ of $x^6 - 6x^5 + 1 = 0$ satisfies $|z| \le x_0$, where $x_0$ is the root of this equation in $(0, 1)$. **[10]**

**Solution:**  
**(i)** Let $f(x) = x^6 - 6x^5 + 1$ for $x \ge 0$. Observe that $f(0) = 1 > 0$ and $f(1) = -4 < 0$. Therefore there exists a root in the interval $(0, 1)$. **[1 mark]**  
Also $f(6) = 1 > 0$. Therefore there exists a root in the interval $(1, 6)$. Since there are only two sign changes, by Descartes’ rule $f$ has at most two positive real roots. Hence $f$ has a unique root in the interval $(0, 1)$. **[2 marks]**  
*(OR Note that $f'(x) = 6x^5 - 30x^4 = 6x^4(x - 5) \le 0$ for $0 \le x \le 5$ and $f'(x) \ge 0$ for $x \ge 5$. Therefore, $f$ is decreasing for $0 \le x \le 5$ and increasing for $x \ge 5$. Hence $f$ has a unique root in the interval $(0, 1)$. [2 marks])*  
*(Note: Correct argument for uniqueness will get 2 marks).*

**(ii) Method 1:**  
Let $x_0$ be the unique root of $f$ in the interval $(0, 1)$. Since $f(0) > 0$, we have $f(x) > 0$ for $0 \le x < x_0$. Let $z = r e^{i\theta}$ be a complex root of $f$ where $r > 0$ and $-\pi < \theta < \pi, \theta \ne 0$.  
The real and imaginary parts of the equation $f(z) = 0$ give:
$$r^6 \cos 6\theta - 6r^5 \cos 5\theta = -1$$
$$r^6 \sin 6\theta - 6r^5 \sin 5\theta = 0$$
Solving these equations we get:
$$r^6 = \frac{\sin 5\theta}{\sin \theta}, \quad r^5 = \frac{\sin 6\theta}{6\sin \theta} \quad [*] \quad \mathbf{[4\text{ marks}]}$$
It can be seen that $r^6 < 5$. Hence we have $r < 5$. To show that $r < x_0$, we must show that $f(r) > 0$.
$$f(r) = r^6 - 6r^5 + 1 = \frac{\sin 5\theta}{\sin \theta} - 6\frac{\sin 6\theta}{6\sin \theta} + 1 = \frac{\cos \frac{\theta}{2} - \cos \frac{11\theta}{2}}{\cos \frac{\theta}{2}}$$
Note that $\cos \frac{\theta}{2} > 0$. If $\cos \frac{11\theta}{2} \le 0$, then $f(r) \ge 1 > 0$.  
If $\cos \frac{11\theta}{2} > 0$, then the first factor in the following is positive:
$$\left(\cos \frac{\theta}{2} + \cos \frac{11\theta}{2}\right)\left(\cos \frac{\theta}{2} - \cos \frac{11\theta}{2}\right) = \frac{\cos \theta - \cos 11\theta}{2} = \sin 5\theta \sin 6\theta$$
Right hand side of the above expression is positive by $[*]$. Hence the second factor is positive.  
Thus $f(r) > 0$. Since $r < 5$ and $f(r) > 0$, we get $r < x_0$. **[6 marks]**

**OR Method 2:**  
Let $x_1$ be the root of $f$ in the interval $(1, 6)$. If $x_0 < x < 1$, then $f(x) < 0$. Therefore $|z^6 + 1| \le |z^6| + 1 < |6z^5|$ if $|z| = x$. So by Rouché’s theorem, $z^6 - 6z^5 + 1$ also has 5 zeros inside $|z| = x$. Since this is true for every $x > x_0$, all zeros except $x_1$ satisfy $|z| \le x_0$. **[10 marks]**

---

### Question 3
(i) Suppose $A, B$ are $n \times n$ complex matrices with $AB^2 - B^2 A = B$. Show that $B$ is a nilpotent matrix. **[9]**  
(ii) Let $B$ be an $n \times n$ complex nilpotent matrix. Does there exist an $n \times n$ matrix $A$ such that $AB^2 - B^2 A = B$? Justify your answer. **[3]**

**Solution:**  
**(i)** *Claim:* $AB^{2^n} - B^{2^n} A = 2^{n-1} B^{2^n - 1}$, for all $n \ge 2$.  
The proof is by induction on $n$. We first prove the result for $n = 2$. Given that $AB^2 - B^2 A = B$.  
Multiplying both sides by $B^2$ from the right we get:
$$AB^4 - B^2 A B^2 = B^3$$
Substituting $AB^2 = B + B^2 A$, we get $AB^4 - B^2(B + B^2 A) = B^3$. Therefore:
$$AB^4 - B^4 A = 2B^3$$
Hence, the result is true for $n = 2$.  
Suppose the result is true for some positive integer $k > 2$. Therefore:
$$AB^{2^k} - B^{2^k} A = 2^{k-1} B^{2^k - 1}$$
Multiplying both sides by $B^{2^k}$ from the right we get:
$$AB^{2^k} B^{2^k} - B^{2^k} A B^{2^k} = 2^{k-1} B^{2^k - 1} B^{2^k}$$
Then put $AB^{2^k} = 2^{k-1} B^{2^k - 1} + B^{2^k} A$. Hence:
$$AB^{2^{k+1}} - B^{2^{k+1}} A = 2^k B^{2^{k+1} - 1}$$
Therefore the result is true for $k + 1$. Thus, the result is true for all $n \ge 2$. **[6 marks]**

By taking norms we get:
$$2^{n-1} \|B^{2^n - 1}\| \le 2 \|A\| \|B^{2^n}\|$$
Suppose $B$ is not a nilpotent matrix. Then $\|B^k\| \ne 0, \forall k \ge 1$. After cancellation we get:
$$2^{n-1} \le 2 \|A\| \|B\| \quad \text{for all positive integers } n \ge 2$$
This is a contradiction. **[3 marks]**

**(ii)** Let $B = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}$. Then $B^2 = 0$. Therefore there does not exist a matrix $A$ such that $AB^2 - B^2 A = B$. *(OR Any other correct example.)* **[3 marks]**

---

### Question 4
Let $A, B, C, D$ be vertices of a quadrilateral inscribed in the unit circle. Let $P$ be a point in the interior of the quadrilateral $ABCD$. Show that
$$|PA||PB||PC||PD| < \frac{27}{16}$$
where $|PX|$ is the length of the line segment $PX$. **[12]**

**Solution:**  
Suppose $P$ is a point on the boundary of the quadrilateral $ABCD$, say on $BC$. Let $x$ be the distance of $P$ from the center of the unit circle $O$. We know that for all chords $XY$ through point $P$ the product $|PX||PY|$ is constant. Therefore:
$$|PB||PC| = (1 - x)(1 + x) \quad \mathbf{[6\text{ marks}]}$$
Applying triangle inequality to triangle $OPA$, $|PA| < 1 + x$. Similarly $|PD| < 1 + x$. Hence:
$$|PA||PB||PC||PD| < (1 - x)(1 + x)^3$$
Let $f(x) = (1 - x)(1 + x)^3$. Then $f'(x) = (1 + x)^2(2 - 4x) = 0$ at $x = \frac{1}{2}$.  
Observe that $f''(1/2) < 0$. Now $f(1/2) = \frac{27}{16}$ is the maximum value.  
By Maximum Modulus Principle, the maximum value cannot occur at any interior point.  
Hence, $|PA||PB||PC||PD| < \frac{27}{16}$. **[6 marks]**
