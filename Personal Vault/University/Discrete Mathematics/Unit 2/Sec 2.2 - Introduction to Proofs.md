# Sec. 2.2 — Introduction to Proofs

- A **theorem** is a statement that can be proven to be true.
- A **proof** consists of a series of steps, each of which follows logically from assumptions, or from previously proven statements, whose final step should result in the statement of the theorem being proven.
- An **axiom** is a statement assumed to be true (without proof).

Many mathematical theorems are universal statements or implication statements. Methods of proof introduced in this course:

(a) Proof by exhaustion ($\forall$)
(b) Disproof by counterexample ($\forall, \rightarrow$)
(c) Constructive proof of existence ($\exists$)
(d) Proof by contradiction
(e) Direct proof ($\rightarrow, \leftrightarrow$)
(f) Proof by contrapositive ($\rightarrow, \leftrightarrow$)
(g) Proof by cases
(h) Proof by induction

### Recall

| | To prove | To disprove |
|---|---|---|
| $\forall x,\ P(x)$ | Show that $P(x)$ is **T** for every $x$ in the domain. | Find one counterexample $x$ such that $P(x)$ is **F**. |
| $\exists x,\ P(x)$ | Find one example $x$ such that $P(x)$ is **T**. | Show that $P(x)$ is **F** for every $x$ in the domain. |

---

## Proof by Exhaustion

If the domain of a universal statement is small, it may be easiest to prove the statement by checking each element individually.

**Example 1.** Prove: "For all positive integers $n < 3$, $(n+1)^2 \geq 3^n$."

The domain is $\{1, 2\}$ (positive integers less than 3).

- $n = 1$: $(1+1)^2 = 4$ and $3^1 = 3$. Since $4 \geq 3$, the statement holds.
- $n = 2$: $(2+1)^2 = 9$ and $3^2 = 9$. Since $9 \geq 9$, the statement holds.

Since the statement holds for every $n$ in the domain, it is proven

---

## Disproof by Counterexample

To show that an implication or a "for all" statement is false, it is enough to find a single case (a counterexample) where the statement does not hold.

**Example 2.** Disprove each statement.

**(a)** "If $x$ is a real number and $x^2 < 1$, then $0 < x < 1$."

*Counterexample:* Let $x = -\dfrac{1}{2}$. Then $x^2 = \dfrac{1}{4} < 1$, so the hypothesis holds. But $0 < -\dfrac{1}{2} < 1$ is false, since $x$ is negative. This disproves the statement.

**(b)** "Every positive integer can be expressed as the sum of the squares of two integers."

*Counterexample:* Consider $n = 3$. The only squares $\leq 3$ are $0^2=0$ and $1^2=1$. Checking all sums: $0+0=0$, $0+1=1$, $1+1=2$. None equal $3$, so $3$ cannot be written as a sum of two squares. This disproves the statement.

---

## Constructive Proof of Existence

To show that a "there exists" statement is true, we can give a specific example of an element in the domain, or a set of directions to construct one, that has the required properties.

**Example 3.**

**(a)** "There are integers $c$ and $d$ such that $3c + 5d = 1$."

*Proof.* Let $c = 2$ and $d = -1$. These are integers, and $3(2) + 5(-1) = 6 - 5 = 1$. Thus such integers exist. $\blacksquare$

**(b)** "There is an integer $n$ such that $2n - 1$ is prime."

*Proof.* Let $n = 2$. Then $2n - 1 = 2(2) - 1 = 3$, and $3$ is prime. Thus such an integer exists. $\blacksquare$

---

## Proof by Contradiction

To prove a statement $A$ is true:
1. Assume that $\neg A$ is true.
2. If this leads to a false statement (a contradiction), then $\neg A$ is false. Thus, $A$ must be true.

**Example 4.** Prove: $A$: "There is no largest integer."

1. Assume $\neg A$: "There is a largest integer."
2. Denote this largest integer by $N$. Then $N \geq m$ for all integers $m$.

   Consider **$N + 1$**, which is also an integer because it is the sum of two integers.

   Then **$N + 1 > N$**, which contradicts our assumption that $N \geq m$ for all integers $m$ (taking $m = N+1$).

   Thus $\neg A$ is false, so $A$ is true. $\blacksquare$
