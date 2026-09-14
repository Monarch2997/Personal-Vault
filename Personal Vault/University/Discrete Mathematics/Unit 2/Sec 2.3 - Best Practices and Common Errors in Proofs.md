# Sec. 2.3 — Best Practices and Common Errors in Proofs

> See zyBook Figure 2.3.1 for allowed assumptions in proofs.
> See zyBook Figure 2.3.2 for common keywords and phrases in proofs.

## Best Practices in Writing Proofs

**1. Indicate when the proof starts and ends.**
- Start with: **"Proof."**
- End with: **$\blacksquare$** (a QED box/symbol) or a closing phrase like "This completes the proof."

**2. Write proofs in complete sentences.**

*Example of a poorly-written proof* for "The sum of two odd integers is an even integer":

> Proof. $x, y \rightarrow$ odd
> $x = 2k+1$
> $y = 2j+1$
> $\rightarrow x+y = 2k+1+2j+1 = 2(\underbrace{k+j+1}_{\text{integer}})$.

This is just symbols strung together — no sentences explaining the logic.

**3. Give the reader a roadmap** of what has been shown, what is assumed, and where the proof is going.
- Start with stating the assumptions and what is to be proved.
- To use a fact that has not yet been proved, write: **"We claim that . . ."**, **"Claim: . . ."**, and prove it later in the proof.

**4. Introduce each variable when it is first used.**
- "Let $x$ be an even integer."
- "Since $x$ is even, $x = 2k$ for some integer $k$."

**5. Introduce blocks of equations with English text**, and justify each step that doesn't follow purely from algebra.
- "Then $x + y = \dots$"
- "Substituting $x = 2k$ into $x^2$ gives $\dots$"
- "Squaring both sides of the equation yields $\left(\sqrt{2}\right)^2 = \left(\dfrac{a}{b}\right)^2 \Rightarrow 2 = \dfrac{a^2}{b^2}$."

**6. Check if everything in the hypothesis is actually used!**
A "good" theorem should not have a redundant hypothesis that is not used in its proof. If there is anything in the hypothesis that is not used in your proof, chances are there is a mistake in the proof, or the theorem's statement can be improved.

*Example of a redundant hypothesis:* "The product of an odd integer and an even integer is even." (The oddness of the first integer is never needed — the evenness of the second alone guarantees the product is even.)

---

## Common Mistakes in Proofs

(a) Generalizing from examples
(b) Skipping steps
(c) Circular reasoning
(d) Assuming facts that have not yet been proven
(e) Invalid uses of existential instantiation (bad variable names)

---

## Example 1 — Find the Mistakes

### (1) "If $n^3$ is even, then $n$ is even."

> *Proof.* We shall prove the contrapositive: "If $n$ is odd, then $n^3$ is odd."
> Assume $n$ is odd. Since $n$ is odd, $n = 2k+1$ for some integer $k$.
> Plugging in gives $n^3 = (2k+1)^3$.
> Therefore, $n^3$ is odd.

**Mistake: (b) Skipping steps.** The proof jumps from $n^3 = (2k+1)^3$ straight to "therefore $n^3$ is odd" without expanding and showing the result has the form $2m+1$.

**Fix:** Expand: $(2k+1)^3 = 8k^3+12k^2+6k+1 = 2(4k^3+6k^2+3k)+1$. Since $4k^3+6k^2+3k$ is an integer, $n^3$ is odd.

### (2) "The sum of two odd integers is even."

> *Proof.* Assume $x$ and $y$ are odd. Since $x$ is odd, $x = 2k+1$. Since $y$ is odd, $y = 2k+1$. Then $x+y = 4k+2 = 2(2k+1)$...

**Mistake: (e) Invalid existential instantiation (bad variable names).** Using the *same* variable $k$ for both $x$ and $y$ forces $x = y$, which isn't given — $x$ and $y$ are two independent odd integers.

**Fix:** Use different variables: $x = 2k+1$ for some integer $k$, and $y = 2j+1$ for some (possibly different) integer $j$. Then $x+y = 2k+2j+2 = 2(k+j+1)$, which is even since $k+j+1$ is an integer.

### (3) "Every nonzero integer $n$ divides 0."

> *Proof.* Let $n$ be a nonzero integer. If $n = 5$, then $0 = 0 \times 5$, so $5$ divides $0$. Therefore, every nonzero integer $n$ divides $0$.

**Mistake: (a) Generalizing from examples.** The proof only checks the single case $n=5$ and then claims the result for *all* nonzero integers — a universal statement can't be proven by checking one example.

**Fix:** Let $n$ be any nonzero integer. Then $0 = 0 \times n$, and since $0$ is an integer, $n \mid 0$ by definition — this holds for the *general* $n$, not just $n=5$.

### (4) "The square of an even integer is even."

> *Proof.* Assume $x$ is even, so $x = 2k$. Since the product of two even integers is even, $x^2 = x \cdot x$ is even.

**Mistake: (d) Assuming facts that have not yet been proven** (closely related to (c) circular reasoning). The proof relies on the unproven fact "the product of two even integers is even" — a claim that is essentially of the same difficulty as (or built on the same idea as) what's being proven, and hasn't been established.

**Fix:** Work directly from the definition: $x^2 = (2k)^2 = 4k^2 = 2(2k^2)$. Since $2k^2$ is an integer, $x^2$ is even.

### (5) "The square of an odd integer is odd."

> *Proof.* Assume $x$ is odd, and $y = x^2$ is odd. Since $y$ is odd, $y = 2k+1$. Since $x^2 = y = 2k+1$, $x^2$ is odd.

**Mistake: (c) Circular reasoning.** The proof *assumes* $y = x^2$ is odd — but that is exactly the conclusion we're trying to prove! It assumes the very thing it sets out to show.

**Fix:** Start only from $x$ odd: $x = 2k+1$ for some integer $k$. Then $x^2 = (2k+1)^2 = 4k^2+4k+1 = 2(2k^2+2k)+1$. Since $2k^2+2k$ is an integer, $x^2$ is odd.
