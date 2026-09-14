# Sec. 1.8 — De Morgan's Law for Quantified Statements

## Negation of "for all" and "there exists"

- $\neg(\forall x,\ P(x)) \equiv \exists x,\ \neg P(x)$
- $\neg(\exists x,\ P(x)) \equiv \forall x,\ \neg P(x)$

**Idea:** Negating a universal statement turns it into an existential statement about the negation of $P(x)$, and vice versa.

---

## Example 1

**What is the negation of "There exist positive integers $a$ and $b$ such that $\left(\dfrac{a}{b}\right)^2 = 2$"?**

- **Original statement in symbols:**
$$\exists\ a, b \in \mathbb{Z}^+,\ \left(\frac{a}{b}\right)^2 = 2$$

- **Take negation and apply De Morgan's Law:**
$$\forall\ a, b \in \mathbb{Z}^+,\ \left(\frac{a}{b}\right)^2 \neq 2$$

In words: "For all positive integers $a$ and $b$, $\left(\dfrac{a}{b}\right)^2 \neq 2$."

---

## Example 2

Domain: students at a university.
- $E(x)$: $x$ is enrolled in the class.
- $T(x)$: $x$ took the test.

**What is the negation of "Everyone who took the test is enrolled in the class"?**

- Original: $\forall x,\ T(x) \rightarrow E(x)$
- Negation: $\exists x,\ T(x) \wedge \neg E(x)$

In words: **"There exists a student who took the test but is not enrolled in the class."**

---

## Summary Table

| Original statement | Negation of statement | Example of original | Example of negation |
|---|---|---|---|
| $p \wedge q$ | $\neg p \vee \neg q$ | "2 is prime and 2 is even" | "2 is not prime or 2 is not even" |
| $p \vee q$ | $\neg p \wedge \neg q$ | "$2^3 = 6$ or $\sqrt{34} = 2$" | "$2^3 \neq 6$ and $\sqrt{34} \neq 2$" |
| $p \rightarrow q$ | $p \wedge \neg q$ | "If 2 is even, then 6 is odd." | "2 is even and 6 is not odd." |
| $\exists x,\ P(x)$ | $\forall x,\ \neg P(x)$ | "There is a real number $x$ such that $x^2 = -1$" | "For all real numbers $x$, $x^2 \neq -1$" |
| $\forall x,\ P(x)$ | $\exists x,\ \neg P(x)$ | "For all integers $n$, $-1$ is a factor of $n$" | "There exists an integer $n$ such that $-1$ is not a factor of $n$" |

### Key takeaways
- $\wedge \leftrightarrow \vee$ swap when negating (De Morgan's).
- $p \rightarrow q$ negates to $p \wedge \neg q$ (NOT $\neg p \rightarrow \neg q$ — that's a common mistake).
- $\forall \leftrightarrow \exists$ swap when negating.
