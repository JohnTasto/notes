# Functions and rates of growth

## Big $\text{O}$
upper bound
small $\text{o}$ means $<$ instead of $\leq$

\[
  f(x) \text{ is O}(g(x)) \Longleftrightarrow \exists ~ c, x_0
  \left|
  \begin{array}{c}
    f(x) \leq c \cdot g(x), \\
    \text{for all } x > x_0
  \end{array}
  \right.
\]

## Big $\Omega$
lower bound
small $\omega$ means $>$ instead of $\geq$

\[
  f(x) \text{ is } \Omega(g(x)) \Longleftrightarrow \exists ~ c, x_0
  \left|
  \begin{array}{c}
    f(x) \geq c \cdot g(x), \\
    \text{for all } x > x_0
  \end{array}
  \right.
\]

## Big $\Theta$
both upper and lower bound

\[
  f(x) \text{ is } \Theta(g(x)) \Longleftrightarrow
  f(x) \text{ is O}(g(x)) \land f(x) \text{ is } \Omega(g(x))
\]

## Common growth rates
\[
  \log n < n < n \log n < n^2 < 2^n
\]

### Example: Show $\log n!$ is $\Theta(n \log n)$

Simple way:
\[
  \begin{matrix}
    \log n! \leq c \cdot n \log n \\
    \text{pick } c = 1 \\
    \log n! \leq \log n^n \leq n \log n \\
  \end{matrix}
\]

More complicated way:
\[
  \begin{matrix}
    \log n! \leq c \cdot n \log n \\
    \begin{aligned}
      & \log n! \\
      = & \log n + \log (n-1) + \log (n-2) + \ldots + \log 2 + \log 1
    \end{aligned}
  \end{matrix}
\]
