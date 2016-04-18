## Branch and Bound
Branching
- Decompose into sequence of subproblems
Bounding
- Compute lower bound on the solution before attemping to solve the branch, "bound", or prune, if it is above best solution so far


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

unate

- Algebraic Expression: an expression in which no cube contains another cube
  - a + bc is
  - a + ab is not
- FG is an algebraic product if
  - F and G have "disjoint" sets, no common variabls
  - F and G are algebraic expressions
  - Otherwise, FG is called a "boolean product"



### Kernels
- Kernels provide a way to find common sub-expressions using weak division
- A **cube-free expression** is an algebraic expression of two or more cubes that has no cube factors
  - ac + ad + bc + bd + e is cube free
  - abc + abd is not cube free
  - abc is not cube free
- Cube Division: F/P can be formed by deleting the literals of P from F
- The **primary divisors** of an expression *f* are the set of expressions
  - D(f) = {f/c such that c is a cube}
- The **kernels** of f are the set of its cube-free primary divisors:
  - K(f) = { g such that g exists D(f) and g id cube-free }
- The **co-kernel** of *k=f/c* is the cube *c*.  
  - co-kernels are not unique
- Kernel generation is accomplished through repeated weak division
  - We will repeadetly divide by each term, until only cube-free expressions remain

Example
  - F = abcd + abdce + efg
  - Kernel: d + e, co-kernel abc
  - Kernel: abc + fg, co-kernel e

## Technology Mapping
- Goal is twofold
  - Matching: Determien librar cells that are functionally equivalent to the sub-networks rooted at all nodes in a Boolean network
  - Covering: Select a minimum-cost set of library cells that math all nodes in the Boolean network

#### Tree Covering Algorithm
- Represent library by trees, the simplest of which are the basic gates (NAND, INV, etc)
- Bind each subtree in the circuit graph by starting at the root (output), and then using the matching algorithm
  - Scan the subject tree from roo node toward the inputs
  - Find the matching library patterns for each node, record is cost
  - Select set of matches or cover for C with the lowest overall cost

## Minimization
- Literal Count:
  - TODO: Look at lecture 2 to confirm this
  - Calculat the literal counts of the following boolean expressions:
    - abc + bcd + ef + a'b'c
    - (a + b + c)(a + e)(a' + c')
    - ab(c + d) + af + a'
- State Minimization
  - Distinguishable States
    - Given M1 in an intial state S1, and M2 in initial state S2.
    - States S1 and S2 are **distinguishable** iff there is at least one input sequence X such that the output of the two systems if different
      - X is a **distinguishable sequence** for S1, S2
    - S1 and S2 are **k-distinguishable** if X's length is at most *k*
    - S1 and S2 are **k-equivalent** if thye are not k-distinguishable
    - S1 and S2 are **equivalent**, denoted S1=S2, iff all outputs are equal for all input sequences X
  - Algorithm: TODO


## Stochastic Circuits
