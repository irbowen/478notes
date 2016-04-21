## Minimization

- State Minimization
  - Distinguishable States
    - Given M1 in an initial state S1, and M2 in initial state S2.
    - States S1 and S2 are **distinguishable** iff there is at least one input sequence X such that the output of the two systems if different
      - X is a **distinguishable sequence** for S1, S2
    - S1 and S2 are **k-distinguishable** if X's length is at most *k*
    - S1 and S2 are **k-equivalent** if thye are not k-distinguishable
    - S1 and S2 are **equivalent**, denoted S1=S2, iff all outputs are equal for all input sequences X
  - State equivalence is a equivalence relation: reflexive, transitive, symmetric

## Methods
- Tabular Method
  - remove essential rows and the columns they cover
  - delete pi's totally covered by the essentials removed
  - Then
    - Use row domiance, and delete the dominated row
    - Use column dominace, and delete the dominating column
- Quine-McCusivty
- Petricks
  - Finds all covers
- Branch and Bound
- Heuristic

- State Minimization
  - Distinguishable States
    - Given M1 in an initial state S1, and M2 in initial state S2.
    - States S1 and S2 are **distinguishable** iff there is at least one input sequence X such that the output of the two systems if different
      - X is a **distinguishable sequence** for S1, S2
    - S1 and S2 are **k-distinguishable** if X's length is at most *k*
    - S1 and S2 are **k-equivalent** if thye are not k-distinguishable
    - S1 and S2 are **equivalent**, denoted S1=S2, iff all outputs are equal for all input sequences X
  - State equivalence is a equivalence relation: reflexive, transitive, symmetric

- Method seen in class
- Method with table and loops
- Does it end up in the same subsection as me?

- Incompetely Specified FSM:
  - We only care about compatability, not whether its an exact match.
  - Compatability means that it matches where the outputs are specified.
  - Two states are compatible if 
    - They produce the same output where both outputs are specified
    - They go to the compatible next states where both next states are specified.

- Literal Count:
  - TODO: Look at lecture 2 to confirm this
  - Calculate the literal counts of the following boolean expressions:
  ```
    abc + bcd + ef + a'b'c
    (a + b + c)(a + e)(a' + c')
    ab(c + d) + af + a'
    ```
-
