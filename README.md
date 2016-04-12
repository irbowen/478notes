## Branch and Bound
Branching
- Decompose into sequence of subproblems
Bounding
- Compute lower bound on the solution beform attemping to solve the branch, "bound", or prune, if it is above best solution so far


## Multi Level Synthesis

We apply various "transformations" to boolean networks, such as
- decomposition
- substituion
- factoring

with the goal being to find good factored forms

NOTES on factoring, division, here

WEAK DIVISION
Algebraic
boolean


### Kernels
- Kernels provide a way to find common sub-expressions using weak division
- A "cube-free expression" is an algebraic expression of two or more cubes that has no cube factors
  - ac + ad + bc + bd + e is cube free
  - abc + abd is not cube free
  - abc is not cube free
- Cube Division: F/P can be formed by deleting the literals of P from F
- The *primary divisors* of an expression *f* are the set of expressions
  - D(f) = {f/c such that c is a cube}

## Terms

- Algebraic Expression: an expression in which no cube contains another cube
  - a + bc is
  - a + ab is not
- FG is an algebraic product if 
  - F and G have "disjoint" sets, no common variabls
  - F and G are algebraic expressions
  - Otherwise, FG is called a "boolean product"
