# DFA & NFA

DFA: Deterministic Finite Automata
NFA: Non-deterministic Finite Automata

DFA:
 - only one start state
 - exactly one transition from each state for each character in alphabet
 - can have many end states
 - has unique minimum machine

NFA:
 - can have many start and end states
 - transitions that don't lead to a successful outcome don't need to be specified
 - can have empty (epsilon) transitions
 - follow all paths in parallel, if ANY end state is reached, then string is accepted
 - no unique minimum machine

DFAs and NFAs are equivalent

To convert an NFA to a DFA, create states in the DFA that are labelled with all the states the NFA could be in by that point (could be $2^n$ states). Mark every state final where any of its original states are final.

To find compliment of DFA, invert final and non-final states
To find reverse of DFA, reverse all arrows, invert start and end states, convert resulting NFA to DFA (double reversal results in a minimum DFA)
To find union of two DFAs, make empty transition to each start state and convert back to DFA
To concatenate two DFAs, make empty transition from each end state of one to the start state of the next, then convert back to DFA
To find intersection of two DFAs, use DeMorgans with union and compliment. Short cut: follow algorithm for union, but instead of morking every state final where any original state was final, only mark final states where BOTH original states are final. (product, so this can only grow to $n \cdot m$ states max)

Minimizing DFAs - just watch the lecture, there are at least 3 ways to do it - $\text{O}(n^3)$, $\text{O}(n^2)$, and $\text{O}(n \log n)$.

Determine if two DFA's are equivalent - check if: $A - B = \emptyset$ and $B - A = \emptyset$ by doing $A \cap \overline{B}$ and $B \cap \overline{A}$. (I feel like this should be $A \cup \overline{B}$ and $B \cup \overline{A}$, but this is how he wrote it on the board, claiming "set theory")

## Example NFA for when I return to this course:
```viz
digraph FSM {
  rankdir = LR;
  size = "8,5"
  bgcolor = transparent;

  node [color = grey60, fontcolor = grey80];

  node [shape = doublecircle];
  LR_0 LR_3 LR_4 LR_8;

  node [shape = circle];
  edge [color=grey60, fontcolor = grey80];
  LR_0 -> LR_2 [ label = "SS(B)" ];
  LR_0 -> LR_1 [ label = "SS(S)" ];
  LR_1 -> LR_3 [ label = "S($end)" ];
  LR_2 -> LR_6 [ label = "SS(b)" ];
  LR_2 -> LR_5 [ label = "SS(a)" ];
  LR_2 -> LR_4 [ label = "S(A)" ];
  LR_5 -> LR_7 [ label = "S(b)" ];
  LR_5 -> LR_5 [ label = "S(a)" ];
  LR_6 -> LR_6 [ label = "S(b)" ];
  LR_6 -> LR_5 [ label = "S(a)" ];
  LR_7 -> LR_8 [ label = "S(b)" ];
  LR_7 -> LR_5 [ label = "S(a)" ];
  LR_8 -> LR_6 [ label = "S(b)" ];
  LR_8 -> LR_5 [ label = "S(a)" ];
}
```
