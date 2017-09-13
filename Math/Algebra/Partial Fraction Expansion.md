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
    {x^2 - 2x - 37 \over x^2 - 3x - 40} &= 1 + {x+3 \over x^2 - 3x - 40}                            \h7 \\
                                        &= 1 + {x+3 \over (x+5)(x-8)}                               \h7 \\[1em]
                 {x+3 \over (x+5)(x-8)} &= {A \over x+5} + {B \over x-8}                            \h7 \\
                                        &= {A(x-8) + B(x+5) \over (x+5)(x-8)}                       \h7 \\[1em]
                                  x + 3 &= A(x-8) + B(x+5)                                          \h3 \\[1em]
    \text{Pick $x$ that makes}&\text{ $B$ disappear:}                                               \h3 \\
                               (-5) + 3 &= A((-5)-8) + B((-5)+5)                                    \h3 \\
                                     -2 &= -13A                                                     \h3 \\
                                      A &= \tfrac{2}{13}                                            \h3 \\[1em]
    \text{Pick $x$ that makes}&\text{ $A$ disappear:}                                               \h3 \\
                                (8) + 3 &= A((8)-8) + B((8)+5)                                      \h3 \\
                                     11 &= 13B                                                      \h3 \\
                                      B &= \tfrac{11}{13}                                           \h3 \\[1em]
    {x^2 - 2x - 37 \over x^2 - 3x - 40} &= 1 + {\frac{2}{13} \over x+5} + {\frac{11}{13} \over x-8} \h7 \\
  \end{aligned}
\]

## Example

\[
  \begin{aligned}
    {10x^2 + 12x + 20 \over x^3 - 8} &= {10x^2 + 12x + 20 \over (x-2)(x^2 + 2x +4)}                \h7 \\
                                     &= {A \over x-2} + {Bx+C \over x^2 + 2x + 4}                  \h7 \\
                                     &= {A(x^2 + 2x + 4) + (Bx+C)(x-2)  \over  (x-2)(x^2 + 2x +4)} \h7 \\[1em]
                    10x^2 + 12x + 20 &= A(x^2 + 2x + 4) + (Bx+C)(x-2)                              \h3 \\[1em]
    \text{Pick $x$ that makes $B$ and}&\text{ $C$ disappear:}                                      \h3 \\
                10(2)^2 + 12(2) + 20 &= A((2)^2 + 2(2) + 4) + (B(2)+C)((2)-2)                      \h3 \\
                        40 + 24 + 20 &= A(4 + 4 + 4)                                               \h3 \\
                                  84 &= 12A                                                        \h3 \\
                                   A &= 7                                                          \h3 \\[1em]
    \text{Substitute known value for $A$ and pick $x$ that makes}&\text{ $B$ disappear:}           \h3 \\
                10(0)^2 + 12(0) + 20 &= (7)((0)^2 + 2(0) + 4) + (B(0)+C)((0)-2)                    \h3 \\
                                  20 &= 28 - 2C                                                    \h3 \\
                                  -8 &= -2C                                                        \h3 \\
                                   C &= 4                                                          \h3 \\[1em]
    \text{Substitute known value for $A$ and $C$ and pick $x$ that simplifi}&\text{es arithmetic:} \h3 \\
                10(1)^2 + 12(1) + 20 &= (7)((1)^2 + 2(1) + 4) + (B(1)+(4))((1)-2)                  \h3 \\
                        10 + 12 + 20 &= 7(7) + (B + 4)(-1)                                         \h3 \\
                                  42 &= 49 - B - 4                                                 \h3 \\
                                  42 &= 45 - B                                                     \h3 \\
                                   B &= -3                                                         \h3 \\[1em]
    {10x^2 + 12x + 20 \over x^3 - 8} &= {7 \over x-2} + {-3x+4 \over x^2 + 2x + 4}                 \h3 \\
  \end{aligned}
\]

## Example

\[
  \begin{aligned}
    {6x^2 - 19x + 15 \over (x-1)(x-2)^2} &= {A \over x-1} + {B \over x-2} + {C \over (x-2)^2}      \h7 \\
                                         &= {A(x-2)^2 + B(x-1)(x-2) + C(x-1)  \over  (x-1)(x-2)^2} \h7 \\[1em]
                         6x^2 - 19x + 15 &= A(x-2)^2 + B(x-1)(x-2) + C(x-1)                        \h3 \\[1em]
    \text{Pick $x$ that makes $A$ and}&\text{ $B$ disappear:}                                      \h3 \\
                     6(2)^2 - 19(2) + 15 &= A((2)-2)^2 + B((2)-1)((2)-2) + C((2)-1)                \h3 \\
                            24 - 38 + 15 &= C                                                      \h3 \\
                                       C &= 1                                                      \h3 \\[1em]
    \text{Pick $x$ that makes $B$ and}&\text{ $C$ disappear:}                                      \h3 \\
                     6(1)^2 - 19(1) + 15 &= A((1)-2)^2 + B((1)-1)((1)-2) + C((1)-1)                \h3 \\
                             6 - 19 + 15 &= A                                                      \h3 \\
                                       A &= 2                                                      \h3 \\[1em]
    \text{Substitute known value for $A$ and $C$ and pick $x$ that simplifi}&\text{es arithmetic:} \h3 \\
                     6(0)^2 - 19(0) + 15 &= (2)((0)-2)^2 + B((0)-1)((0)-2) + (1)((0)-1)            \h3 \\
                                      15 &= 2\cdot4 + 2B - 1                                       \h3 \\
                                      15 &= 7 + 2B                                                 \h3 \\
                                       8 &= 2B                                                     \h3 \\
                                       B &= 4                                                      \h3 \\[1em]
    {6x^2 - 19x + 15 \over (x-1)(x-2)^2} &= {2 \over x-1} + {4 \over x-2} + {1 \over (x-2)^2}      \h7 \\
  \end{aligned}
\]
