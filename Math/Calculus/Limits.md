# Limits

## Useful Limits

\[
  \begin{aligned}
    \lim_{x \to 0}\frac{x}{\sin x} = &\lim_{x \to 0}\frac{\sin x}{x} = 1 \\[1em]
    \lim_{x \to 0}\frac{\cos x - 1}{x} = &\lim_{x \to 0}\frac{1 - \cos x}{x} = 0
          && \text{Both work, I checked} \\[1em]
    &\lim_{x \to 0}\frac{1 - \cos x}{x^2} = \frac{1}{2}
          && \text{Don't know about the other here...}\\[1em]
    &\lim_{x \to n^\pm}\tan (\pi x + \frac{\pi}{2}) = \mp\infty
          && \forall n | n \in \mathbb{N} \qquad\text{(according to Google)}\\[1em]
    &\lim_{x \to 0} x^ne^{-x} = 0
          && \forall n\\[1em]
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
