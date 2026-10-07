---
tags:
  - Unit-3
Note: Claude
---
# Sec. 3.2 — Set of Sets

We have seen that a set can be an element of another set. For example, $\{x, y, \{1\}\}$.

## Definition — Power Set

The **power set** of a set $A$, denoted by $\mathcal{P}(A)$, is the set of all subset(s) of $A$.

**Using set builder notation:**
$$\mathcal{P}(A) = \{S : S \subseteq A\}$$

---

## Example 1

- If $A = \emptyset$, then $\mathcal{P}(A) = \{\emptyset\}$.
- If $A = \{a\}$, then $\mathcal{P}(A) = \{\emptyset, \{a\}\}$.
- If $A = \{a, b\}$, then $\mathcal{P}(A) = \{\emptyset, \{a\}, \{b\}, \{a,b\}\}$.
- If $A = \{a, b, c\}$, then $\mathcal{P}(A) = \{\emptyset, \{a\}, \{b\}, \{c\}, \{a,b\}, \{a,c\}, \{b,c\}, \{a,b,c\}\}$.

---

## Theorem 2

If $A$ is a finite set with $n$ elements, then $\mathcal{P}(A)$ has $2^n$ elements.

**Reason:** To form a subset of $A$, go through each of the $n$ elements one at a time and decide whether to *include* it or *exclude* it — 2 independent choices per element. By the multiplication principle, there are $\underbrace{2 \times 2 \times \cdots \times 2}_{n \text{ times}} = 2^n$ possible subsets.

---

## Exercise 3

Let $X = \{0, \{1\}, \{x, y\}\}$.

- $|X| = 3$ *(the three elements are $0$, $\{1\}$, and $\{x,y\}$)*

- $\mathcal{P}(X) = \big\{\ \emptyset,\ \{0\},\ \{\{1\}\},\ \{\{x,y\}\},\ \{0,\{1\}\},\ \{0,\{x,y\}\},\ \{\{1\},\{x,y\}\},\ \{0,\{1\},\{x,y\}\}\ \big\}$
  *(there are $2^3 = 8$ subsets total)*

- $\{A \in \mathcal{P}(X) : |A| = 2\} = \big\{\ \{0,\{1\}\},\ \{0,\{x,y\}\},\ \{\{1\},\{x,y\}\}\ \big\}$

- $\{A \in \mathcal{P}(X) : 0 \in A\} = \big\{\ \{0\},\ \{0,\{1\}\},\ \{0,\{x,y\}\},\ \{0,\{1\},\{x,y\}\}\ \big\}$

---

## Exercise 4 — Express using roster notation, then give the cardinality

**1. $\mathcal{P}(\emptyset)$**
$$\mathcal{P}(\emptyset) = \{\emptyset\}, \qquad |\mathcal{P}(\emptyset)| = 1$$

**2. $\mathcal{P}(\mathcal{P}(\emptyset))$**
$$\mathcal{P}(\mathcal{P}(\emptyset)) = \mathcal{P}(\{\emptyset\}) = \{\emptyset, \{\emptyset\}\}, \qquad \left|\mathcal{P}(\mathcal{P}(\emptyset))\right| = 2$$

**3. $\mathcal{P}(\mathcal{P}(\mathcal{P}(\emptyset)))$**
$$\mathcal{P}(\mathcal{P}(\mathcal{P}(\emptyset))) = \mathcal{P}(\{\emptyset, \{\emptyset\}\}) = \big\{\ \emptyset,\ \{\emptyset\},\ \{\{\emptyset\}\},\ \{\emptyset,\{\emptyset\}\}\ \big\}, \qquad \left|\mathcal{P}(\mathcal{P}(\mathcal{P}(\emptyset)))\right| = 4$$

*(Pattern: each time you take the power set, the cardinality doubles: $1 \to 2 \to 4 \to \dots$, consistent with Theorem 2: $|\mathcal{P}(A)| = 2^{|A|}$.)*

---

## Exercise 5 — Determine the truth value

*(For items 13–16, a counterexample is given whenever the statement is false.)*

