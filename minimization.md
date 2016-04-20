## Minimization
- Literal Count:
  - TODO: Look at lecture 2 to confirm this
  - Calculate the literal counts of the following boolean expressions:
  ```
    abc + bcd + ef + a'b'c
    (a + b + c)(a + e)(a' + c')
    ab(c + d) + af + a'
    ```
- State Minimization
  - Distinguishable States
    - Given M1 in an initial state S1, and M2 in initial state S2.
    - States S1 and S2 are **distinguishable** iff there is at least one input sequence X such that the output of the two systems if different
      - X is a **distinguishable sequence** for S1, S2
    - S1 and S2 are **k-distinguishable** if X's length is at most *k*
    - S1 and S2 are **k-equivalent** if thye are not k-distinguishable
    - S1 and S2 are **equivalent**, denoted S1=S2, iff all outputs are equal for all input sequences X
  - Algorithm: TODO
