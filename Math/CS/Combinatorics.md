# Combinatorics

## Factorial rules
\[
  \begin{aligned}
                   0! &= 1                               \\
                   1! &= 1                               \\[1em]
                   n! &= n(n-1)(n-2)\ldots(2)(1)         \\
                  n!! &= n(n-2)(n-4)\ldots               \\
                 n!!! &= n(n-3)(n-6)\ldots               \\[1.5em]
    \frac{n!}{(n+m)!} &= \frac{1}{(n+1)(n+2)\ldots(n+m)} \\[1em]
    \frac{n!}{(n-m)!} &= (n)(n-1)(n-2)\ldots(n-m+1)
  \end{aligned}
\]

See [Multifactorial](http://mathworld.wolfram.com/Multifactorial.html).

## Permutations

Permutations are the number of ways to choose $k$ objects out of $n$ when order matters.

With repetition:
\[
  n^k
\]

Without repetition:
\[
  \begin{aligned}
    P(n,k) =\ _nP_k &= (n)(n-1)(n-2)\ldots(n-k+1) \\[1em]
                    &= \frac{n!}{(n-k)!}          \\[1em]
  \end{aligned}
\]

## Combinations

Combinations are the number of ways to choose $k$ objects out of $n$ when order does not matter.

With repetition:
\[
  \binom{k+n-1}{k} = \frac{(k+n-1)!}{k!(n-1)!}
\]

Without repetition:
\[
  \begin{aligned}
    C(n,k) =\ _nC_k = \binom{n}{k} &= \frac{(n)(n-1)(n-2)\ldots(n-k+1)}{k!} \\[1em]
                                   &=\ \frac{_nP_k}{k!}                     \\[1em]
                                   &= \frac{n!}{k!(n-k)!}                   \\[1em]
  \end{aligned}
\]

## Binomial Symmetry

\[
  \binom{n}{k} = \binom{n}{n-k}
\]

i.e., choosing $3$ out of $16$ gives the same number of combinations as choosing $13$ out of $16$.

## Pascal's Triangle

\[
  \binom{\text{row}}{\text{column}}
\]

\[
  \binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}
\]

\[
  \begin{matrix}
                                              \:1\:                                           \\[.5em]
                                        \:1\: \quad \:1\:                                     \\[.5em]
                                  \:1\: \quad \:2\: \quad \:1\:                               \\[.5em]
                            \:1\: \quad \:3\: \quad \:3\: \quad \:1\:                         \\[.5em]
                      \:1\: \quad \:4\: \quad \:6\: \quad \:4\: \quad \:1\:                   \\[.5em]
                \:1\: \quad \:5\: \quad   10  \quad   10  \quad \:5\: \quad \:1\:             \\[.5em]
          \:1\: \quad \:6\: \quad   15  \quad   20  \quad   15  \quad \:6\: \quad \:1\:       \\[.5em]
    \:1\: \quad \:7\: \quad   21  \quad   35  \quad   35  \quad   21  \quad \:7\: \quad \:1\:
  \end{matrix}
\]

\[
  \begin{array}{ccccccccl}
    ~~~~ & ~~~~ & ~~~~ & ~~~~ & ~~~~ & ~~~~ & ~~~~ & ~~~~                              \\
      1  &   1  &   1  &   1  &   1  &   1  &   1  &   1                               \\[.75em]
      1  &   2  &   3  &   4  &   5  &   6  &   7  &      & \text{Natural numbers}     \\[.75em]
      1  &   3  &   6  &  10  &  15  &  21  &      &      & \text{Triangle numbers}    \\[.75em]
      1  &   4  &  10  &  20  &  35  &      &      &      & \text{Tetrahedral numbers} \\[.75em]
      1  &   5  &  15  &  35  &      &      &      &      & \text{Pentalope numbers}   \\[.75em]
      1  &   6  &  21                                                                  \\[.75em]
      1  &   7                                                                         \\[.75em]
      1
  \end{array}
\]
