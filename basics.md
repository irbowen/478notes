## Basics
- PMOS and NMOS transistors have voltages applied to them that are not interchangeable. Only PMOS transistors can be used in the pull up circuit, and only NMOS transistors can be used in the pull down circuit.

- **Boole Shannon Expansion Thm**
- __* Sup Brah *__


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
  - Distributive
  - These properties are only defined on lattices!  Not non-lattice posets

#### Boolean Algebra
