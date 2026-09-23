# Sec. 3.1 — Sets and Subsets

## Definition 1

- A **set** is a collection of objects.
- The objects in a set are called **elements** or **members** of the set.

### Notation

- **Roster notation:** $A = \{3, 1, 2\}$, $B = \{\text{ice cream, coffee, donut}\}$, $C = \{1, 2, 3, 3\}$, $D = \{x, y, \{1\}\}$.
- **Set builder notation:** $\{x : P(x)\}$ — "the set of all $x$ such that $P(x)$ is true," or $\{(\text{expression}) : (\text{expression}) \text{ has some properties}\}$.
- **"$\in$"**: means **"is an element of."**
- **"$\notin$"**: means **"is not an element of."**

### Common Mathematical Sets

| Set                | Notation                                                                    | Description                                              |
| ------------------ | --------------------------------------------------------------------------- | -------------------------------------------------------- |
| Natural numbers    | $\mathbb{N} = \{0, 1, 2, 3, \dots\}$                                        | Non-negative integers                                    |
| Integers           | $\mathbb{Z} = \{\dots, -2, -1, 0, 1, 2, \dots\}$                            | Whole numbers, positive, negative, or zero               |
| Rational numbers   | $\mathbb{Q} = \left\{\dfrac{a}{b} : a, b \in \mathbb{Z},\ b \neq 0\right\}$ | Numbers expressible as a ratio of integers               |
| Real numbers       | $\mathbb{R}$                                                                | All numbers on the number line (rational and irrational) |
| Complex numbers    | $\mathbb{C} = \{a + bi : a, b \in \mathbb{R},\ i = \sqrt{-1}\}$             | Numbers of the form $a+bi$                               |
| Even integers      | $\{2k : k \in \mathbb{Z}\} = \{\dots, -4, -2, 0, 2, 4, \dots\}$             | Integers divisible by 2                                  |
| Odd integers       | $\{2k+1 : k \in \mathbb{Z}\} = \{\dots, -3, -1, 1, 3, \dots\}$              | Integers not divisible by 2                              |
| Irrational numbers | $\mathbb{R} \setminus \mathbb{Q}$                                           | Real numbers that are **not** rational                   |

### Relationship of $\mathbb{C}, \mathbb{N}, \mathbb{Q}, \mathbb{R}, \mathbb{Z}$

$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$$

We will define the "$\subset$" symbol (proper subset) on the next page.

**Exercise — show that each "$\neq$" is true (find examples!):**
- $\mathbb{N} \neq \mathbb{Z}$: e.g., $-1 \in \mathbb{Z}$ but $-1 \notin \mathbb{N}$.
- $\mathbb{Z} \neq \mathbb{Q}$: e.g., $\dfrac{1}{2} \in \mathbb{Q}$ but $\dfrac{1}{2} \notin \mathbb{Z}$.
- $\mathbb{Q} \neq \mathbb{R}$: e.g., $\sqrt{2} \in \mathbb{R}$ but $\sqrt{2} \notin \mathbb{Q}$.
- $\mathbb{R} \neq \mathbb{C}$: e.g., $i \in \mathbb{C}$ but $i \notin \mathbb{R}$.

---

## Definition 2

- The set with no elements is called the **empty set** (or **null set**), denoted by $\emptyset$ or $\{\}$.
- The **universal set**, denoted by $U$, is a set that contains all elements mentioned in a particular context.

---

## Definition 3

Let $A$ be a set.

- $A$ is **finite** if either
  (a) $A = \emptyset$, or
  (b) elements in $A$ can be numbered $1$ through $n$ for some positive integer $n$.

- The **cardinality** of finite set $A$, written $|A|$, is
  (a) $|A| = 0$, if $A = \emptyset$.
  (b) $|A| = n$, if elements in $A$ can be numbered $1$ through $n$ for some positive integer $n$.

- $A$ is **infinite** if it is not finite.

---

## Example 1 — Roster notation, set builder notation, and cardinality

- $A = \{x \in \mathbb{R} : x^2 - 3x = 0\} = \{0, 3\}$, so $|A| = 2$.
  *(Solve $x^2-3x=0 \Rightarrow x(x-3)=0 \Rightarrow x=0 \text{ or } x=3$.)*

- $B = \{r \in \mathbb{Q} : r^2 = 2\} = \emptyset$, so $|B| = 0$.
  *(No rational number squares to $2$ — $\sqrt{2}$ is irrational.)*

- $C = \{4, 8, 12, 16, 20, \dots\} = \{x \in \mathbb{Z}^+ : 4 \mid x\} = \{4k : k \in \mathbb{Z}^+\}$.
  *($C$ is **infinite**.)*

---

## Definition 4

Two sets $A$ and $B$ are **equal**, written $A = B$, if and only if they have exactly the same elements.

**Note:** This includes the case that neither set contains any element (i.e., $\emptyset = \emptyset$).

---

## Definition 5

