## Basics
- PMOS and NMOS transistors have voltages applied to them that are not interchangeable. Only PMOS transistors can be used in the pull up circuit, and only NMOS transistors can be used in the pull down circuit.

### AND
| A | B |Out|
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

### NAND
| A | B |Out|
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

### OR
| A | B |Out|
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

### NOR
| A | B |Out|
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

### XOR
| A | B |Out|
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

### XNOR
| A | B |Out|
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

## Terms you should know
- Gate
- Combinational circuit
- Truth table
- Boolean algebra
- Boolean function
- **Minterm**
  - A minterm is 1 for exactly one input combination
  - It can be implemented by a single AND gate
- **Maxterm**
  - A maxterm is 0 for exactly one input combination
  - It can be implemented by a single OR gate
- Prime implicant
- Two-level design
- Karnaugh map (Kmap)
- Latch and flipflop
- State table
- Sequential circuit

## Sets, Relations, Partial Orderings, Lattices
- Set
  - A collection of elements
- Relation
  - A mapping of ordered pairs

#### Properties
- Reflexive
  - R is reflexive if a R a for every a in A
- Symmetric
  - R is symmetric if a R b implies that b R a
- Antisymmetric
  - R is antisymmetric if a R b and b R a implies that a = b
  - Not the same as not symmetric
- Transitive
  - R is transitive if a R b and b R c implies that a R c
- **Compatibility Relation** - Reflexive and Symmetric
  - Need not be transitive
- **Equivalence Relation** - Reflexive, Symmetric, Transitive
  - \# (pi): number of blocks
  - p (pi): number of elements in largest block
  - Subset of the Compatibility Relation

#### Partial Orderings
#### Partial Ordered Sets
#### Lattices
#### Boolean Algebra



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
