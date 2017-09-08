# Integrals

## Definition

\[
  \int_a^b f(x)~dx = \lim_{n \to \infty} \sum_{i=1}^n f(x_{i-1})\Delta x, \text{ where } \Delta x = \frac{b-a}{n}
\]

Note: since the sum starts at $i=1$, this is a right sum (rectangles touch $f(x)$ on right). Seems pretty arbitrary to me.

## Fundamental Theorem of Calculus

\[
  \frac{dF}{dx} = \frac{d}{dx} \int_a^x f(t)~dt = f(x)
\]

\[
  \int_a^b f(t)~dt = F(b) - F(a)
\]

## Rules

\[
  \begin{aligned}
    \int_a^b \big(f(x) \pm g(x)\big)~dx &= \int_a^b f(x)~dx \pm \int_a^b g(x)~dx   && \text{Sum/Difference}       \\[1em]
               \int_a^b c \cdot f(x)~dx &= c \cdot \int_a^b f(x)~dx                && \text{Scalar Multiple}      \\[1em]
                       \int_a^b f(x)~dx &= -\int_b^a f(x)~dx                       && \text{Reversing the limits} \\[1em]
    \int_a^b f(x)~dx + \int_b^c f(x)~dx &= \int_a^c f(x)~dx                        && \text{Concatenation}        \\[1em]
                                        &                                          && \text{Betweenness?}
  \end{aligned}
\]

## Common Integrals

Always add a constant ($+ \text{ C}$)!

\[
  \begin{aligned}
                \int k~dx &= kx                         & \int \ln?? \\[1em]
           \int x^n~dx &= \frac{x^{n+1}}{n+1},~n \ne -1 & \int x^{-1}~dx = \int \frac{1}{x}~dx &= \ln|x| \\[1em]
              \int e^x~dx &= e^x                        &            \int a^x~dx &= \frac{a^x}{\ln a}    \\[3em]
           \int \sin x~dx &= -\cos x                    &         \int \csc x~dx &= \ln|\csc x - \cot x| \\[1em]
           \int \cos x~dx &= \sin x                     &         \int \sec x~dx &= \ln|\sec x + \tan x| \\[1em]
           \int \tan x~dx &= -\ln|\cos x| = \ln|\sec x| &         \int \cot x~dx &= \ln|\sin x|          \\[1em]
         \int \sec^2 x~dx &= \tan x                     &       \int \csc^2 x~dx &= -\cot x              \\[1em]
    \int \sec x \tan x~dx &= \sec x                     &  \int \csc x \cot x~dx &= -\csc x              \\[1em]
  \end{aligned}
\]

## Techniques

\[
  \begin{aligned}
        \int f(x) \cdot g'(x)~dx &= f(x) \cdot g(x) - \int f'(x) \cdot g(x)~dx && \text{Integration by Parts} \\[1em]
                       \int u~dv &= uv - \int v~du                             && \text{Integration by Parts} \\[1em]
     \int f(g(x)) \cdot g'(x)~dx &= \int f(u)~du                               && \text{$u$-Substitution}     \\[1em]
    \int f'(g(x)) \cdot g'(x)~dx &= f(g(x))                                    && \text{Reverse Chain Rule}
  \end{aligned}
\]

 - **Integration by Parts**: (reverse product rule) Use on products, when the derivative of one factor is simpler and the integral of the other factor becomes no more complicated. One of the factors can be $1$, as when calculating $\int \ln x~dx$.
 - **$u$-Substitution**: (reverse chain rule) Use when the derivative of some part of the expression is also part of the expression.

## Trigonometric Substitutions

\[
  \begin{aligned}
     \sqrt{a^2 - x^2} &= \sqrt{a^2 - a^2 \sin^2 θ} = a\phantom{^2}\cos\phantom{^2} θ &
                    x &= a \sin θ &
        -\tfrac{π}{2} &\le θ \le \tfrac{π}{2} &
         1 - \sin^2 θ &= \cos^2 θ                        \\
            a^2 - x^2 &= \kern{1.278em} a^2 - a^2 \sin^2 θ = a^2 \cos^2 θ &
                   dx &= a \cos θ~dθ &
                  (-a &\le x \le a)                      \\[1em]
     \sqrt{x^2 - a^2} &= \sqrt{a^2 \sec^2 θ - a^2} = a\phantom{^2}\tan\phantom{^2} θ &
                    x &= a \sec θ &
                    0 &\le θ \lt \rlap{\kern{.155em}\tfrac{π}{2}}{\phantom{\tfrac{3π}{2}}},\ x \gt 0 &
         \sec^2 θ - 1 &= \tan^2 θ                        \\
            x^2 - a^2 &= \kern{1.278em} a^2 \sec^2 θ - a^2 = a^2 \tan^2 θ &
                   dx &= a \sec θ \tan θ~dθ &
                    π &\le θ \lt \tfrac{3π}{2},\ x \lt 0 \\[1em]
     \sqrt{x^2 + a^2} &= \sqrt{a^2 + a^2 \tan^2 θ} = a\phantom{^2}\sec\phantom{^2} θ &
                    x &= a \tan θ &
        -\tfrac{π}{2} &\lt θ \lt \tfrac{π}{2} &
         1 + \tan^2 θ &= \sec^2 θ                        \\
            x^2 + a^2 &= \kern{1.278em} a^2 + a^2 \tan^2 θ = a^2 \sec^2 θ &
                   dx &= a \sec^2 θ~dθ
  \end{aligned}
\]

