# Integrals

## Definition

\[
  \int_a^b f(x) \dx = \lim_{n \to \infty} \sum_{i=1}^n f(x_{i-1})\Delta x, \text{ where } \Delta x = {b-a \over n}
\]

Note: since the sum starts at $i=1$, this is a right sum (rectangles touch $f(x)$ on right). Seems pretty arbitrary to me.

## Fundamental Theorem of Calculus

\[
  \drv[F]{x} = \drv{x} \int_a^x f(t) \dt = f(x)
\]

\[
  \int_a^b f(t) \dt = F(b) - F(a)
\]

## Rules

\[
  \begin{aligned}
     \int_a^b \big(f(x) \pm g(x)\big) \dx &= \int_a^b f(x) \dx \pm \int_a^b g(x) \dx && \text{Sum/Difference}       \h7 \\
                \int_a^b c \cdot f(x) \dx &= c \cdot \int_a^b f(x) \dx               && \text{Scalar Multiple}      \h7 \\
                        \int_a^b f(x) \dx &= -\int_b^a f(x) \dx                      && \text{Reversing the limits} \h7 \\
    \int_a^b f(x) \dx + \int_b^c f(x) \dx &= \int_a^c f(x) \dx                       && \text{Concatenation}        \h7 \\
                                          &                                          && \text{Betweenness?}         \h7 \\
  \end{aligned}
\]

## Common Integrals

Always add a constant ($+ \text{ C}$)!

\[
  \begin{aligned}
                \int k \dx &= kx                         &                                                    \h7 \\
           \int x^n \dx &= {x^{n+1} \over n+1},~n \ne -1 & \int x^{-1} \dx = \int {1 \over x} \dx &= \ln|x|   \h7 \\[2em]
              \int e^x \dx &= e^x                        &            \int a^x \dx &= {a^x \over \ln a}       \h7 \\
            \int \ln x \dx &= x \ln x - x                &       \int \log_a x \dx &= x\log_a x-{x\over\ln a} \h7 \\[2em]
           \int \sin x \dx &= -\cos x                    &         \int \csc x \dx &= \ln|\csc x - \cot x|    \h7 \\
           \int \cos x \dx &= \sin x                     &         \int \sec x \dx &= \ln|\sec x + \tan x|    \h7 \\
           \int \tan x \dx &= -\ln|\cos x| = \ln|\sec x| &         \int \cot x \dx &= \ln|\sin x|             \h7 \\[2em]
         \int \sec^2 x \dx &= \tan x                     &       \int \csc^2 x \dx &= -\cot x                 \h7 \\
    \int \sec x \tan x \dx &= \sec x                     &  \int \csc x \cot x \dx &= -\csc x                 \h7 \\
  \end{aligned}
\]

## Techniques

\[
  \begin{aligned}
        \int f(x) \cdot g'(x) \dx &= f(x) \cdot g(x) - \int f'(x) \cdot g(x) \dx && \text{Integration by Parts} \h7 \\
                       \int u \dv &= uv - \int v \du                             && \text{Integration by Parts} \h7 \\
     \int f(g(x)) \cdot g'(x) \dx &= \int f(u) \du                               && \text{$u$-Substitution}     \h7 \\
    \int f'(g(x)) \cdot g'(x) \dx &= f(g(x))                                     && \text{Reverse Chain Rule}   \h7 \\
  \end{aligned}
\]

 - **Integration by Parts**: (reverse product rule) Use on products, when the derivative of one factor is simpler and the integral of the other factor becomes no more complicated. One of the factors can be $1$, as when calculating $\int \ln x \dx$.
 - **$u$-Substitution**: (reverse chain rule) Use when the derivative of some part of the expression is also part of the expression.

## Trigonometric Substitutions

