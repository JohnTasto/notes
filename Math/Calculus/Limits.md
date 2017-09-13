# Limits

## Rules

\[
  \newcommand\cs{\pf{\tf{0^0}}{\tf{0^0}}}
  \begin{aligned}
    \lim_{x \to a} \big(f(x) \pm g(x) \big) &= \lim_{x \to a} f(x) \pm \lim_{x \to a} g(x)
          && \text{Sum/Difference}  \BG \\
    \lim_{x \to a} \big( c \cdot f(x) \big) &= c \cdot \lim_{x \to a} f(x)
          && \text{Scalar Multiple} \BG \\
             \lim_{x \to a} f(x) \cdot g(x) &= \lim_{x \to a} f(x) \cdot \lim_{x \to a} g(x)
          && \text{Product}         \BG \\
           \lim_{x \to a} {f(x) \over g(x)} &= {\lim_{x \to a} f(x) \over \lim_{x \to a} g(x)}
          && \text{Quotient}        \BG \\
  \end{aligned}
\]

## Useful Limits

\[
  \begin{aligned}
    \lim_{x \to 0} {x \over \sin x} = &\lim_{x \to 0} {\sin x \over x} = 1     \BG \\
    \lim_{x \to 0} {\cos x - 1 \over x} = &\lim_{x \to 0} {1 - \cos x \over x} = 0
          && \text{Both work, I checked}                                       \BG \\
    &\lim_{x \to 0} {1 - \cos x \over x^2} = \frac12
          && \text{Don't know about the other here...}                         \BG \\
    &\lim_{x \to n^\pm} \tan \Big(π x + \fracπ2 \Big) = \mp\infty
          && \forall n ~|~ n \in \mathbb{N} \qquad\text{(according to Google)} \BG \\
    &\lim_{x \to 0} x^ne^{-x} = 0
          && \forall n                                                         \BG \\
  \end{aligned}
\]

## Indeterminate Forms

\[
  \begin{aligned}
    \text{Form} \;\, &&
    \text{Condit} & \text{ion} &
    \text{Condit} & \text{ion} &
    \text{Transfor} & \text{mation to}~ \tfrac00 &
    \text{Transfor} & \text{mation to}~ \tfrac\infty\infty & \cs \\
    {0 \over 0}           \;\;\;\:\, && \lim_{x \to c} f(x) &= 0      & \lim_{x \to c} g(x) &= 0      &
                                     &                                                                &
    \lim_{x \to c} {f(x) \over g(x)} &=      \lim_{x \to c} {{1 \over g(x)} \over {1 \over   f(x)  }} \cs \\
    {\infty \over \infty} \;\;\;\,   && \lim_{x \to c} f(x) &= \infty & \lim_{x \to c} g(x) &= \infty &
    \lim_{x \to c} {f(x) \over g(x)} &=      \lim_{x \to c} {{1 \over g(x)} \over {1 \over   f(x)  }} &
                                     &                                                                \cs \\
    0\cdot\infty          \;\,       && \lim_{x \to c} f(x) &= 0      & \lim_{x \to c} g(x) &= \infty &
    \lim_{x \to c}       f(x)  g(x)  &=      \lim_{x \to c} {    f(x)       \over {1 \over   g(x)  }} &
    \lim_{x \to c}       f(x)  g(x)  &=      \lim_{x \to c} {    g(x)       \over {1 \over   f(x)  }} \cs \\
    \infty - \infty                  && \lim_{x \to c} f(x) &= \infty & \lim_{x \to c} g(x) &= \infty &
    \lim_{x \to c}     (f(x) - g(x)) &= \lim_{x \to c} {{1 \over g(x)} - {1 \over f(x)} \over {1 \over f(x)g(x)}} &
    \lim_{x \to c}     (f(x) - g(x)) &= \ln  \lim_{x \to c} {  e^{f(x)}     \over       e^{g(x)}    } \cs \\
    0^0                   \;\;\;\;   && \lim_{x \to c} f(x) &= 0^+    & \lim_{x \to c} g(x) &= 0      &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} {    g(x)       \over {1 \over \ln f(x)}} &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} {  \ln f(x)     \over {1 \over   g(x)  }} \cs \\
    1^\infty              \;\;\:\,   && \lim_{x \to c} f(x) &= 1      & \lim_{x \to c} g(x) &= \infty &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} {  \ln f(x)     \over {1 \over   g(x)  }} &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} {    g(x)       \over {1 \over \ln f(x)}} \cs \\
    \infty^0              \;\;\,\,   && \lim_{x \to c} f(x) &= \infty & \lim_{x \to c} g(x) &= 0      &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} {    g(x)       \over {1 \over \ln f(x)}} &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} {  \ln f(x)     \over {1 \over   g(x)  }} \cs \\
  \end{aligned}
\]

## L'Hôpital's Rule

\[
  \text{If }
  {\lim_{x \to a}f(x) \over \lim_{x \to a}g(x)} =
  {0 \over 0} \text{ or } {\pm\infty \over \pm\infty}
  \text{, then }
  \lim_{x \to a}{f(x) \over g(x)} = \lim_{x \to a}{f'(x) \over g'(x)}
\]

  - applies if limit is one sided ($x \to a^{\pm}$)
  - applies if limit is taken as x approaches infinity ($x \to \pm\infty$)
  - can be repeated
  - can be used for other indeterminate forms - but the expression must be transformed to $\frac{0}{0}$ or $\frac{\pm\infty}{\pm\infty}$ form first.

(watch [indeterminate products](http://patrickjmt.com/lhospitals-rule-indeterminate-products/), [indeterminate differences](http://patrickjmt.com/lhospitals-rule-indeterminate-differences/), [indeterminate powers](http://patrickjmt.com/lhospitals-rule-indeterminate-powers/))

## Example

\[
  \begin{aligned}
    \lim_{n\to\infty} {3^n \over 3^n - 1}
      &= \lim_{n\to\infty} {{3^n \over 3^n} \over {3^n - 1 \over 3^n}} \BG \\
      &= \lim_{n\to\infty} {1 \over 1 - {1 \over 3^n}}                 \BG \\
      &= \lim_{n\to\infty} {1 \over 1 - 0}                             \BG \\
      &= 1                                                             \BG \\
  \end{aligned}
\]

## Example

\[
  \begin{aligned}
      \lim_{n\to\infty} {(n+1)^a \cdot n! \over (n+1)! \cdot n^a}
      &= \lim_{n\to\infty} {(n+1)^a \cdot n! \over (n+1) \cdot n! \cdot n^a} \BG \\
      &= \lim_{n\to\infty} {(n+1)^a \over (n+1) n^a}                         \BG \\
      &= \lim_{n\to\infty} {n^a + \ldots \over n^{a+1} + n^a}                \BG \\
      &= 0                                                                   \BG \\
  \end{aligned}
\]