| # | Statement | Truth Value | Explanation |
|---|---|---|---|
| 1 | $\{a\} \subseteq \{x,y,a\}$ | **True** | The only element of $\{a\}$, namely $a$, is in $\{x,y,a\}$. |
| 2 | $\{a\} \in \{x,y,a\}$ | **False** | The elements of $\{x,y,a\}$ are $x, y, a$ — not the set $\{a\}$. |
| 3 | $\{a\} \subseteq \{x,y,\{a\}\}$ | **False** | We'd need $a \in \{x,y,\{a\}\}$, but the elements there are $x, y, \{a\}$ — not $a$ itself. |
| 4 | $\emptyset \subseteq \emptyset$ | **True** | The empty set is a subset of every set, including itself. |
| 5 | $\emptyset \subseteq \{\emptyset\}$ | **True** | The empty set is a subset of every set. |
| 6 | $\{\emptyset\} \subseteq \{\{\emptyset\}\}$ | **False** | We'd need $\emptyset \in \{\{\emptyset\}\}$, but the only element of $\{\{\emptyset\}\}$ is $\{\emptyset\}$, and $\emptyset \neq \{\emptyset\}$. |
| 7 | $\{\emptyset\} \in \{\emptyset\}$ | **False** | The only element of $\{\emptyset\}$ is $\emptyset$ itself, not $\{\emptyset\}$. |
| 8 | $\emptyset \subseteq \{\{\emptyset\}\}$ | **True** | The empty set is a subset of every set. |
| 9 | $\emptyset \in \{\{\emptyset\}\}$ | **False** | The only element of $\{\{\emptyset\}\}$ is $\{\emptyset\}$, and $\emptyset \neq \{\emptyset\}$. |
| 10 | $\emptyset \subseteq \{x,y,\emptyset\}$ | **True** | The empty set is a subset of every set. |
| 11 | $\emptyset \in \{x,y,\emptyset\}$ | **True** | $\emptyset$ is explicitly listed as an element. |
| 12 | $\{\emptyset\} \subseteq \{x,y,\emptyset\}$ | **True** | The only element of $\{\emptyset\}$, namely $\emptyset$, is listed in $\{x,y,\emptyset\}$. |
| 13 | $(A \subseteq B) \wedge (B \subseteq C) \rightarrow A \subseteq C$ | **True** | This is the **transitivity of $\subseteq$**: if every element of $A$ is in $B$, and every element of $B$ is in $C$, then every element of $A$ is in $C$. Always true — no counterexample exists. |
| 14 | $(A \subseteq B) \wedge (B \in C) \rightarrow A \in C$ | **False** | **Counterexample:** Let $A = \{1\}$, $B = \{1,2\}$, $C = \{\{1,2\}\}$. Then $A \subseteq B$ (true) and $B \in C$ (true, since $\{1,2\}$ is the element of $C$). But $A \in C$? Is $\{1\} \in \{\{1,2\}\}$? No — the only element of $C$ is $\{1,2\}$, not $\{1\}$. So the conclusion fails. |
| 15 | $A \subseteq B \leftrightarrow \mathcal{P}(A) \subseteq \mathcal{P}(B)$ | **True** | ($\rightarrow$) If $A \subseteq B$, every subset of $A$ is also a subset of $B$, so $\mathcal{P}(A) \subseteq \mathcal{P}(B)$. ($\leftarrow$) If $\mathcal{P}(A) \subseteq \mathcal{P}(B)$, then since $A \in \mathcal{P}(A)$ (as $A \subseteq A$), we get $A \in \mathcal{P}(B)$, meaning $A \subseteq B$. Both directions hold, so this is a true theorem. |
| 16 | $A = \emptyset \leftrightarrow \mathcal{P}(A) = \emptyset$ | **False** | **Counterexample:** Let $A = \emptyset$. Then $A = \emptyset$ is true, but $\mathcal{P}(A) = \mathcal{P}(\emptyset) = \{\emptyset\} \neq \emptyset$. In fact, $\mathcal{P}(A)$ is **never** empty for any set $A$, since $\emptyset \in \mathcal{P}(A)$ always. |
