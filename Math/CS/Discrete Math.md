# Discrete Math

## Triangle Numbers
Discrete Math Lecture 1, 24:40

$$
\begin{aligned}
  T_n &= 1 + 2 + 3 + \ldots + n                \h6 \\
  &= (n + 1) {n \over 2}                       \h6 \\
  &= {n(n + 1) \over 2}                        \h6 \\
  &= \binom{n + 1}{2} && \text{binomial form}  \h6 \\
  &= T_{n-1} + n && \text{recurrence relation} \h6 \\[2em]
  T_{n+1} &= T_n + n + 1                       \h6 \\
\end{aligned}
$$

## Boolean Algebra

### Rules

$$
\begin{aligned}
  A + 0 &= A & A \cdot 1 &= A
  && \text{Identity}     \h4 \\
  A + 1 &= 1 & A \cdot 0 &= 0
  && \text{Annihilator}  \h4 \\
  A + (A \cdot B) &= A & A \cdot (A + B) &= A
  && \text{Absorption}   \h4 \\
  A + \ng|A &= 1 & A \cdot \ng|A &= 0
  && \text{Complement (also, $\smash{\ng|{\ng|A}} = A$)} \h4 \\
  A + A &= A & A \cdot A &= A
  && \text{Idempotence}  \h4 \\
  A + (B + C) &= (A + B) + C & A \cdot (B \cdot C) &= (A \cdot B) \cdot C
  && \text{Associative}  \h4 \\
  A + B &= B + A & A \cdot B &= B \cdot A
  && \text{Commutative}  \h4 \\
  A + (B \cdot C) &= (A + B) \cdot (A + C) & A \cdot (B + C) &= (A \cdot B) + (A \cdot C)
  && \text{Distributive} \h4 \\
  \ng|A + \ng|B &= \ng|{(A \cdot B)} & \ng|A \cdot \ng|B &= \ng|{(A + B)}
  && \text{DeMorgan's}   \h4 \\
\end{aligned}
$$

\[
  \begin{array}{cc|ccc}
    A & \cem2B & A \cdot B & A + B & A \rightarrow B \h3 \\[.5em]
    \hline
    0 & 0 & 0 & 0 & 1 \h3 \\
    0 & 1 & 0 & 1 & 1 \h3 \\
    1 & 0 & 0 & 1 & 0 \h3 \\
    1 & 1 & 1 & 1 & 1 \h3 \\
  \end{array}
\]

$$
\begin{aligned}
  A \rightarrow B &= (\ng|A \cdot \ng|B) + (\ng|A \cdot B) + (A \cdot B) \h3 \\
  &= \ng|A + B \h3 \\
\end{aligned}
$$

Disjunctive Normal Form (DNF) example:
$$
\begin{aligned}
  \ng|A \ng|B + A \ng|B + A B \\
\end{aligned}
$$

Conjunctive Normal Form (CNF) example:
$$
\begin{aligned}
  (\ng|A + \ng|B) \cdot (A + \ng|B) \cdot (A + B) \\
\end{aligned}
$$

Nors (or Nands) are sufficient to describe any operation:
$$
\begin{aligned}
  \ng|X &= X \downarrow X \h3 \\
  XY &= (X \downarrow X) \downarrow (Y \downarrow Y) \h3 \\
  X + Y &= (X \downarrow Y) \downarrow (X \downarrow Y) \h3 \\
\end{aligned}
$$

## Algorithms

Reduction: if algorithm $A \le B$ ($A$ reduces to $B$), then $A$ is no harder than $B$. Reduction must be in poly time to be useful.

Classes of algorithms for decision problems (yes/no answer):

  - P (polynomial)
    - solvable in poly time
  - NP (nondeterministic polynomial)
    - solvable in polynomial time by a nondeterministic Turing machine
    - runs in exponential time on real computers
    - check result in poly time
    - can be parallelized
    - examples:
      - boolean satisfiability (solving a CNF)
      - traveling salesman
      - integer factorization. This is the problem that given integers $n$ and $m$, is there an integer $f$ with $1 < f < m$, such that $f \mid n$ ($f$ is a factor of $n$)?
  - NP-Complete
    - NP $\le$ NP-Complete
    - examples:
      - 3SAT (boolean satisfiability where each disjunction has three clauses)
  - NP-Hard
    - NP-Complete $\le$ NP-Hard

## Sets

### Definitions

$$
\begin{aligned}
  \varnothing &=                       \{\}                                    && \text{Empty set}        \h4 \\
  \mathbb{N}  &=                       \{0, 1, 2, \ldots\}                     && \text{Natural numbers}  \h4 \\
  \mathbb{Z}  &=       \mathbb{N} \cup \{\ldots, -2, -1\}                      && \text{Integers}         \h4 \\
  \mathbb{Q}  &\supset \mathbb{Z} \cup \{-\tfrac17, \tfrac13, \ldots\}         && \text{Rational numbers} \h4 \\
              &=                       \{\tfrac{p}{q} \mid p, q \in \mathbb{Z}, q \ne 0\}                 \h4 \\
  \mathbb{R}  &\supset \mathbb{Q} \cup \{\sqrt{2}, e, \pi, \ldots\}            && \text{Real numbers}     \h4 \\
  \mathbb{C}  &\supset \mathbb{R} \cup \{\sqrt{-1}, i, \ldots\}                && \text{Complex numbers}  \h4 \\
  \mathbb{E}  &=                       \{\ldots, -2, 0, 2, 4, \ldots\}         && \text{Even numbers}     \h4 \\
  \mathbb{O}  &=                       \{\ldots, -1, 1, 3, 5, \ldots\}         && \text{Odd numbers}      \h4 \\
  \mathbb{U}  &                                                                && \text{Universal set}    \h4 \\
  A \subseteq  B &\iff x \in A \rightarrow x \in B        && \text{Subset}              \h4 \\
  x \in A \cap B &\iff x \in A \land x \in B              && \text{Intersection}        \h4 \\
  x \in A \cup B &\iff x \in A \lor  x \in B              && \text{Union}               \h4 \\
  x \in    \ng|A &\iff x \in \mathbb{U} \land x \notin A  && \text{Absolute Complement} \h4 \\
  x \in A \setminus B &\iff x\in A \land x \notin B       && \text{Relative Complement} \h4 \\
\end{aligned}
$$

### Rules

$$
\begin{aligned}
  A \cup \varnothing &= A & A \cap \varnothing &= \varnothing
  && \text{Universal}    \h4 \\
  A \cup \mathbb{U} &= \mathbb{U} & A \cap \mathbb{U} &= A
  && \text{Empty}        \h4 \\
  A \cup \ng|A &= \mathbb{U} & A \cap \ng|A &= \varnothing
  && \text{Complement (also, $\ng|{\mathbb{U}} = \varnothing$)} \h4 \\
  A \cup (B \cup C) &= (A \cup B) \cup C & A \cap (B \cap C) &= (A \cap B) \cap C
  && \text{Associative}  \h4 \\
  A \cup B &= B \cup A & A \cap B &= B \cap A
  && \text{Commutative}  \h4 \\
  A \cup (B \cap C) &= (A \cup B) \cap (A \cup C) & A \cap (B \cup C) &= (A \cap B) \cup (A \cap C)
  && \text{Distributive} \h4 \\
  \ng|{A \cap B} &= \ng|A \cup \ng|B & \ng|{A \cup B} &= \ng|A \cap \ng|B
  && \text{DeMorgan's}    \h4 \\[1em]
  A \setminus \varnothing &= A & \varnothing \setminus A &= \varnothing
  && \text{Complement (also, $A \setminus A = \varnothing$)} \h4 \\
  A \setminus B &= \ng|B \setminus \ng|A & A \subset B &\implies \ng|B \subset \ng|A \h4 \\
  A \setminus B &= A \cap \ng|B & \ng|{A \setminus B} &= \ng|A \cup B \h4 \\
  C \setminus (A \cap B) &= (C \setminus A) \cup (C \setminus B) &
  C \setminus (A \cup B) &= (C \setminus A) \cap (C \setminus B)
  && \text{Distributive} \h4 \\
  C \setminus (B \setminus A) &= (C \cap A) \cup (C \setminus B) &
  C \setminus (C \setminus A) &= (C \cap A) \h4 \\
  (B \setminus A) \cap C &= (B \cap C) \setminus A = B \cap (C \setminus A) &
  (B \setminus A) \cup C &= (B \cup C) \setminus (A \setminus C) \h4 \\
\end{aligned}
$$

#### Proof of the distributive rule for sets:
$$
\begin{aligned}
  A \cup (B \cap C) &= (A \cup B) \cap (A \cup C) \h3 \\
  x \in A \cup (B \cap C) &= x \in (A \cup B) \cap (A \cup C) \h3 \\
  x \in A \lor x \in (B \cap C) &= x \in (A \cup B) \land x \in (A \cup C) \h3 \\
  x \in A \lor (x \in B \land x \in C) &= (x \in A \lor x \in B) \land (x \in A \lor x \in C) \h3 \\
\end{aligned}
$$
By applying the distributive rule from boolean algebra, both sides are equal.

#### Proof that distributive rule applies to any number of sets:
$$
\begin{aligned}
  A \cup (B_1 \cap B_2 \cap \ldots \cap B_n) &= (A \cap B_1) \cup (A \cap B_2) \cup \ldots \cup (A \cap B_n) \h3 \\
  A \cup (B_1 \cap B_2 \cap \ldots \cap B_{n+1}) &= (A \cap B_1) \cup (A \cap B_2) \cup \ldots \cup (A \cap B_{n+1}) \h3 \\
  A \cup [(B_1 \cap B_2 \cap \ldots \cap B_n) \cap B_{n+1}] \h3 \\
  \space [A \cup (B_1 \cap B_2 \cap \ldots \cap B_n)] \cap (A \cup B_{n+1}) \h3 \\
\end{aligned}
$$
By induction, bla bla bla.

## Combinations

Two tricks:

  - count the stuff you're not interested in
  - count double/multiple in a controlled way

Inclusion Exclusion Theorem:

$$
\begin{aligned}
  |A \cup B| &= |A| + |B| - |A \cap B| \h4 \\
  |A \cup B \cup C| &= |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C| \h4 \\
\end{aligned}
$$

Useful because ands are often easier to count than ors.
Can keep going with more sets, just alternate adding and subtracting.
The number of terms for each step is binomial.
Can be proven by induction by grouping all but one set.

## Functions and 1:1 Correspondence

If a function has a 1:1 correspondence, then it has an inverse.
If a function is both **one-one** and **onto**, then it has both a 1:1 correspondence and an inverse.

  - **one-one**: No value in the range has more than one input that maps to it.
  - **onto**: Every value in the range has at least one input that maps to it.

\[
  \begin{gathered}
    \text{one-one, not onto} & \text{onto, not one-one} & \text{one-one and onto}\\[.5em]
    \begin{aligned}
        \mathbb{N} ~\longrightarrow&~ \mathbb{N} \\
        f:~ x ~\longrightarrow&~ x^2 \\[.5em]
        1 \longleftrightarrow&~ 1 \\
        2 \longleftrightarrow&~ 4 \\
        3 \longleftrightarrow&~ 9 \\
    \end{aligned} &
    \begin{aligned}
        \mathbb{R} ~\longrightarrow&~ \mathbb{Z} \\
        f:~ x ~\longrightarrow&~ \lceil x \rceil \\[.5em]
    \end{aligned} &
    \begin{aligned}
        \mathbb{R} ~\longrightarrow&~ \mathbb{R} \\
        f:~ x ~\longrightarrow&~ x + 1 \\
        f^{-1}:~ x ~\longrightarrow&~ x - 1 \\[.5em]
    \end{aligned} \\
  \end{gathered}
\]

## Dunno

\[
  \begin{aligned}
                      1^3 + 2^3 + \cdots + n^3 &= (1 + 2 + \cdots + n)^2 \h4 \\
              (1 + 2 + \cdots + (n-1))^2 + n^3 &= (1 + 2 + \cdots + n)^2 \h4 \\
    (1 + 2 + \cdots + (n-2))^2 + (n-1)^3 + n^3 &= (1 + 2 + \cdots + n)^2 \h4 \\
  \end{aligned}
\]

## Summations

Show that $1^2 + 2^2 + \cdots + n^2 = {n(n+1)(2n+1) \over 6}$.

\[
  \begin{gathered}
    \begin{aligned}
          1^2 &= 1 \h4 \\
          2^2 &= 1 + 3 \h4 \\
          3^2 &= 1 + 3 + 5 \h4 \\
          4^2 &= 1 + 3 + 5 + 7 \h4 \\
          n^2 &= 1 + 3 + 5 + \cdots + (2n-3) + (2n-1) \h4 \\
      (n+1)^2 &= n^2 + (2n+1) \h4 \\
    \end{aligned} \\[1em]
    \begin{alignedat}{1}
               &1 \h4 \\
               &1 &+    3 \h4 \\
               &1 &+    3 &+      5 \h4 \\
               &1 &+    3 &+      5      &+ 7 \h4 \\
      + \qquad &1 &+    3 &+      5      &+ 7      &+ \cdots + (2n-1) \h4 \\
      \hline
      = \qquad &1(n) &+ 3(n-1) &+ 5(n-2) &+ 7(n-3) &+ \cdots + (2n-1)1 \h4 \\
    \end{alignedat} \\[1em]
    \begin{array}{c|c|c}
      \text{term} & ~\text{factor} &~\text{factor} \h3 \\[.5em]
      \hline
      1      & n      & 1      \h3 \\
      2      & n-1    & 3      \h3 \\
      3      & n-2    & 5      \h3 \\
      \vdots & \vdots & \vdots \h3 \\
      i      & n-i+1  & 2i - 1 \h3 \\
    \end{array} \\[1em]
  \end{gathered} \qquad
  \begin{aligned}
     \sum_{i=1}^n i^2 &= \sum_{i=1}^n (n - i + 1)(2i - 1)                           \h7 \\
                      &= \sum_{i=1}^n 2in - 2i^2 + 2i - n + i - 1                   \h7 \\
                      &= \sum_{i=1}^n 3i + 2in - n - 1 - 2i^2                       \h7 \\
                      &= \sum_{i=1}^n (3 + 2n)i - n - 1 - 2i^2                      \h7 \\
                      &= \sum_{i=1}^n \[(3 + 2n)i - 2i^2] - n^2 - n                 \h7 \\
                      &= \sum_{i=1}^n \[(3 + 2n)i] - 2\sum_{i=1}^n \[i^2] - n^2 - n \h7 \\
    3 \sum_{i=1}^ni^2 &= \sum_{i=1}^n \[(3 + 2n)i] - n^2 - n                        \h7 \\
                      &= (3 + 2n)\sum_{i=1}^n \[i] - n^2 - n                        \h7 \\
                      &= (3 + 2n)\({n(n + 1) \over 2}) - n(n + 1)                   \h7 \\
                      &= {(3 + 2n)n(n + 1) \over 2} - {2n(n + 1) \over 2}           \h7 \\
                      &= {(3 + 2n - 2)n(n + 1) \over 2}                             \h7 \\
      \sum_{i=1}^ni^2 &= {(2n + 1)(n + 1)n \over 6}                                 \h7 \\
  \end{aligned}
\]

### Geometric Series

Solve $x = {1 \over 10^1} + {2 \over 10^2} + {3 \over 10^3} + {4 \over 10^4} + \cdots$.

\[
  \begin{aligned}
                x ~~&=~~    {1 \over 10^1} +   {2 \over 10^2} + {3 \over 10^3} + {4 \over 10^4} + \cdots \h7 \\
    {1 \over 10}x ~~&=~~ \p{{1 \over 10^1} +{}}{1 \over 10^2} + {2 \over 10^3} + {3 \over 10^4} + \cdots
    && \raise1.5em{\smash{\text{Subtract $\sim rx$}}} \h7 \\[1em]
    x - {1 \over 10}x ~~=~~ \left(1 - {1 \over 10}\right)x ~~=~~ {9 \over 10} x
                  ~~&=~~    {1 \over 10^1} +   {1 \over 10^2} + {1 \over 10^3} + {1 \over 10^4} + \cdots \h7 \\
        {1 \over 10}{9 \over 10} x ~~=~~ {9 \over 100} x
                  ~~&=~~ \p{{1 \over 10^1} +{}}{1 \over 10^2} + {1 \over 10^3} + {1 \over 10^4} + \cdots
    && \raise1.5em{\smash{\text{Do it again!}}} \h7 \\[1em]
                 {9 \over 10} x - {9 \over 100} x = { 1 \over  10} \qquad
    \left({90 \over 100} - {9 \over 100}\right)x &= {10 \over 100} \qquad
                                              81x = 10 \h7 \qquad
                                                x = {10 \over 81} && \text{Now just solve for $x$.} \h7 \\
  \end{aligned}
\]
