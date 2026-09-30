# Sec. 3.4 — More Set Operations

## Definitions

Let $A$ and $B$ be two sets.

- The **set difference** of $A$ and $B$, written $A - B$, is the set of elements of $A$ that are **not** in $B$.
$$A - B = \{x : x \in A \ \wedge\ x \notin B\}$$

  **Venn diagram:** Two overlapping circles $A$ and $B$ — shade only the part of circle $A$ that does **not** overlap with $B$.

- The **complement** of $A$, written $\overline{A}$ (or $A^c$), is the set $\overline{A} = \{x \in U : x \notin A\}$, where $U$ is a universal set made clear by the context.

  **Venn diagram:** A circle $A$ inside a rectangle representing $U$ — shade everything in the rectangle **except** the circle.

- **Note:** $A - B = A \cap \overline{B}$, $\qquad \overline{A} = U - A$.

---

## Example 1

- If $A = \{1,2,3,4,5\}$, $B = \{3,5,7,9\}$, then
  $$A - B = \{1,2,4\}, \qquad B - A = \{7,9\}$$

- If $U = \{1,2,3,4,5,6,7,8\}$, $A = \{2,4,6,8\}$, then
  $$\overline{A} = \{1,3,5,7\}$$

- If $U = \mathbb{R}$, $A = (-\infty, 1) \cup (1, 3]$, then
  $$\overline{A} = \{1\} \cup (3, \infty)$$
  *(The only real numbers **not** in $A$ are exactly $1$ itself, and everything greater than $3$.)*

---

## Definition — Symmetric Difference

Let $A$ and $B$ be two sets. The **symmetric difference** of $A$ and $B$, written $A \oplus B$, is the set of elements that are in $A$ or $B$, but **not in both**.
$$A \oplus B = \{x : (x \in A \ \vee\ x \in B) \wedge \neg(x \in A \wedge x \in B)\}$$

**Venn diagram:** Two overlapping circles — shade **both** non-overlapping crescent regions (the part of $A$ outside $B$, and the part of $B$ outside $A$), but leave the middle overlap **unshaded**.

**Other ways to express $A \oplus B$:**
$$A \oplus B = (A - B) \cup (B - A) = (A \cup B) - (A \cap B) = (A \cap \overline{B}) \cup (\overline{A} \cap B)$$

---

## Example 2

$$\{a,b,c\} \oplus \{x,y,a\} = \{b, c, x, y\}$$

*(Union is $\{a,b,c,x,y\}$; intersection is $\{a\}$; removing the intersection from the union leaves $\{b,c,x,y\}$.)*

---

## De Morgan's Law for Sets

$$\overline{A \cup B} = \overline{A} \cap \overline{B}, \qquad \overline{A \cap B} = \overline{A} \cup \overline{B}$$

*(Same structure as De Morgan's law for logic in Sec. 1.8 — complementing a union of sets is like negating an "or," and complementing an intersection is like negating an "and.")*

---

## Exercise 3

Let $U = \mathbb{Z}$ be the universal set. Define:
$$A = \{-3,-1,0,1,2,3,4,9,10\}, \qquad B = \{0,-1,-2,-3\}$$
$$C = \{-3,0,1,3,5,6\}, \qquad D = \{x \in \mathbb{Z}^+ : x < 7\} = \{1,2,3,4,5,6\}$$
$$E = \{x \in \mathbb{Z} : x \text{ is even}\}$$

**(a) $(A - C) \cup B$**

$A - C$: remove from $A$ any element also in $C$ ($-3, 0, 1, 3$ are removed):
$$A - C = \{-1, 2, 4, 9, 10\}$$
$$(A-C) \cup B = \{-1,2,4,9,10\} \cup \{0,-1,-2,-3\} = \{-3,-2,-1,0,2,4,9,10\}$$

**(b) $A \oplus D$**

$A \cup D = \{-3,-1,0,1,2,3,4,5,6,9,10\}$, $\quad A \cap D = \{1,2,3,4\}$
$$A \oplus D = (A \cup D) - (A \cap D) = \{-3,-1,0,5,6,9,10\}$$

**(c) $A \oplus B \oplus C$** *(compute left to right: $(A \oplus B) \oplus C$)*

First, $A \oplus B$: $A \cup B = \{-3,-2,-1,0,1,2,3,4,9,10\}$, $A \cap B = \{-3,-1,0\}$
$$A \oplus B = \{-2,1,2,3,4,9,10\}$$

Then, $(A \oplus B) \oplus C$: $(A\oplus B) \cup C = \{-3,-2,0,1,2,3,4,5,6,9,10\}$, $(A\oplus B) \cap C = \{1,3\}$
$$A \oplus B \oplus C = \{-3,-2,0,2,4,5,6,9,10\}$$

**(d) $(A \cap B) - E$**

$A \cap B = \{-3,-1,0\}$. Removing the even element ($0$) leaves:
$$(A \cap B) - E = \{-3, -1\}$$

**(e) $(C \cap A) \cap B$**

$C \cap A = \{-3, 0, 1, 3\}$
$$(C \cap A) \cap B = \{-3,0,1,3\} \cap \{0,-1,-2,-3\} = \{-3, 0\}$$

---

## Summary for Sec. 3.3 and 3.4

*(Using $A = \{1,2\}$, $B = \{2,3\}$, $U = \{1,2,3,4\}$ for the "Example" column.)*

| Symbol | Name | Definition | Venn Diagram | Example |
|---|---|---|---|---|
| $A \cup B$ | Union | $x \in A \cup B \leftrightarrow x \in A \vee x \in B$ | Shade all of both circles | $A \cup B = \{1,2,3\}$ |
| $A \cap B$ | Intersection | $x \in A \cap B \leftrightarrow x \in A \wedge x \in B$ | Shade only the overlap | $A \cap B = \{2\}$ |
| $A - B$ | Set difference | $x \in A - B \leftrightarrow x \in A \wedge x \notin B$ | Shade $A$, excluding overlap | $A - B = \{1\}$ |
| $\overline{A}$ | Complement | $\forall x \in U,\ x \in \overline{A} \leftrightarrow x \notin A$ | Shade all of $U$ outside $A$ | $\overline{A} = \{3,4\}$ |
| $A \oplus B$ | Symmetric difference | $x \in A \oplus B \leftrightarrow (x\in A \vee x\in B) \wedge \neg(x\in A \wedge x\in B)$ | Shade both crescents, not the overlap | $A \oplus B = \{1,3\}$ |

**Associativity:**
$$(A_1 \cup A_2) \cup A_3 = A_1 \cup (A_2 \cup A_3), \qquad (A_1 \cap A_2) \cap A_3 = A_1 \cap (A_2 \cap A_3)$$

**Distributivity:**
$$A \cap (B \cup C) = (A \cap B) \cup (A \cap C), \qquad A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$$

**De Morgan's Law:**
$$\overline{A \cup B} = \overline{A} \cap \overline{B}, \qquad \overline{A \cap B} = \overline{A} \cup \overline{B}$$
