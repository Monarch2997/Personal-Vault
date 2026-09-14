# Sec. 2.1 — Mathematical Definitions

## What is an "integer"?
An integer is any number in the set $\mathbb{Z} = \{\dots, -2, -1, 0, 1, 2, \dots\}$ — i.e., a whole number that can be positive, negative, or zero, with no fractional or decimal part.

---

## Definition 1 — Parity

Let $n$ be an integer. Then:
- $n$ is **even** if $n = 2k$ for some integer $k$.
- $n$ is **odd** if $n = 2k + 1$ for some integer $k$.
- The **parity** of an integer is whether the integer is odd or even.

**Examples:** $4 = 2(2)$ is even. $7 = 2(3)+1$ is odd. $-6 = 2(-3)$ is even.

---

## Definition 2 — Rational numbers

A number $x$ is **rational** if $x = \dfrac{a}{b}$ for some integers $a, b$ with $b \neq 0$.

**Examples:** $\dfrac{1}{2}$, $3 = \dfrac{3}{1}$, $0.5 = \dfrac{1}{2}$, $-\dfrac{7}{3}$ are all rational.

---

## Definition 3 — Divisibility

Let $x, y$ be two integers. Then **$x$ divides $y$** if and only if $x \neq 0$ and $y = kx$ for some integer $k$.

Equivalently: "$y$ is divisible by $x$", "$y$ is a multiple of $x$", "$x$ is a factor of $y$", "$x$ is a divisor of $y$".

**Notation:** $x \mid y$

---

## Definition 4 — Prime and Composite

- An integer $n \geq 2$ is called **prime** if and only if the only (positive) divisors of $n$ are $1$ and $n$.
- An integer $n \geq 2$ is called **composite** if and only if it is not prime, that is, $n = ab$ for some integers $a, b$ with $1 < a < n$ and $1 < b < n$.

**Examples:** $2, 3, 5, 7, 11$ are prime. $4, 6, 8, 9, 10$ are composite.

---

## Properties of 0

| Property | Result |
|---|---|
| **Parity** | Even ($0 = 2 \times 0$) |
| **Rationality** | Rational ($0 = \dfrac{0}{1}$) |
| **Divisibility** | Every nonzero integer divides $0$ (since $0 = n \times 0$); but $0$ does not divide any nonzero integer |
| **Primality** | Neither prime nor composite (fails $n \geq 2$ requirement) |

## Properties of 1

| Property | Result |
|---|---|
| **Parity** | Odd ($1 = 2(0) + 1$) |
| **Rationality** | Rational ($1 = \dfrac{1}{1}$) |
| **Divisibility** | $1$ divides every integer |
| **Primality** | Neither prime nor composite (fails $n \geq 2$ requirement) |

---

## Inequalities (Trichotomy)

For any real numbers $x$ and $y$, **exactly one** of the following is true:
$$x < y, \qquad x = y, \qquad x > y$$

---

## Definition 5 — Sign of a number

Let $x$ be a real number. Then:
- $x$ is **positive** if $x > 0$.
- $x$ is **negative** if $x < 0$.
- $x$ is **non-positive** if $x \leq 0$.
- $x$ is **non-negative** if $x \geq 0$.

---

## Example 6 — Negating inequalities

- Negation of "$x < 3$" is $x \geq 3$.
- Negation of "$x > 4$" is $x \leq 4$.
- Negation of "$x \leq 5$" is $x > 5$.
- Negation of "$x \geq 6$" is $x < 6$.

**Pattern:** Negating $<$ gives $\geq$; negating $>$ gives $\leq$ (and vice versa) — the boundary point flips into the negated statement.
