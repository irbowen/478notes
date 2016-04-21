## Basics
- PMOS and NMOS transistors have voltages applied to them that are not interchangeable. Only PMOS transistors can be used in the pull up circuit, and only NMOS transistors can be used in the pull down circuit.
- Sets that are functionally complete
  - AND, OR, NOT
  - NAND
  - NOR
  - OR, NOT
  - XOR, NOT is NOT functionally completes

## Early Defintions
- In Boolean logic, an *implicant* is a "covering" (sum term or product term) of one or more minterms in a sum of products (or maxterms in a product of sums) of a Boolean function
- Any single 1 or group of 1's that can be combined together on a Karnaugh map of the function F represents a product term which is called an *IMPLICANT*
- A *PRIME IMPLICANT* is a product term that cannot be combined with sanother term to eliminate a variable.
- A lattice is a poset in which ever ypair of elements has a unique glb and a unique lub
- A finite lattice has a least and greatest element
- Implicant refers to product terms
- Implicate refers to sums

## SOP to POS Conversion
- Distributivity
  - x(y+z) = xy + xz
  - x + yz = (x + z)(x + z)
- Example
  - z = ab + cd
  - (ab + c)(ab +d)
  - (c + ab)(d + ab)
  - (c + a)(c + b)(d + a)(d + b)

- **Minterm**
  - A minterm is 1 for exactly one input combination
  - It can be implemented by a single AND gate
- **Maxterm**
  - A maxterm is 0 for exactly one input combination
  - It can be implemented by a single OR gate


## Sets, Relations, Partial Orderings, Lattices
- Set
  - A collection of elements
- Relation
  - A mapping of ordered pairs

#### Properties
- Reflexive
  - R is reflexive if a**_R_**a for every a in A
  - Self-loops in a diagram
- Symmetric
  - R is symmetric if a**_R_**b implies that b**_R_**a
- Antisymmetric
  - R is antisymmetric if a**_R_**b and b**_R_**a implies that a = b
  - Not the same as not symmetric
- Transitive
  - R is transitive if a R b and b R c implies that a R c
- **Compatibility Relation** - Reflexive and Symmetric
  - Need not be transitive
- **Equivalence Relation** - Reflexive, Symmetric, Transitive
  - \# (pi): number of blocks
  - p (pi): number of elements in largest block
  - Subset of the Compatibility Relation
- **Partial Order** - Reflexive, Antisymmetric, Transitive

#### Partial Ordered Sets
- POSET: an alternative to a total ordering
- Can be drawn with a Hasse diagram
- Reflexive, AntiSymmetric, Transitive
- Meet = AND = glb (greatest lower bound)
- Join = OR = lub (least upper bound)

#### Lattices
- **Lattice:** Poset where any/every two elements have a meet and join
- Two propeties lattices can have:
  - Complemented
    - If every element has a complement
    - Complment meaning that their exist a node a' such that
      - a and a' = 0
      - a or a' = 1
  - Distributive
    - If the distributive law holds in all cases
    - a(b+c) = ab + ac
    - a + bc = (a+b)(a+c)
  - These properties are only defined on lattices!  Not non-lattice posets
- Boolean Algebra
  - A complmented, distributed lattice

## Terms you should know
- Gate
- Combinational circuit
- Truth table
- Boolean algebra
- Boolean function
- Prime implicant
- Two-level design
- Karnaugh map (Kmap)
- Latch and flipflop
- State table
- Sequential circuit

## BDDs
- *Boole Shannon Expansion Thm*
  - Set the variable equal to true or false, and then map the results value in each child
- SOP or POS is not cannoical
- ROBDD is
- BDD to ROBDD
  - merge identical sub trees
  - remove nodes with identical children graphs
- Probabilities of BDDs
  - number of 1s in its truth table divided by number of rows

## Davis-Putnam Method
- Used to determine a boolean functions validity
  - Unit clase rule: assign lone literals to 1 - they have to be
  - Pure literal rule: if a literal is never negated, then it must have a value of 1
  - Then, split and branch
  - Consider: conseous: (x+y)•(x’+z) = (x+y)•(x’+z)•(y+z)
