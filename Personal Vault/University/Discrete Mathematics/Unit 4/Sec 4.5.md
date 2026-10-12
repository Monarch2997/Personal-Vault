---
Note: Human
tags:
  - Unit-4
---
#### Definition: Let f: A->B and g: B->C. Then the Composition of g with f is the function:
[[Drawing 2026-10-12 09.12.21.excalidraw]]
note: For GoF to exist, we must have **range(f) <= Domain(g)**

#### Example 1: 
let A={1,2,3}, B={x,y}, C={a,b}. Define f: A->B by  f={(1,x), (2,x), (3,y)}
g: B->C by g={(x,b),(y,a)}   
GoF(1) = g(x) = b
GoF(2) = g(x) = b
GoF(3) = g(y) = a
*GoF inroste notation*
GoF{(1,b),(2,b),(3,a)} <= A x C

#### Example 2:
Define f: $R$ -> $R$ by f(x) = 2x-3, and g: $R$ - {1} -> $R$ by g(x) = x/(x-1)
(GoF)(x) = g(2x-3) = (2x-3)/(2x-3-1) = (2x-3)/(2x-4)
FoG(x) = f(x/(x-1)) = 2(x/(x-1))-3 = 2x/(x-1) -3
*Notes:*
GoF(x)
	$$GoF(2) =\frac{2(2) -3}{2(2) -4} = \frac{1}{0} = DNE$$
*Not well-defined*
$$FoG(x) = \frac{2x}{x-1} - 3 $$
is well-defined

#### Definition:
Let A be a set, the identity function on A is the function: 
$$I_A: A->A  $$
X element is going to X or in other words: X->X
All of this or:
$$\forall x \in A, I_A(x) =x$$
The identity function works like "I" for functions. If f: A->B, then $$FoI_A = f)$$
$$I_AoF = f$$
*Theorem 3,* if f: A->B, g: B->A, then f and g are inverses if and only if: $$GoF = I_A$$
$$GoF(x)=x$$
and
$$FoG=I_B$$ $$FoG(y) = y$$[[Drawing 2026-10-12 09.33.27.excalidraw]]

*Theorem 4:* Composition of functions is an associative operation
(FoG)oH = Fo(GoH) * NOT commutative FoG /= GoF
[[Drawing 2026-10-12 09.39.45.excalidraw]]