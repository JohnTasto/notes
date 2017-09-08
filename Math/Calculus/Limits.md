# Limits

## Rules

\[
  \begin{aligned}
    \lim_{x \to a} \big(f(x) \pm g(x) \big) &= \lim_{x \to a} f(x) \pm \lim_{x \to a} g(x) &&
    \text{Sum/Difference} \\[1em]
    \lim_{x \to a} \big( c \cdot f(x) \big) &= c \cdot \lim_{x \to a} f(x)      &&
    \text{Scalar Multiple} \\[1em]
             \lim_{x \to a} f(x) \cdot g(x) &= \lim_{x \to a} f(x) \cdot \lim_{x \to a} g(x) &&
    \text{Product} \\[1em]
           \lim_{x \to a} \frac{f(x)}{g(x)} &= \frac{\lim_{x \to a} f(x)}{\lim_{x \to a} g(x)} &&
    \text{Quotient}
  \end{aligned}
\]

## Useful Limits

\[
  \begin{aligned}
    \lim_{x \to 0}\frac{x}{\sin x} = &\lim_{x \to 0}\frac{\sin x}{x} = 1 \\[1em]
    \lim_{x \to 0}\frac{\cos x - 1}{x} = &\lim_{x \to 0}\frac{1 - \cos x}{x} = 0
          && \text{Both work, I checked} \\[1em]
    &\lim_{x \to 0}\frac{1 - \cos x}{x^2} = \frac{1}{2}
          && \text{Don't know about the other here...} \\[1em]
    &\lim_{x \to n^\pm}\tan \Big(π x + \frac{π}{2} \Big) = \mp\infty
          && \forall n | n \in \mathbb{N} \qquad\text{(according to Google)} \\[1em]
    &\lim_{x \to 0} x^ne^{-x} = 0
          && \forall n \\[1em]
  \end{aligned}
\]

## Indeterminate Forms

\[
  \begin{aligned}
    \text{Form} \;\, &&
    \text{Condit} & \text{ion} &
    \text{Condit} & \text{ion} &
    \text{Transfor} & \text{mation to}~ \tfrac{0}{0} &
    \text{Transfor} & \text{mation to}~ \tfrac{\infty}{\infty} & \\[2em]
    \frac{0}{0}           \;\;\;\:\, && \lim_{x \to c} f(x) &= 0      & \lim_{x \to c} g(x) &= 0       &
                                     &                                                                 &
    \lim_{x \to c} \frac{f(x)}{g(x)} &=      \lim_{x \to c} \frac{\frac{1}{g(x)}} {  \frac{1}{f(x)}  } \\[1.5em]
    \frac{\infty}{\infty} \;\;\;\,   && \lim_{x \to c} f(x) &= \infty & \lim_{x \to c} g(x) &= \infty  &
    \lim_{x \to c} \frac{f(x)}{g(x)} &=      \lim_{x \to c} \frac{\frac{1}{g(x)}} {  \frac{1}{f(x)}  } &
                                     &                                                                 \\[1.5em]
    0\cdot\infty          \;\,       && \lim_{x \to c} f(x) &= 0      & \lim_{x \to c} g(x) &= \infty  &
    \lim_{x \to c}       f(x)  g(x)  &=      \lim_{x \to c} \frac{     f(x)     } {  \frac{1}{g(x)}  } &
    \lim_{x \to c}       f(x)  g(x)  &=      \lim_{x \to c} \frac{     g(x)     } {  \frac{1}{f(x)}  } \\[1.5em]
    \infty - \infty                  && \lim_{x \to c} f(x) &= \infty & \lim_{x \to c} g(x) &= \infty  &
    \lim_{x \to c}     (f(x) - g(x)) &= \lim_{x \to c} \frac{\frac{1}{g(x)} - \frac{1}{f(x)}} {\frac{1}{f(x)g(x)}} &
    \lim_{x \to c}     (f(x) - g(x)) &= \ln  \lim_{x \to c} \frac{   e^{f(x)}   } {     e^{g(x)}     } \\[1.5em]
    0^0                   \;\;\;\;   && \lim_{x \to c} f(x) &= 0^+    & \lim_{x \to c} g(x) &= 0       &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} \frac{     g(x)     } {\frac{1}{\ln f(x)}} &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} \frac{   \ln f(x)   } {  \frac{1}{g(x)}  } \\[1.5em]
    1^\infty              \;\;\:\,   && \lim_{x \to c} f(x) &= 1      & \lim_{x \to c} g(x) &= \infty  &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} \frac{   \ln f(x)   } {  \frac{1}{g(x)}  } &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} \frac{     g(x)     } {\frac{1}{\ln f(x)}} \\[1.5em]
    \infty^0              \;\;\,\,   && \lim_{x \to c} f(x) &= \infty & \lim_{x \to c} g(x) &= 0       &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} \frac{     g(x)     } {\frac{1}{\ln f(x)}} &
    \lim_{x \to c}       f(x)^{g(x)} &= \exp \lim_{x \to c} \frac{   \ln f(x)   } {  \frac{1}{g(x)}  }
  \end{aligned}
\]

## L'Hôpital's Rule

\[
  \text{If }
  \frac{\lim_{x \to a}f(x)}{\lim_{x \to a}g(x)} =
  \frac{0}{0} \text{ or } \frac{\pm\infty}{\pm\infty}
  \text{, then }
  \lim_{x \to a}\frac{f(x)}{g(x)} = \lim_{x \to a}\frac{f'(x)}{g'(x)}
\]

  - applies if limit is one sided ($x \to a^{\pm}$)
  - applies if limit is taken as x approaches infinity ($x \to \pm\infty$)
  - can be repeated
  - can be used for other indeterminate forms - but the expression must be transformed to $\frac{0}{0}$ or $\frac{\pm\infty}{\pm\infty}$ form first.

(watch [indeterminate products](http://patrickjmt.com/lhospitals-rule-indeterminate-products/), [indeterminate differences](http://patrickjmt.com/lhospitals-rule-indeterminate-differences/), [indeterminate powers](http://patrickjmt.com/lhospitals-rule-indeterminate-powers/))

## Example

\[
  \begin{aligned}
    \lim_{n\to\infty} \frac{3^n}{3^n - 1}
      &= \lim_{n\to\infty} \frac{\frac{3^n}{3^n}}{\frac{3^n - 1}{3^n}} \\[1em]
      &= \lim_{n\to\infty} \frac{1}{1 - \frac{1}{3^n}}                 \\[1em]
      &= \lim_{n\to\infty} \frac{1}{1 - 0}                             \\[1em]
      &= 1
  \end{aligned}
\]

## Example

\[
  \begin{aligned}
      \lim_{n\to\infty} \frac{(n+1)^a \cdot n!}{(n+1)! \cdot n^a}
      &= \lim_{n\to\infty} \frac{(n+1)^a \cdot n!}{(n+1) \cdot n! \cdot n^a} \\[1em]
      &= \lim_{n\to\infty} \frac{(n+1)^a}{(n+1) n^a}                         \\[1em]
      &= \lim_{n\to\infty} \frac{n^a + \ldots}{n^{a+1} + n^a}                \\[1em]
      &= 0
  \end{aligned}
\]