Let $A$ and $B$ be two sets.

- $A$ is a **subset** of $B$, written $A \subseteq B$, if and only if every element of $A$ is also an element of $B$.
  More precisely (useful in proofs!): $A \subseteq B$ if and only if $\forall x,\ (x \in A \rightarrow x \in B)$.

- If $A \subseteq B$ but $A \neq B$, then $A$ is a **proper subset** of $B$, written $A \subset B$.

- **Alternative definition of $A = B$** (useful in proofs!): $A = B$ if and only if $A \subseteq B$ **and** $B \subseteq A$.

- **Does the order of the list, or the number of times an element is listed, affect the set?**
  **No.** $\{1,2,3\} = \{3,2,1\} = \{1,1,2,3,3\}$ — sets are unordered and have no duplicate elements.

- **Does adding or removing any brackets affect the set?**
  **Yes.** $\{1,2\}$ and $\{\{1,2\}\}$ are different sets — the latter has exactly **one** element (the set $\{1,2\}$ itself), not two.

---

## Example 2 — The following statements are true

1. $a \in \{a, b, \{c\}\}$
2. $b \in \{a, b, \{c\}\}$
3. $c \notin \{a, b, \{c\}\}$ *(the element listed is the **set** $\{c\}$, not $c$ itself)*
4. $\{c\} \in \{a, b, \{c\}\}$
5. $\{a, \{c\}\} \subseteq \{a, b, \{c\}\}$
6. $\{a, \{c\}\} \subset \{a, b, \{c\}\}$ *(proper, since $b$ is in the bigger set but not the smaller one)*
7. $\{a, b, c\} \not\subseteq \{a, b, \{c\}\}$ *(since $c$ itself is not an element of the right-hand set — only $\{c\}$ is)*

---

## Example 3 — Which symbol(s) can be used?

|                                         | $\subseteq$ or $\not\subseteq$? | $\subset$? | $\in$ or $\notin$? |
| --------------------------------------- | ------------------------------- | ---------- | ------------------ |
| $\{1,2\}$ ___ $\{1,2,3,\{1,2,3\}\}$     | $\subseteq$                     | $\subset$  | $\notin$           |
| $\{\{1,2\}\}$ ___ $\{1,2,3,\{1,2,3\}\}$ | $\not\subseteq$                 | —          | $\notin$           |
| $\{1,2\}$ ___ $\{1,2,\{1,2\}\}$         | $\subseteq$                     | $\subset$  | $\in$              |
| $\{\{1,2\}\}$ ___ $\{1,2,\{1,2\}\}$     | $\subseteq$                     | $\subset$  | $\notin$           |

**Reasoning:**
- **Row 1:** Both $1,2$ are elements of the right set, so $\{1,2\} \subseteq$ (and $\subset$, since not equal) the right set. But $\{1,2\}$ itself is not listed as an element of the right set (only $\{1,2,3\}$ is), so $\{1,2\} \notin$ right set.
- **Row 2:** For $\{\{1,2\}\} \subseteq$ right set, we'd need its only element $\{1,2\}$ to be an element of the right set — but it isn't (only $\{1,2,3\}$ is), so $\not\subseteq$. Likewise $\{\{1,2\}\}$ is not itself listed as an element, so $\notin$.
- **Row 3:** $1, 2 \in$ right set, so $\{1,2\} \subseteq$ (and $\subset$). Also, $\{1,2\}$ **is** explicitly listed as an element of the right set, so $\{1,2\} \in$ right set too.
- **Row 4:** The only element of $\{\{1,2\}\}$ is $\{1,2\}$, which **is** an element of the right set, so $\{\{1,2\}\} \subseteq$ (and $\subset$). But $\{\{1,2\}\}$ itself is not listed as an element of the right set (only $1, 2, \{1,2\}$ are), so $\notin$.

---

## Theorem

For any set $A$, $\quad \emptyset \subseteq A \quad$ and $\quad A \subseteq A$.

---

## Summary — Fill in the Blanks

- A set is a collection of objects. The objects are called **elements** or **members** of the set.
- If $A = \{1, 2, 3\}$, then $1 \in A$, and $4 \notin A$.
- The symbol $\emptyset$ denotes **the empty set (the set with no elements)**.
- The cardinality of a finite set $A$, written $|A|$, is **the number of elements in $A$**.
- $A$ is a subset of $B$, written $A \subseteq B$, if and only if **every element of $A$ is also an element of $B$**.
- $A$ is a proper subset of $B$, written $A \subset B$, if and only if **$A \subseteq B$ and $A \neq B$**.
- Sets $A$ and $B$ are equal if and only if $A \subseteq B$ and $B \subseteq A$.
- For any set $A$, $\emptyset \subseteq A$ and $A \subseteq A$.
- Fill in the blanks with $\mathbb{C}, \mathbb{N}, \mathbb{Q}, \mathbb{R}, \mathbb{Z}$: $\ \mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$.
