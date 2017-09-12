# Integrals

## Definition

\[
  \newcommand\bs{\vpppp}
  \newcommand\ls{\vpp}
  \int_a^b f(x) \d x = \lim_{n \to \infty} \sum_{i=1}^n f(x_{i-1})\Delta x, \text{ where } \Delta x = {b-a \over n}
\]

Note: since the sum starts at $i=1$, this is a right sum (rectangles touch $f(x)$ on right). Seems pretty arbitrary to me.

## Fundamental Theorem of Calculus

\[
  \drv{F}{x} = \drv{}{x} \int_a^x f(t)~\d t = f(x)
\]

\[
  \int_a^b f(t)~\d t = F(b) - F(a)
\]

## Rules

\[
  \begin{aligned}
    \int_a^b \big(f(x) \pm g(x)\big) \d x &= \int_a^b f(x) \d x \pm \int_a^b g(x) \d x && \text{Sum/Difference}       \bs \\
               \int_a^b c \cdot f(x) \d x &= c \cdot \int_a^b f(x) \d x                && \text{Scalar Multiple}      \bs \\
                       \int_a^b f(x) \d x &= -\int_b^a f(x) \d x                       && \text{Reversing the limits} \bs \\
  \int_a^b f(x) \d x + \int_b^c f(x) \d x &= \int_a^c f(x) \d x                        && \text{Concatenation}        \bs \\
                                          &                                            && \text{Betweenness?}         \bs \\
  \end{aligned}
\]

## Common Integrals

Always add a constant ($+ \text{ C}$)!

\[
  \begin{aligned}
                \int k \d x &= kx                         & \int \ln??                                         \bs \\
           \int x^n \d x &= {x^{n+1} \over n+1},~n \ne -1 & \int x^{-1} \d x = \int {1 \over x} \d x &= \ln|x| \bs \\
              \int e^x \d x &= e^x                        &            \int a^x \d x &= {a^x \over \ln a}      \bs \\[3em]
           \int \sin x \d x &= -\cos x                    &         \int \csc x \d x &= \ln|\csc x - \cot x|   \bs \\
           \int \cos x \d x &= \sin x                     &         \int \sec x \d x &= \ln|\sec x + \tan x|   \bs \\
           \int \tan x \d x &= -\ln|\cos x| = \ln|\sec x| &         \int \cot x \d x &= \ln|\sin x|            \bs \\
         \int \sec^2 x \d x &= \tan x                     &       \int \csc^2 x \d x &= -\cot x                \bs \\
    \int \sec x \tan x \d x &= \sec x                     &  \int \csc x \cot x \d x &= -\csc x                \bs \\
  \end{aligned}
\]

## Techniques

\[
  \begin{aligned}
        \int f(x) \cdot g'(x) \d x &= f(x) \cdot g(x) - \int f'(x) \cdot g(x) \d x && \text{Integration by Parts} \bs \\
                       \int u~\d v &= uv - \int v~\d u                             && \text{Integration by Parts} \bs \\
     \int f(g(x)) \cdot g'(x) \d x &= \int f(u)~\d u                               && \text{$u$-Substitution}     \bs \\
    \int f'(g(x)) \cdot g'(x) \d x &= f(g(x))                                      && \text{Reverse Chain Rule}   \bs \\
  \end{aligned}
\]

 - **Integration by Parts**: (reverse product rule) Use on products, when the derivative of one factor is simpler and the integral of the other factor becomes no more complicated. One of the factors can be $1$, as when calculating $\int \ln x \d x$.
 - **$u$-Substitution**: (reverse chain rule) Use when the derivative of some part of the expression is also part of the expression.

## Trigonometric Substitutions

\[
  \begin{aligned}
     \sqrt{a^2 - x^2} &= \sqrt{a^2 - a^2 \sin^2 θ} = a\p{^2}\cos\p{^2} θ &
                    x &= a \sin θ &
        -\tfrac{π}{2} &\le θ \le \tfrac{π}{2} &
         1 - \sin^2 θ &= \cos^2 θ                        \ls \\
            a^2 - x^2 &= \kern{1.278em} a^2 - a^2 \sin^2 θ = a^2 \cos^2 θ &
                 \d x &= a \cos θ ~\d θ &
                  (-a &\le x \le a)                      \ls \\[1em]
     \sqrt{x^2 - a^2} &= \sqrt{a^2 \sec^2 θ - a^2} = a\p{^2}\tan\p{^2} θ &
                    x &= a \sec θ &
                    0 &\le θ \lt \lgrowp{\kern{.155em}\tfrac{π}{2}}{\tfrac{3π}{2}},\ x \gt 0 &
         \sec^2 θ - 1 &= \tan^2 θ                        \ls \\
            x^2 - a^2 &= \kern{1.278em} a^2 \sec^2 θ - a^2 = a^2 \tan^2 θ &
                 \d x &= a \sec θ \tan θ ~\d θ &
                    π &\le θ \lt \tfrac{3π}{2},\ x \lt 0 \ls \\[1em]
     \sqrt{x^2 + a^2} &= \sqrt{a^2 + a^2 \tan^2 θ} = a\p{^2}\sec\p{^2} θ &
                    x &= a \tan θ &
        -\tfrac{π}{2} &\lt θ \lt \tfrac{π}{2} &
         1 + \tan^2 θ &= \sec^2 θ                        \ls \\
            x^2 + a^2 &= \kern{1.278em} a^2 + a^2 \tan^2 θ = a^2 \sec^2 θ &
                 \d x &= a \sec^2 θ ~\d θ                \ls \\
  \end{aligned}
\]

