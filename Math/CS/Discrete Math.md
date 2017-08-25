# Discrete Math

## Triangle numbers
Discrete Math Lecture 1, 24:40

$$
\begin{aligned}
  T_n &= 1 + 2 + 3 + \ldots + n \\[0.5em]
  &= (n + 1) \frac{n}{2} \\[1em]
  &= \frac{n(n + 1)}{2} \\[1em]
  &= \binom{n + 1}{2} && \text{binomial form} \\[1em]
  &= T_{n-1} + n && \text{recurrence relation} \\[2.5em]
  T_{n+1} &= T_n + n + 1 \\
\end{aligned}
$$

## Boolean Algebra

|  $A$  |  $B$  | $A \land B$ | $A \lor B$ | $A \rightarrow B$ |
| :---: | :---: | :---------: | :--------: | :---------------: |
|   0   |   0   |      0      |     0      |         1         |
|   0   |   1   |      0      |     1      |         1         |
|   1   |   0   |      0      |     1      |         0         |
|   1   |   1   |      1      |     1      |         1         |

$$
\begin{aligned}
  A \rightarrow B &= (\neg A \land \neg B) \lor (\neg A \land B) \lor (A \land B) \\
  &= \neg A \lor B \\
\end{aligned}
$$

Indeed! We've both almost doubled our ages since saw each other! We should catch up sometime!
Indeed! We've both nearly doubled our ages since saw each other. Wow that's kinda scary to think about... We should catch up sometime!

Hey man, yeah I sort of dropped out for a while there. We still need to finish that System of a Down track!

Years! How's life been? You still doing spinning gigs?


Commutative
Associative
DeMorgans
Distributive
Can distribute $\land$s through $\lor$s and $\lor$s through $\land$s!
$$
\begin{aligned}
  (A \lor B) \land C &= (A \land C) \lor (B \land C) \\
  (A \land B) \lor C &= (A \lor C) \land (B \lor C) \\
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
  \neg X &= X \downarrow X \\
  XY &= (X \downarrow X) \downarrow (Y \downarrow Y) \\
  X + Y &= (X \downarrow Y) \downarrow (X \downarrow Y) \\
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
  \emptyset  &=                       \{\}                                    && \text{Empty set} \\
  \mathbb{N} &=                       \{0, 1, 2, \ldots\}                     && \text{Natural numbers} \\
  \mathbb{Z} &=       \mathbb{N} \cup \{\ldots, -2, -1\}                      && \text{Integers} \\
  \mathbb{Q} &\supset \mathbb{Z} \cup \{-\tfrac{1}{7}, \tfrac{1}{3}, \ldots\} && \text{Rational numbers} \\
  \mathbb{R} &\supset \mathbb{Q} \cup \{\sqrt{2}, e, \pi, \ldots\}            && \text{Real numbers} \\
  \mathbb{C} &\supset \mathbb{R} \cup \{\sqrt{-1}, i, \ldots\}                && \text{Complex numbers} \\
  \mathbb{E} &=                       \{\ldots, -2, 0, 2, 4, \ldots\}         && \text{Even numbers} \\
  \mathbb{O} &=                       \{\ldots, -1, 1, 3, 5, \ldots\}         && \text{Odd numbers} \\
  \mho       &                                                                && \text{Universal set} \\
  A \subseteq  B &\Longleftrightarrow x \in A \rightarrow x \in B && \text{Subset} \\
  x \in A \cap B &\Longleftrightarrow x \in A \cap x \in B        && \text{Intersection} \\
  x \in A \cup B &\Longleftrightarrow x \in A \cup x \in B        && \text{Union} \\
\end{aligned}
$$

### Rules

$$
\begin{aligned}
  A \cup B &= B \cup A && \text{Commutative} \\
  A \cup (B \cap C) &= (A \cup B) \cap (A \cup C) && \text{Distributive} \\
  A \cap (B \cup C) &= (A \cap B) \cup (A \cap C) && \text{Distributive} \\
  \overline{A \cap B} &= \overline A \cup \overline B && \text{DeMorgans} \\
  \overline{A \cup B} &= \overline A \cap \overline B && \text{DeMorgans} \\
\end{aligned}
$$

### Proof of the distributive rule for sets:
$$
\begin{aligned}
  A \cup (B \cap C) &= (A \cup B) \cap (A \cup C) \\
  x \in A \cup (B \cap C) &= x \in (A \cup B) \cap (A \cup C) \\
  x \in A \lor x \in (B \cap C) &= x \in (A \cup B) \land x \in (A \cup C) \\
  x \in A \lor (x \in B \land x \in C) &= (x \in A \lor x \in B) \land (x \in A \lor x \in C) \\
\end{aligned}
$$
By applying the distributive rule from boolean algebra, both sides are equal.

### Proof that distributive rule applies to any number of sets:
$$
\begin{aligned}
  A \cup (B_1 \cap B_2 \cap \ldots \cap B_n) &= (A \cap B_1) \cup (A \cap B_2) \cup \ldots \cup (A \cap B_n) \\
  A \cup (B_1 \cap B_2 \cap \ldots \cap B_{n+1}) &= (A \cap B_1) \cup (A \cap B_2) \cup \ldots \cup (A \cap B_{n+1}) \\
  A \cup [(B_1 \cap B_2 \cap \ldots \cap B_n) \cap B_{n+1}] \\
  \space [A \cup (B_1 \cap B_2 \cap \ldots \cap B_n)] \cap (A \cup B_{n+1}) \\
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
  |A \cup B| &= |A| + |B| - |A \cap B| \\
  |A \cup B \cup C| &= |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C| \\
\end{aligned}
$$

Useful because ands are often easier to count than ors.
Can keep going with more sets, just alternate adding and subtracting.
The number of terms for each step is binomial.
Can be proven by induction by grouping all but one set.
