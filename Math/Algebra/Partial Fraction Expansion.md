# Partial Fraction Expansion

Numerator must have a lower degree than the denominator. If it isn't, try dividing polynomials.

## Fraction addition

General:

\[
  \frac{A}{C} + \frac{B}{D} = \frac{AD}{CD} + \frac{BC}{CD} = \frac{AD+BC}{CD}
\]

Denominators containing powers of binomials (see last example):

\[
  \sum_{k=1}^n {A_k \over (x-a)^k}
= {A_1 \over (x-a)} + {A_2 \over (x-a)^2} + \ldots + {A_n \over (x-a)^n}
= {\text{polynomial} \over (x-a)^n}
\]

## Example

\[
  \begin{aligned}
    {x^2 - 2x - 37 \over x^2 - 3x - 40} &= 1 + {x+3 \over x^2 - 3x - 40}                            \BG \\
                                        &= 1 + {x+3 \over (x+5)(x-8)}                               \BG \\[1em]
                 {x+3 \over (x+5)(x-8)} &= {A \over x+5} + {B \over x-8}                            \BG \\
                                        &= {A(x-8) + B(x+5) \over (x+5)(x-8)}                       \BG \\[1em]
                                  x + 3 &= A(x-8) + B(x+5)                                          \Bg \\[1em]
    \text{Pick $x$ that makes}&\text{ $B$ disappear:}                                               \Bg \\
                               (-5) + 3 &= A((-5)-8) + B((-5)+5)                                    \Bg \\
                                     -2 &= -13A                                                     \Bg \\
                                      A &= \tfrac{2}{13}                                            \Bg \\[1em]
    \text{Pick $x$ that makes}&\text{ $A$ disappear:}                                               \Bg \\
                                (8) + 3 &= A((8)-8) + B((8)+5)                                      \Bg \\
                                     11 &= 13B                                                      \Bg \\
                                      B &= \tfrac{11}{13}                                           \Bg \\[1em]
    {x^2 - 2x - 37 \over x^2 - 3x - 40} &= 1 + {\frac{2}{13} \over x+5} + {\frac{11}{13} \over x-8} \BG \\
  \end{aligned}
\]

## Example

\[
  \begin{aligned}
    {10x^2 + 12x + 20 \over x^3 - 8} &= {10x^2 + 12x + 20 \over (x-2)(x^2 + 2x +4)}                \BG \\
                                     &= {A \over x-2} + {Bx+C \over x^2 + 2x + 4}                  \BG \\
                                     &= {A(x^2 + 2x + 4) + (Bx+C)(x-2)  \over  (x-2)(x^2 + 2x +4)} \BG \\[1em]
                    10x^2 + 12x + 20 &= A(x^2 + 2x + 4) + (Bx+C)(x-2)                              \Bg \\[1em]
    \text{Pick $x$ that makes $B$ and}&\text{ $C$ disappear:}                                      \Bg \\
                10(2)^2 + 12(2) + 20 &= A((2)^2 + 2(2) + 4) + (B(2)+C)((2)-2)                      \Bg \\
                        40 + 24 + 20 &= A(4 + 4 + 4)                                               \Bg \\
                                  84 &= 12A                                                        \Bg \\
                                   A &= 7                                                          \Bg \\[1em]
    \text{Substitute known value for $A$ and pick $x$ that makes}&\text{ $B$ disappear:}           \Bg \\
                10(0)^2 + 12(0) + 20 &= (7)((0)^2 + 2(0) + 4) + (B(0)+C)((0)-2)                    \Bg \\
                                  20 &= 28 - 2C                                                    \Bg \\
                                  -8 &= -2C                                                        \Bg \\
                                   C &= 4                                                          \Bg \\[1em]
    \text{Substitute known value for $A$ and $C$ and pick $x$ that simplifi}&\text{es arithmetic:} \Bg \\
                10(1)^2 + 12(1) + 20 &= (7)((1)^2 + 2(1) + 4) + (B(1)+(4))((1)-2)                  \Bg \\
                        10 + 12 + 20 &= 7(7) + (B + 4)(-1)                                         \Bg \\
                                  42 &= 49 - B - 4                                                 \Bg \\
                                  42 &= 45 - B                                                     \Bg \\
                                   B &= -3                                                         \Bg \\[1em]
    {10x^2 + 12x + 20 \over x^3 - 8} &= {7 \over x-2} + {-3x+4 \over x^2 + 2x + 4}                 \Bg \\
  \end{aligned}
\]

## Example

\[
  \begin{aligned}
    {6x^2 - 19x + 15 \over (x-1)(x-2)^2} &= {A \over x-1} + {B \over x-2} + {C \over (x-2)^2}      \BG \\
                                         &= {A(x-2)^2 + B(x-1)(x-2) + C(x-1)  \over  (x-1)(x-2)^2} \BG \\[1em]
                         6x^2 - 19x + 15 &= A(x-2)^2 + B(x-1)(x-2) + C(x-1)                        \Bg \\[1em]
    \text{Pick $x$ that makes $A$ and}&\text{ $B$ disappear:}                                      \Bg \\
                     6(2)^2 - 19(2) + 15 &= A((2)-2)^2 + B((2)-1)((2)-2) + C((2)-1)                \Bg \\
                            24 - 38 + 15 &= C                                                      \Bg \\
                                       C &= 1                                                      \Bg \\[1em]
    \text{Pick $x$ that makes $B$ and}&\text{ $C$ disappear:}                                      \Bg \\
                     6(1)^2 - 19(1) + 15 &= A((1)-2)^2 + B((1)-1)((1)-2) + C((1)-1)                \Bg \\
                             6 - 19 + 15 &= A                                                      \Bg \\
                                       A &= 2                                                      \Bg \\[1em]
    \text{Substitute known value for $A$ and $C$ and pick $x$ that simplifi}&\text{es arithmetic:} \Bg \\
                     6(0)^2 - 19(0) + 15 &= (2)((0)-2)^2 + B((0)-1)((0)-2) + (1)((0)-1)            \Bg \\
                                      15 &= 2\cdot4 + 2B - 1                                       \Bg \\
                                      15 &= 7 + 2B                                                 \Bg \\
                                       8 &= 2B                                                     \Bg \\
                                       B &= 4                                                      \Bg \\[1em]
    {6x^2 - 19x + 15 \over (x-1)(x-2)^2} &= {2 \over x-1} + {4 \over x-2} + {1 \over (x-2)^2}      \BG \\
  \end{aligned}
\]
