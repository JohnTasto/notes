# Combinatorics

## Factorial rules
\[
  \begin{aligned}
                   0! &= 1                               \\
                   1! &= 1                               \\[1em]
                   n! &= \prod_{n=1}^k k                 \\
                      &=  n(n-1)(n-2)\cdots(2)(1)        \\
                  n!! &= n(n-2)(n-4)\cdots               \\
                 n!!! &= n(n-3)(n-6)\cdots               \\[1em]
               (n+1)! &= n \cdot n!                      \\[1em]
    {n! \over (n+m)!} &= {1 \over (n+1)(n+2)\cdots(n+m)} \\[1em]
    {n! \over (n-m)!} &= (n)(n-1)(n-2)\cdots(n-m+1)      \\
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
    P(n,k) =\ _nP_k &= (n)(n-1)(n-2)\cdots(n-k+1) \\[1em]
                    &= {n! \over (n-k)!}          \\[1em]
  \end{aligned}
\]

## Combinations

Combinations are the number of ways to choose $k$ objects out of $n$ when order does not matter.

With repetition:
\[
  \binom{k+n-1}{k} = {(k+n-1)! \over k!(n-1)!}
\]

Without repetition:
\[
  \begin{aligned}
    C(n,k) =\ _nC_k = \binom{n}{k} &= {(n)(n-1)(n-2)\cdots(n-k+1) \over k!} \\[1em]
                                   &= {_nP_k \over k!}                      \\[1em]
                                   &= {n! \over k!(n-k)!}                   \\[1em]
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
                                       \cem3{1}                                     \\[.5em]
                                  \cem3{1}  \cem3{1}                                \\[.5em]
                             \cem3{1}  \cem3{2}  \cem3{1}                           \\[.5em]
                        \cem3{1}  \cem3{3}  \cem3{3}  \cem3{1}                      \\[.5em]
                   \cem3{1}  \cem3{4}  \cem3{6}  \cem3{4}  \cem3{1}                 \\[.5em]
              \cem3{1}  \cem3{5} \cem3{10} \cem3{10}  \cem3{5}  \cem3{1}            \\[.5em]
         \cem3{1}  \cem3{6} \cem3{15} \cem3{20} \cem3{15}  \cem3{6}  \cem3{1}       \\[.5em]
    \cem3{1}  \cem3{7} \cem3{21} \cem3{35} \cem3{35} \cem3{21}  \cem3{7}  \cem3{1}
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
