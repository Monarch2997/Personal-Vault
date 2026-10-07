---
tags:
  - Unit-4
Note: Human
---
## Definitions:  let A, B be two sets. Let f: A -> B be a 
##### Then f is one-to-one (injective) if and only if different inputs in A map to different outputs in B.

**In symbols:** (useful for proving and disproving)
$\forall$x1, x2 $\in$ A, x1 /= x2 -> f(x1) /= f(x2)
- One-to-one *implies->* |A| <= |B|

*Contrapositive:* (useful for proving)
$\forall$x1, x2 $\in$ A, f(x1) = f(x2) -> x1 = x2 

**A -> B:**

| **A** | -> 1 |
| ----- | ---- |
| B     | -> 2 |
| C     | -> 3 |
| D     | -> 2 |
###### f is Onto(surjective) if and only if range(f) = target(f) i.e. every element in B is an output of f
**In symbols:**
$\forall$y $\in$ B, $\exists$x $\in$ A | (x,y) $\in$ f

$\forall$y $\in$ B, f(x) = y is a solution x $\in$ A

| A   | -> 1 |
| --- | ---- |
| B   | -> 2 |
| C   | -> 3 |
| D   | -> 3 |
Onto *imply->* |A| >= |B|

| A   | -> 1         |
| --- | ------------ |
| B   | -> 2         |
| C   | -> 3<br>-> 4 |
This cannot exist. One input does not equal two outputs. Instead we want:

| A   | -> 1 |
| --- | ---- |
| B   | -> 2 |
| C   | -> 3 |
| D   | -> 4 |
##### f is Bijective if and only if f is both one-to-one and onto
Bijective -> |A| = |B|

## Example 1:

| Section          |                                                                       |                                                                          |                                                         |
| ---------------- | --------------------------------------------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------- |
| domain           | A1 = {1,2,3,4}                                                        | A2 = {1,2,3}                                                             | A3 ={1,2,3}                                             |
| target           | B1 = {x,y,z}                                                          | B2 = {w,x,y,z}                                                           | B3 = {x,y,z}                                            |
| function         | f1 = {(1,x), (2,y),(3,z), (4,y)}                                      | f2 = {(1,w), (2,y), (3,x)}                                               | f3 = {(1,z), (2,y), (3,x)}                              |
| Arrow Diagram    | A1:       B1<br>1    ->   x<br>2   ->   y<br>3   ->   z<br>4   ->   y | A2:       B2<br>1    ->   w<br>2   ->   y<br>3   ->   x<br>            z | A3:       B3<br>1    ->   z<br>2   ->   y<br>3   ->   x |
| one-to-one?      | Not one-to-one, f(2)=f(4)                                             | Yes                                                                      | Yes                                                     |
| onto? (range =?) | Yes, every element in B1 is used                                      | No, Z is unused                                                          | Yes                                                     |
| Bijective?       | No, it is not one-to-one                                              | No, not onto                                                             | Yes                                                     |
## Example 2:
**Let A = $\mathbb{R}$, and f : A → A such that f (x) = 2x −3. Is f one-to-one? Is f onto? Is f bijective?**

**One-to-one:**
Proof: Let x*1*, x*2*  $\in$ A and f(x*1*) = f(x*2*)
Then, 2x*1* -3 = 2x*2* -3
2x*1* = 2x*2*
x*1* = x*2*
f is one-to-one

**Onto:**
Proof: Let y $\in$ $\mathbb{R}$, consider f(x) = y
then 2x-3 = y
2x = y+3
x = (y+3)/2 
since $\mathbb{R}$ are closed over addition and division, and y, 3, and 2 are $\in$ $\mathbb{R}$
then x = (y+3)/2 $\in$ $\mathbb{R}$ , which is in the domain
f is onto

 Since it is onto and one-to-one, then **it is bijective**
## Example 3:
**Let A = $\mathbb{Z}$, and f : A → A such that f (x) = 2x −3. Is f one-to-one? Is f onto? Is f bijective? (Exercise: What if A = $\mathbb{N}$ instead?)**

**One-to-one:**
Proof: Let x*1*, x*2*  $\in$ A and f(x*1*) = f(x*2*)
Then, 2x*1* -3 = 2x*2* -3
2x*1* = 2x*2*
x*1* = x*2*
f is one-to-one

**Onto:**
Proof: Let y $\in$ $\mathbb{Z}$, consider f(x) = y
then 2x-3 = y
2x = y+3
x = (y+3)/2 
since $\mathbb{Z}$ are closed over addition and subtraction
Then y cannot be onto since it is closed by division

 Since it is not onto, then **it is not bijective**

| Concept:                 | One-to-one:                                             | Well Defined                                            |
| ------------------------ | ------------------------------------------------------- | ------------------------------------------------------- |
| To prove<br>*Rigorously* | f(x1) = f(x2) -> x1 = x2<br>*Same output -> Same input* | x1 = x2 -> f(x1) = f(x2)<br>*Same input -> same output* |
| To check<br>*informal*   | Horizontal Line Test<br>Stupid ass drawing              | Vertical Line Test<br>*Stupid ass drawing*              |
