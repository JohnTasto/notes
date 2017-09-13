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

\[
  \begin{array}{cc|ccc}
    A & \cem2B & A \land B & A \lor B & A \rightarrow B \h3 \\[.5em]
    \hline
    0 & 0 & 0 & 0 & 1 \h3 \\
    0 & 1 & 0 & 1 & 1 \h3 \\
    1 & 0 & 0 & 1 & 0 \h3 \\
    1 & 1 & 1 & 1 & 1 \h3 \\
  \end{array}
\]

$$
\begin{aligned}
  A \rightarrow B &= (\neg A \land \neg B) \lor (\neg A \land B) \lor (A \land B) \h3 \\
  &= \neg A \lor B \h3 \\
\end{aligned}
$$

Commutative
Associative
DeMorgans
Distributive
Can distribute $\land$s through $\lor$s and $\lor$s through $\land$s!
$$
\begin{aligned}
  (A \lor B) \land C &= (A \land C) \lor (B \land C) \h3 \\
  (A \land B) \lor C &= (A \lor C) \land (B \lor C)  \h3 \\
\end{aligned}
$$

Disjunctive Normal Form (DNF) example:
$$
\begin{aligned}
  \overline A \overline B + A \overline B + A B \\
\end{aligned}
$$

Conjunctive Normal Form (CNF) example:
$$
\begin{aligned}
  (\overline A + \overline B) \cdot (A + \overline B) \cdot (A + B) \\
\end{aligned}
$$

Nors (or Nands) are sufficient to describe any operation:
$$
\begin{aligned}
  \neg X &= X \downarrow X \h3 \\
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

$\emptyset$ = $\{ \}$ (empty set)

$\mho$ = universal set

$$
\begin{aligned}
  \emptyset  &=                       \{\}                                    && \text{Empty set}        \h4 \\
  \mathbb{N} &=                       \{0, 1, 2, \ldots\}                     && \text{Natural numbers}  \h4 \\
  \mathbb{Z} &=       \mathbb{N} \cup \{\ldots, -2, -1\}                      && \text{Integers}         \h4 \\
  \mathbb{Q} &\supset \mathbb{Z} \cup \{-\tfrac17, \tfrac13, \ldots\}         && \text{Rational numbers} \h4 \\
             &=                       \{\tfrac{p}{q} \mid p, q \in \mathbb{Z}, q \ne 0\}                 \h4 \\
  \mathbb{R} &\supset \mathbb{Q} \cup \{\sqrt{2}, e, \pi, \ldots\}            && \text{Real numbers}     \h4 \\
  \mathbb{C} &\supset \mathbb{R} \cup \{\sqrt{-1}, i, \ldots\}                && \text{Complex numbers}  \h4 \\
  \mathbb{E} &=                       \{\ldots, -2, 0, 2, 4, \ldots\}         && \text{Even numbers}     \h4 \\
  \mathbb{O} &=                       \{\ldots, -1, 1, 3, 5, \ldots\}         && \text{Odd numbers}      \h4 \\
  \mho       &                                                                && \text{Universal set}    \h4 \\
  A \subseteq  B &\iff x \in A \rightarrow x \in B && \text{Subset}       \h4 \\
  x \in A \cap B &\iff x \in A \cap x \in B        && \text{Intersection} \h4 \\
  x \in A \cup B &\iff x \in A \cup x \in B        && \text{Union}        \h4 \\
\end{aligned}
$$

### Rules

$$
\begin{aligned}
  A \cup B &= B \cup A && \text{Commutative}                              \h4 \\
  A \cup (B \cap C) &= (A \cup B) \cap (A \cup C) && \text{Distributive}  \h4 \\
  A \cap (B \cup C) &= (A \cap B) \cup (A \cap C) && \text{Distributive}  \h4 \\
  \overline{A \cap B} &= \overline A \cup \overline B && \text{DeMorgans} \h4 \\
  \overline{A \cup B} &= \overline A \cap \overline B && \text{DeMorgans} \h4 \\
\end{aligned}
$$

### Proof of the distributive rule for sets:
$$
\begin{aligned}
  A \cup (B \cap C) &= (A \cup B) \cap (A \cup C) \h3 \\
  x \in A \cup (B \cap C) &= x \in (A \cup B) \cap (A \cup C) \h3 \\
  x \in A \lor x \in (B \cap C) &= x \in (A \cup B) \land x \in (A \cup C) \h3 \\
  x \in A \lor (x \in B \land x \in C) &= (x \in A \lor x \in B) \land (x \in A \lor x \in C) \h3 \\
\end{aligned}
$$
By applying the distributive rule from boolean algebra, both sides are equal.

### Proof that distributive rule applies to any number of sets:
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