Example:

\[
  \begin{aligned}
    \int x^3\sqrt{9 - x^2} ~dx
    &= \int x^3\sqrt{3^2 - x^2} ~dx                        \\[1em]
    &\begin{aligned}
            \kern{4em}                                         \\[-1em]
                     a &= 3                                    \\[1em]
      \sqrt{3^2 - x^2} &= 3\cos θ                              \\
                     x &= 3\sin θ                              \\
                    dx &= 3\cos θ ~dθ                          \\
    \end{aligned}                                          \\
    &= \int (3\sin θ)^3(3\cos θ)(3\cos θ ~dθ)              \\
    &=  243 \int \sin^3 θ \cos^2 θ ~dθ                     \\
    &=  243 \int \sin^2 θ \cos^2 θ \sin θ ~dθ              \\
    &=  243 \int (1 - \cos^2 θ) \cos^2 θ   \sin θ ~dθ      \\
    &= -243 \int (1 - \cos^2 θ) \cos^2 θ (-\sin θ ~dθ)     \\[1em]
    &\begin{aligned}
      \kern{4em}                                               \\[-1em]
      u &= \cos θ                                              \\
      du &= -\sin θ ~dθ                                        \\
    \end{aligned}                                          \\
    &= -243 \int (1 - u^2)u^2 ~du                          \\
    &= -243 \int u^2 - u^4 ~du                             \\
    &= -243 \bigg(\frac{u^3}{3} - \frac{u^5}{5} \bigg) + C \\[1em]
    &=  243 \bigg(\frac{u^3}{5} - \frac{u^5}{3} \bigg) + C \\[1em]
    &\begin{aligned}
            \kern{4em}                                         \\[-1em]
                     x &= 3\sin θ                              \\
                \sin θ &= \tfrac{x}{3}                         \\[1em]
                     u &= \cos θ                               \\
                       &= \sqrt{1 - \sin^2 θ}                  \\
                       &= \sqrt{1 - \big(\tfrac{x}{3} \big)^2} \\
                       &= \sqrt{1 - \tfrac{x^2}{9}}            \\
                       &= \Big(1 - \tfrac{x^2}{9} \Big)^{1/2}  \\
    \end{aligned}                                          \\
    &= 243 \Bigg(\frac{\Big(1 - \frac{x^2}{9} \Big)^{5/2}}{5} - \frac{\Big(1 - \frac{x^2}{9} \Big)^{3/2}}{3} \Bigg) + C
  \end{aligned}
\]

## Improper Integrals

### Example

\[
  \begin{aligned}
  \int_1^\infty \frac{1}{x^2} ~dx &= \lim_{n\to\infty} \int_1^n \frac{1}{x^2} ~dx      \\[1em]
                                  &= \lim_{n\to\infty} \bigg[-\!\frac{1}{x}\bigg]_1^n  \\[1em]
                                  &= \lim_{n\to\infty} \bigg[-\!\frac{1}{n} - -1\bigg] \\[1em]
                                  &= \lim_{n\to\infty} \bigg[1 - \frac{1}{n}\bigg]     \\[1em]
                                  &= 1
  \end{aligned}
\]

### Example

\[
  \begin{aligned}
    \int_{-\infty}^\infty \frac{250}{25+x^2} ~dx
 &= \int_{-\infty}^0 \frac{250}{25+x^2} ~dx + \int_0^\infty \frac{250}{25+x^2} ~dx \\[1em]
 &= \lim_{n\to-\infty} \int_n^0 \frac{250}{25+x^2} ~dx + \lim_{m\to\infty} \int_0^m \frac{250}{25+x^2} ~dx \\[1em]
 &\ldots
  \end{aligned}
\]