Example:

\[
  \begin{aligned}
    \int x^3\sqrt{9 - x^2} \d x
    &= \int x^3\sqrt{3^2 - x^2} \d x                      \bs \\[.5em]
    &\begin{aligned}
        \rgrow{5em}{a} &= 3                                    \ls \\[1em]
      \sqrt{3^2 - x^2} &= 3\cos θ                              \ls \\
                     x &= 3\sin θ                              \ls \\
                  \d x &= 3\cos θ ~\d θ                        \ls \\
    \end{aligned}                                              \\[.5em]
    &= \int (3\sin θ)^3(3\cos θ)(3\cos θ ~\d θ)            \bs \\
    &=  243 \int \sin^3 θ \cos^2 θ ~\d θ                   \bs \\
    &=  243 \int \sin^2 θ \cos^2 θ \sin θ ~\d θ            \bs \\
    &=  243 \int (1 - \cos^2 θ) \cos^2 θ   \sin θ ~\d θ    \bs \\
    &= -243 \int (1 - \cos^2 θ) \cos^2 θ (-\sin θ ~\d θ)   \bs \\[.5em]
    &\begin{aligned}
        \rgrow{5em}{u} &= \cos θ                               \ls \\
                  \d u &= -\sin θ ~\d θ                        \ls \\
    \end{aligned}                                            \\[.5em]
    &= -243 \int (1 - u^2)u^2 ~\d u                        \bs \\
    &= -243 \int u^2 - u^4 ~\d u                           \bs \\
    &= -243 \bigg({u^3 \over 3} - {u^5 \over 5} \bigg) + C \bs \\
    &=  243 \bigg({u^3 \over 5} - {u^5 \over 3} \bigg) + C \bs \\[1em]
    &\begin{aligned}
        \rgrow{5em}{x} &= 3\sin θ                              \ls \\
                \sin θ &= \tfrac{x}{3}                         \ls \\[1em]
                     u &= \cos θ                               \ls \\
                       &= \sqrt{1 - \sin^2 θ}                  \ls \\
                       &= \sqrt{1 - \big(\tfrac{x}{3} \big)^2} \ls \\
                       &= \sqrt{1 - \tfrac{x^2}{9}}            \ls \\
                       &= \big(1 - \tfrac{x^2}{9} \big)^{1/2}  \ls \\
    \end{aligned}                                              \\[1em]
    &= 243 \Bigg({\big(1 - {x^2 \over 9} \big)^{5/2} \over 5} - {\big(1 - {x^2 \over 9} \big)^{3/2} \over 3} \Bigg) + C
  \end{aligned}
\]

## Improper Integrals

Example:

\[
  \begin{aligned}
    \int_1^\infty {1 \over x^2} \d x &= \lim_{n\to\infty} \int_1^n {1 \over x^2} \d x      \bs \\
                                      &= \lim_{n\to\infty} \bigg[-\!{1 \over x}\bigg]_1^n  \bs \\
                                      &= \lim_{n\to\infty} \bigg[-\!{1 \over n} - -1\bigg] \bs \\
                                      &= \lim_{n\to\infty} \bigg[1 - {1 \over n}\bigg]     \bs \\
                                      &= 1                                                 \bs \\
  \end{aligned}
\]

Example:

\[
  \begin{aligned}
       \int_{-\infty}^\infty {250 \over 25+x^2} \d x
    &= \int_{-\infty}^0 {250 \over 25+x^2} \d x + \int_0^\infty {250 \over 25+x^2} \d x                         \bs \\
    &= \lim_{n\to-\infty} \int_n^0 {250 \over 25+x^2} \d x + \lim_{m\to\infty} \int_0^m {250 \over 25+x^2} \d x \bs \\
    &= \cdots \bs \\
  \end{aligned}
\]
