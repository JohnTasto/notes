# Polynomial Division

If we know one factor of a polynomial, we can divide the two to find the other factor.

## Long Division

\[
  \newcommand\ls{\vp}
  \begin{aligned}
                                        x^2 + 2x - 1 - \tfrac{7}{3x - 2}     \ls \\[-.1em]
    3x - 2 ~\enclose{longdiv}{ ~3x^3 + 4x^2 - 7x - 5 }         \kern{3.13em} \ls \\[.25em]
               \underline{{} - (3x^3 - 2x^2 )}                 \kern{6.81em} \ls \\[.15em]
                                       6x^2 - 7x               \kern{4.94em} \ls \\[.25em]
                      \underline{{} - (6x^2 - 4x)}             \kern{4.53em} \ls \\[.15em]
                                             -3x - 5           \kern{3.24em} \ls \\[.25em]
                            \underline{{} - (-3x + 2)}         \kern{2.83em} \ls \\[.15em]
                                              {} - 7           \kern{3.24em} \ls \\
  \end{aligned}
\]

## Synthetic Division

[Look it up...](https://chilimath.com/lessons/intermediate-algebra/synthetic-division/)
