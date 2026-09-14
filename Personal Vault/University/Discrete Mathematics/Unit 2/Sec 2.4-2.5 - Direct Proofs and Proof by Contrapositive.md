# Sec. 2.4 — Writing Direct Proofs
# Sec. 2.5 — Proof by Contrapositive

## Direct Proof of an Implication

To prove an implication is true, we **assume the hypothesis is true**, and use the hypothesis and other known true statements and definitions to deduce that the conclusion is true.

| $p$ | $q$ | $p \rightarrow q$ |
|---|---|---|
| T | T | T |
| T | F | F |
| F | T | T |
| F | F | T |

*(An implication is only false when the hypothesis is true and the conclusion is false — this is why a direct proof only needs to handle the case where $p$ is true.)*

---

## Example 1 — "The sum of two odd integers is an even integer."

**(a) Hypothesis:** $x$ and $y$ are odd integers.

**(b) Conclusion:** $x + y$ is an even integer.

**(c) In the form $p \rightarrow q$:** "If $x$ and $y$ are odd integers, then $x+y$ is even."

**(d) Proof.**
1. Assume that **$x$ and $y$ are odd integers**. We will show that **$x+y$ is even**.
2. Since **$x$ is odd**, $x = 2k+1$ for some integer $k$.
   Since **$y$ is odd**, $y = 2j+1$ for some integer $j$.
3. Then, $x + y = (2k+1) + (2j+1) = 2k + 2j + 2 = 2(k+j+1)$.
4. Since $k$ and $j$ are integers, **$k+j+1$ is an integer**.
5. Hence, $x+y = 2(k+j+1)$ is even. $\blacksquare$

---

## Using the Definitions (Sec. 2.1)

For each implication below: what should we **assume** (and how do we use it)? What is the **goal**?

**"If $x$ is an even integer and $y$ is an odd integer, then $2x + 5y$ is odd."**
- **Assume:** $x = 2a$ for some integer $a$ (since $x$ even); $y = 2b+1$ for some integer $b$ (since $y$ odd).
- **Goal:** Show $2x+5y = 2m+1$ for some integer $m$.
- *(Work: $2x+5y = 2(2a) + 5(2b+1) = 4a + 10b + 5 = 2(2a+5b+2)+1$, which is odd.)*

**"If $r$ is rational, then $r^2$ is also rational."**
- **Assume:** $r = \dfrac{a}{b}$ for integers $a, b$ with $b \neq 0$ (since $r$ rational).
- **Goal:** Show $r^2 = \dfrac{c}{d}$ for some integers $c, d$ with $d \neq 0$.
- *(Work: $r^2 = \dfrac{a^2}{b^2}$; since $a^2, b^2$ are integers and $b^2 \neq 0$, $r^2$ is rational.)*

**"If $x, y$ are integers and $x \mid y$, then $x^2 \mid y^2$."**
- **Assume:** $y = kx$ for some integer $k$ (since $x \mid y$).
- **Goal:** Show $y^2 = m \cdot x^2$ for some integer $m$.
- *(Work: $y^2 = (kx)^2 = k^2x^2$, so $m = k^2$, which is an integer.)*

---

## Exercise 2 — "The sum of the square of an odd integer and the square of an even integer is an odd integer."

**(a) Hypothesis:** $x$ is an odd integer and $y$ is an even integer.

**(b) Conclusion:** $x^2 + y^2$ is an odd integer.

**(c) In the form $p \rightarrow q$:** "If $x$ is odd and $y$ is even, then $x^2+y^2$ is odd."

**(d) Proof.**
1. Assume that $x$ is odd and $y$ is even. We will show that $x^2+y^2$ is odd.
2. Since $x$ is odd, $x = 2k+1$ for some integer $k$. Since $y$ is even, $y = 2j$ for some integer $j$.
3. Then,
$$x^2+y^2 = (2k+1)^2 + (2j)^2 = 4k^2+4k+1+4j^2 = 2(2k^2+2k+2j^2)+1.$$
4. Since $k, j$ are integers, $2k^2+2k+2j^2$ is an integer.
5. Hence, $x^2+y^2$ is odd. $\blacksquare$

---

## Proof by Contrapositive

Since an implication is logically equivalent to its contrapositive, we may prove the contrapositive instead (if it's easier!).

- The contrapositive of an implication $p \rightarrow q$ is $\neg q \rightarrow \neg p$.
- The contrapositive statement and the original statement are **logically equivalent** (they have the same truth value).

---

## Example 3 — "For any integers $x$ and $y$, if $x - y$ is odd, then $x$ is odd or $y$ is odd."

**(a) Negation of the conclusion ($\neg q$):** $x$ is even **and** $y$ is even.

**(b) Negation of the hypothesis ($\neg p$):** $x - y$ is even.

**(c) Contrapositive form ($\neg q \rightarrow \neg p$):** "If $x$ is even and $y$ is even, then $x - y$ is even."

**(d) Proof of the contrapositive.**
1. Assume that $x$ and $y$ are even integers. We will show that $x - y$ is even.
2. Since $x$ is even, $x = 2k$ for some integer $k$. Since $y$ is even, $y = 2j$ for some integer $j$.
3. Then, $x - y = 2k - 2j = 2(k - j)$.
4. Since $k, j$ are integers, $k - j$ is an integer.
5. Hence, $x - y$ is even. Since the contrapositive is true, the original statement is also true. $\blacksquare$

---

## When to Use a Direct Proof vs. a Proof by Contrapositive

In principle, choose the approach with a **hypothesis that is easier to work with**.

**"For every integer $n$, if $n^2 - 2n + 7$ is even, then $n$ is odd."**

| | Hypothesis | Conclusion |
|---|---|---|
| **Direct** | "$n^2-2n+7$ is even" — hard to use directly | "$n$ is odd" |
| **Contrapositive** | "$n$ is even" — easy to use ($n=2k$) | "$n^2-2n+7$ is odd" |

$\Rightarrow$ **Use the contrapositive** — assuming $n$ is even is much easier to work with than assuming an expression is even.

**"For every positive real number $r$, if $r$ is irrational, then $\sqrt{r}$ is irrational."**

| | Hypothesis | Conclusion |
|---|---|---|
| **Direct** | "$r$ is irrational" — hard to use (no nice algebraic form) | "$\sqrt{r}$ is irrational" |
| **Contrapositive** | "$\sqrt{r}$ is rational" — easy to use ($\sqrt{r} = a/b$) | "$r$ is rational" |

$\Rightarrow$ **Use the contrapositive** — a rational hypothesis (explicit fraction form) is far easier to manipulate than an irrational one.

### General guidance
- **Hypotheses that are usually easier to work with:** positive/constructive statements that give an explicit algebraic form — e.g., "is even" ($x=2k$), "is rational" ($x=a/b$), "$x \mid y$" ($y=kx$).
- **Hypotheses that are usually harder to work with:** negative statements with no explicit form — e.g., "is irrational," "is not divisible by," "$\neq$." When the *original* hypothesis is one of these, consider proving the **contrapositive** instead, since its hypothesis will be the easier, positive kind.
