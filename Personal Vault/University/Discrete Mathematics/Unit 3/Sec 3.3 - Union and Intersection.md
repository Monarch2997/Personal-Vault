# Sec. 3.3 — Union and Intersection

## Definitions

Let $A$ and $B$ be two sets.

- The **union** of $A$ and $B$, written $A \cup B$, is the set of elements in $A$ **or** $B$.
$$A \cup B = \{x : x \in A \ \vee\ x \in B\}$$

  **Venn diagram:** Two overlapping circles labeled $A$ and $B$ — the **entire shaded region covers both circles** (everything inside $A$, inside $B$, or inside both).

- The **intersection** of $A$ and $B$, written $A \cap B$, is the set of elements in $A$ **and** $B$.
$$A \cap B = \{x : x \in A \ \wedge\ x \in B\}$$

  **Venn diagram:** Two overlapping circles labeled $A$ and $B$ — **only the overlapping "lens" region in the middle** is shaded (elements in both circles at once).

---

## Example 1

Let $A = \{a, b, c\}$ and $B = \{a, x, y, b\}$. Then:

1. $A \cup B = \{a, b, c, x, y\}$
2. $A \cap B = \{a, b\}$

---

## Example 2

For any set $A$:
$$A \cup \emptyset = A, \qquad A \cap \emptyset = \emptyset$$

*(Union with the empty set adds nothing new; intersection with the empty set has nothing in common.)*

---

## Exercise 3

Let
$$A = \{x \in \mathbb{Z} : 3 \mid x\}, \qquad B = \{x \in \mathbb{Z} : 5 \mid x\}$$
$$C = \{-30, -4, 0, 1, 5, 9\}, \qquad D = \{-10, -6, 1, 4, 9, 15\}$$

- **$A \cap C$** — elements of $C$ divisible by 3: $-30 = 3(-10)$ ✓, $-4$ ✗, $0 = 3(0)$ ✓, $1$ ✗, $5$ ✗, $9 = 3(3)$ ✓
  $$A \cap C = \{-30, 0, 9\}$$

- **$C \cup D$** — combine all elements, no duplicates:
  $$C \cup D = \{-30, -10, -6, -4, 0, 1, 4, 5, 9, 15\}$$

- **$A \cap B$** — integers divisible by both 3 and 5, i.e., divisible by 15:
  $$A \cap B = \{x \in \mathbb{Z} : 15 \mid x\}$$

- **$B \cap (C \cup D)$** — elements of $C \cup D$ divisible by 5: $-30$ ✓, $-10$ ✓, $-6$ ✗, $-4$ ✗, $0$ ✓, $1$ ✗, $4$ ✗, $5$ ✓, $9$ ✗, $15$ ✓
  $$B \cap (C \cup D) = \{-30, -10, 0, 5, 15\}$$

---

## Properties of Union and Intersection

### Associativity

- $(A_1 \cup A_2) \cup A_3 = A_1 \cup (A_2 \cup A_3)$
- $A_1 \cup A_2 \cup A_3 \cup \cdots \cup A_n = \{x : x \in A_i \text{ for at least one } i \in \{1, \dots, n\}\}$
- $(A_1 \cap A_2) \cap A_3 = A_1 \cap (A_2 \cap A_3)$
- $A_1 \cap A_2 \cap A_3 \cap \cdots \cap A_n = \{x : x \in A_i \text{ for every } i \in \{1, \dots, n\}\}$

*(Because union and intersection are associative, the grouping/parentheses don't matter, so we can drop them and write a long chain of unions or intersections without ambiguity.)*

### Distributivity

- $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$
- $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$

---

## Example 4

For $i \in \mathbb{Z}^+$, define:
$$A_i = \{i^0, i^1, i^2\}, \qquad B_i = \{x \in \mathbb{R} : -i \leq x \leq 1/i\}, \qquad C_i = \{x \in \mathbb{R} : -1/i \leq x \leq 1/i\}$$

**1. $\displaystyle\bigcap_{i=2}^{5} A_i$**

$A_2 = \{1,2,4\}$, $A_3 = \{1,3,9\}$, $A_4 = \{1,4,16\}$, $A_5 = \{1,5,25\}$. The only value common to all four sets is $1$.
$$\bigcap_{i=2}^{5} A_i = \{1\}$$

**2. $\displaystyle\bigcap_{i=1}^{100} B_i$**

Each $B_i = [-i,\ 1/i]$. As $i$ increases, the left endpoint $-i$ moves further left (less restrictive), while the right endpoint $1/i$ shrinks toward $0$ (more restrictive). The intersection is bounded by the **most restrictive** endpoints: the largest left endpoint occurs at $i=1$ ($-1$), and the smallest right endpoint occurs at $i=100$ ($1/100$).
$$\bigcap_{i=1}^{100} B_i = [-1,\ 1/100]$$

**3. $\displaystyle\bigcup_{i=1}^{100} C_i$**

Each $C_i = [-1/i,\ 1/i]$. As $i$ increases, this interval shrinks toward $\{0\}$; the **largest** interval occurs at $i=1$: $C_1 = [-1, 1]$. Since $C_i \subseteq C_1$ for all $i = 1, \dots, 100$, the union is just the largest one.
$$\bigcup_{i=1}^{100} C_i = [-1, 1]$$

---

## Example 5 — False Equalities: Venn Diagrams and Counterexamples

### $A \cap (B \cup C) = (A \cap B) \cup C$   — **FALSE**

**Left side, $A \cap (B \cup C)$:** In a three-circle Venn diagram ($A$, $B$, $C$), shade the region inside $A$ **and** inside ($B$ or $C$) — this shades only the parts of $A$ that overlap with $B$ or with $C$ (i.e., the $A\cap B$-only region, the $A\cap C$-only region, and the $A\cap B\cap C$ region).

**Right side, $(A \cap B) \cup C$:** Shade the region inside both $A$ and $B$, **together with the entire circle $C$** (all of $C$, whether or not it overlaps $A$ or $B$).

These shaded regions differ — the right side always includes all of $C$ (even the part of $C$ outside $A$), while the left side never includes any part of $C$ that's outside $A$.

**Counterexample:** Let $A = \{1,2\}$, $B = \{2,3\}$, $C = \{4\}$.
- Left: $B \cup C = \{2,3,4\}$, so $A \cap (B \cup C) = \{1,2\} \cap \{2,3,4\} = \{2\}$.
- Right: $A \cap B = \{2\}$, so $(A \cap B) \cup C = \{2\} \cup \{4\} = \{2,4\}$.

Since $\{2\} \neq \{2,4\}$, the equality fails. $\blacksquare$

### $A \cup (B \cap C) = (A \cup B) \cap C$   — **FALSE**

**Left side, $A \cup (B \cap C)$:** Shade **all of $A$**, together with the region where $B$ and $C$ overlap.

**Right side, $(A \cup B) \cap C$:** Shade the region that is inside $C$ **and** inside ($A$ or $B$) — this restricts everything to being inside $C$, including all of $A \cap C$.

These differ — the left side always includes all of $A$ (even the part of $A$ outside $C$), while the right side never includes any part of $A$ that's outside $C$.

**Counterexample:** Let $A = \{1\}$, $B = \{2\}$, $C = \{3\}$.
- Left: $B \cap C = \emptyset$, so $A \cup (B \cap C) = \{1\} \cup \emptyset = \{1\}$.
- Right: $A \cup B = \{1,2\}$, so $(A \cup B) \cap C = \{1,2\} \cap \{3\} = \emptyset$.

Since $\{1\} \neq \emptyset$, the equality fails. $\blacksquare$