\[
  \begin{aligned}
     \sqrt{a^2 - x^2} &= \sqrt{a^2 - a^2 \sin^2 θ} = a\p{^2}\cos\p{^2} θ &
                    x &= a \sin θ &
        -\tfrac{π}{2} &\le θ \le \tfrac{π}{2} &
         1 - \sin^2 θ &= \cos^2 θ                        \h4 \\
            a^2 - x^2 &= \kern{1.278em} a^2 - a^2 \sin^2 θ = a^2 \cos^2 θ &
                 \dx &= a \cos θ \dθ &
                  (-a &\le x \le a)                      \h4 \\[1em]
     \sqrt{x^2 - a^2} &= \sqrt{a^2 \sec^2 θ - a^2} = a\p{^2}\tan\p{^2} θ &
                    x &= a \sec θ &
                    0 &\le θ \lt \pc{\tfrac{3π}{2}}{\tfrac{π}{2}},\ x \gt 0 &
         \sec^2 θ - 1 &= \tan^2 θ                        \h4 \\
            x^2 - a^2 &= \kern{1.278em} a^2 \sec^2 θ - a^2 = a^2 \tan^2 θ &
                 \dx &= a \sec θ \tan θ \dθ &
                    π &\le θ \lt \tfrac{3π}{2},\ x \lt 0 \h4 \\[1em]
     \sqrt{x^2 + a^2} &= \sqrt{a^2 + a^2 \tan^2 θ} = a\p{^2}\sec\p{^2} θ &
                    x &= a \tan θ &
        -\tfrac{π}{2} &\lt θ \lt \tfrac{π}{2} &
         1 + \tan^2 θ &= \sec^2 θ                        \h4 \\
            x^2 + a^2 &= \kern{1.278em} a^2 + a^2 \tan^2 θ = a^2 \sec^2 θ &
                 \dx &= a \sec^2 θ \dθ                   \h4 \\
  \end{aligned}
\]

Example:

\[
  \begin{aligned}
    \int x^3\sqrt{9 - x^2} \dx
    &= \int x^3\sqrt{3^2 - x^2} \dx                    \h7 \\[.5em]
    &\begin{aligned}
       \krgrow{5em}{a} &= 3                                    \h3 \\[1em]
      \sqrt{3^2 - x^2} &= 3\cos θ                              \h3 \\
                     x &= 3\sin θ                              \h3 \\
                   \dx &= 3\cos θ \dθ                          \h3 \\
    \end{aligned}                                          \\[.5em]
    &= \int (3\sin θ)^3(3\cos θ)(3\cos θ \dθ)          \h7 \\
    &=  243 \int \sin^3 θ \cos^2 θ \dθ                 \h7 \\
    &=  243 \int \sin^2 θ \cos^2 θ \sin θ \dθ          \h7 \\
    &=  243 \int (1 - \cos^2 θ) \cos^2 θ   \sin θ \dθ  \h7 \\
    &= -243 \int (1 - \cos^2 θ) \cos^2 θ (-\sin θ \dθ) \h7 \\[.5em]
    &\begin{aligned}
       \krgrow{5em}{u} &= \cos θ                               \h3 \\
                   \du &= -\sin θ \dθ                          \h3 \\
    \end{aligned}                                          \\[.5em]
    &= -243 \int (1 - u^2)u^2 \du                      \h7 \\
    &= -243 \int u^2 - u^4 \du                         \h7 \\
    &= -243 \({u^3 \over 3} - {u^5 \over 5}) + C \h7       \\
    &=  243 \({u^3 \over 5} - {u^5 \over 3}) + C \h7       \\[1em]
    &\begin{aligned}
       \krgrow{5em}{x} &= 3\sin θ                              \h3 \\
                \sin θ &= \tfrac{x}{3}                         \h3 \\[1em]
                     u &= \cos θ                               \h3 \\
                       &= \sqrt{1 - \sin^2 θ}                  \h3 \\
                       &= \sqrt{1 - \big(\tfrac{x}{3} \big)^2} \h3 \\
                       &= \sqrt{1 - \tfrac{x^2}{9}}            \h3 \\
                       &= \big(1 - \tfrac{x^2}{9} \big)^{1/2}  \h3 \\
    \end{aligned}                                          \\[1em]
    &= 243 \(\vc{{\(1 - {x^2 \over 9})^{5/2} \over 5}
               - {\(1 - {x^2 \over 9})^{3/2} \over 3}}) + C
  \end{aligned}
\]

## Improper Integrals

Example:

\[
  \begin{aligned}
    \int_1^\infty {1 \over x^2} \dx &= \lim_{n\to\infty} \int_1^n {1 \over x^2} \dx \h7 \\
                                    &= \lim_{n\to\infty} \[-\!{1 \over x}]_1^n      \h7 \\
                                    &= \lim_{n\to\infty} \[-\!{1 \over n} - -1]     \h7 \\
                                    &= \lim_{n\to\infty} \[1 - {1 \over n}]         \h7 \\
                                    &= 1                                            \h7 \\
  \end{aligned}
\]

Example:

\[
  \begin{aligned}
       \int_{-\infty}^\infty {250 \over 25+x^2} \dx
    &= \int_{-\infty}^0 {250 \over 25+x^2} \dx + \int_0^\infty {250 \over 25+x^2} \dx                         \h7 \\
    &= \lim_{n\to-\infty} \int_n^0 {250 \over 25+x^2} \dx + \lim_{m\to\infty} \int_0^m {250 \over 25+x^2} \dx \h7 \\
    &= \cdots \h7 \\
  \end{aligned}
\]
