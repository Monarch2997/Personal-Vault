# Sec. 3.6 — Cartesian Products

## Definition

- An **ordered pair** of items is written $(a, b)$.

- The **Cartesian product** of two sets $A$ and $B$ is the set:
$$A \times B = \{(a,b) : a \in A,\ b \in B\}$$

- $(a_1, b_1) = (a_2, b_2) \ \leftrightarrow\ a_1 = a_2 \ \wedge\ b_1 = b_2$
  *(Two ordered pairs are equal exactly when their corresponding entries match — unlike sets, **order matters** and duplicates aren't collapsed.)*

- In general:
$$A_1 \times A_2 \times \cdots \times A_n = \{(a_1, a_2, \dots, a_n) : a_i \in A_i \text{ for each } i = 1, \dots, n\}$$

---

## Example 1

Let $A = \mathbb{R}$. Then:
$$A \times A = \mathbb{R} \times \mathbb{R} = \{(x,y) : x, y \in \mathbb{R}\} = \mathbb{R}^2$$
*(This is the familiar Cartesian plane.)*

---

## Example 2

Let $A = \{a, b\}$, $B = \{x, y, z\}$.

**1. $A \times B$**
$$A \times B = \{(a,x), (a,y), (a,z), (b,x), (b,y), (b,z)\}$$

**2. $B \times A$**
$$B \times A = \{(x,a), (x,b), (y,a), (y,b), (z,a), (z,b)\}$$

*(Note $A \times B \neq B \times A$ in general — the Cartesian product is **not commutative**, since $(a,x) \neq (x,a)$.)*

---

## Exercise 3

Let $A = \{1,2\}$, $B = \{2,3\}$, $C = \{+, \$\}$.

**1. $(A \cap B) \times C$**

$A \cap B = \{2\}$, so:
$$(A \cap B) \times C = \{(2,+), (2,\$)\}$$

**2. $B \times C \times A$**
$$B \times C \times A = \big\{\ (2,+,1),\ (2,+,2),\ (2,\$,1),\ (2,\$,2),\ (3,+,1),\ (3,+,2),\ (3,\$,1),\ (3,\$,2)\ \big\}$$

---

## Definition — Strings

- A **sequence of characters** is called a **string**.
- **String notation:** If $A$ is a set of symbols or characters, the elements in $A^n$ can be written **without** the usual punctuation (no parentheses, no commas) — e.g., the tuple $(0,1)$ is written simply as $01$.

---

## Example 4

Let $A = \{0, 1\}$. Then $A^2 = \ ?$

- **Using $n$-tuples notation:** $A^2 = \{(0,0), (0,1), (1,0), (1,1)\}$
- **Using string notation:** $A^2 = \{00, 01, 10, 11\}$

---

## Definition — Empty String and Concatenation

- The **empty string** is the unique string whose length is **$0$**, denoted by $\lambda$ (or $\varepsilon$).
- If $s$ and $t$ are two strings, then the **concatenation** of $s$ and $t$ (denoted $st$) is the string obtained by putting $s$ and $t$ together, one after the other.

---

## Example 5

Let $s = 01$, $t = 101$. Then:

- $st = 01101$ *(write $s$ then $t$ back-to-back)*
- $t^1 = t = 101$ *(concatenating $t$ with itself just once gives back $t$ — same idea as $x^1 = x$)*
- $\lambda s = s = 01$ *(the empty string is the identity for concatenation — attaching "nothing" in front leaves $s$ unchanged)*

---

## Exercise 6 — Give an element of each set in string notation

**$\{xy : x \in \{0,1\}^2,\ y \in \{a,b,c\}^3\}$**

Here $x$ is any length-2 string over $\{0,1\}$, and $y$ is any length-3 string over $\{a,b,c\}$; $xy$ concatenates them. One valid element:
$$x = 01,\quad y = abc \quad \Rightarrow \quad xy = \texttt{01abc}$$

**$\{10t : t \in \{a,b\} \cup \{a,b\}^2 \cup \{a,b\}^3\}$**

Here $t$ can be any string of length $1$, $2$, **or** $3$ over $\{a,b\}$, prefixed with $10$. One valid element (taking $t = ab$, a length-2 string):
$$t = ab \quad \Rightarrow \quad 10t = \texttt{10ab}$$

*(Other valid choices exist too — e.g., $t = a$ gives $\texttt{10a}$, or $t = aab$ gives $\texttt{10aab}$.)*

---

## Summary — Fill in the Blanks

- $A \times B$ denotes the **Cartesian product** of sets $A$ and $B$.
  Definition in set builder notation:
  $$A \times B = \{(a,b) : a \in A,\ b \in B\}$$

- For example, if $A = \{1,2\}$, $B = \{2,3\}$, then:
  $$A \times B = \{(1,2), (1,3), (2,2), (2,3)\}$$

- $$A_1 \times A_2 \times \cdots \times A_n = \{(a_1, a_2, \dots, a_n) : a_i \in A_i \text{ for each } i\}$$
  The elements in this set are called **ordered $n$-tuples**.

- If $A = \{1,2\}$, $B = \{2,3\}$, express the elements of $A \times B$ in string notation:
  $$A \times B = \{12, 13, 22, 23\}$$

- Let $x = 112$, $y = 212$ be two strings from the set $\{1,2\}^3$, then the concatenation of $x$ and $y$ is:
  $$xy = 112212$$
