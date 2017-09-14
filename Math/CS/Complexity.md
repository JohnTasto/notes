# Complexity

## Common growth rates
\[
  1 ~~<~~ \lg^* n ~~<~~ \lg \lg n ~~<~~ \lg n ~~<~~ \lg^2 n ~~<~~ \sqrt{n} ~~<~~ n \\
  n ~~<~~ n \lg^* n ~~<~~ n \lg n \equiv \lg n! ~~<~~ n^2  ~~<~~ 2^n ~~<~~ 2^{n \lg n} \equiv n! ~~<~~ 2^{2^n}
\]

See [Summation Growth Rates](https://en.wikipedia.org/wiki/Summation#Growth_rates) for Θ of some common sums.

## Big $\O$
upper bound
small $\text{o}$ means $<$ instead of $\leq$

\[
  f(x) \text{ is } \O(g(x)) \iff \exists ~ c, x_0
  \left|
  \begin{array}{c}
    f(x) \leq c \cdot g(x), \\
    \text{for all } x > x_0
  \end{array}
  \right.
\]

\[
  \text{If}~~ \lim_{x \to \infty} {f(x) \over g(x)} \le c, ~~\text{then}~~ f(x) \text{ is } \O(g(x))
\]

## Big $Ω$
lower bound
small $\omega$ means $>$ instead of $\geq$

\[
  f(x) \text{ is } Ω(g(x)) \iff \exists ~ c, x_0
  \left|
  \begin{array}{c}
    f(x) \geq c \cdot g(x), \\
    \text{for all } x > x_0
  \end{array}
  \right.
\]

\[
  \text{If}~~ \lim_{x \to \infty} {f(x) \over g(x)} \ge c, ~~\text{then}~~ f(x) \text{ is } Ω(g(x))
  \qquad \text{not verified...}
\]

## Big $Θ$
both upper and lower bound

\[
  f(x) \text{ is } \Theta(g(x)) \iff
  f(x) \text{ is } \O(g(x)) \text{ and } f(x) \text{ is } Ω(g(x))
\]

See [Time Complexity](https://en.wikipedia.org/wiki/Time_complexity)

Example: Show $\lg n!$ is $\Theta(n \lg n)$.

\[
  \begin{aligned}
    \lg n! &\le c \cdot n \lg n \\
    \lg n! &\le c \cdot \lg n^n \\
    \lg ((n)(n-1)(n-2)\cdots(2)(1)) &\le c \cdot \lg ((n)_n(n)_{n-1}(n)_{n-2}\cdots(n)_2(n)_1) \\[1em]
    c &= 1 \\
    n_0 &= 1 \\[2em]
    \lg n! &\ge c \cdot n \lg n \\
    \lg n + \lg (n-1) + \lg (n-2) + \cdots + \lg 2 + \lg 1 & \\
    (\lg n + \lg 1) + (\lg (n-1) + \lg 2) + \cdots + (\lg \tfrac{n}{2} + \lg \tfrac{n}{2})
      &\gt \tfrac{1}{2}n\lg \tfrac{n}{2} \\
    (\lg n + \lg 1) + (\lg (n-1) + \lg 2) + \cdots + (\lg \tfrac{n}{2} + \lg \tfrac{n}{2})
      &\gt \tfrac{n}{2} \lg n - \tfrac{n}{2} \c{\lg 2} \\[1em]
    \tfrac{n}{2} \lg n - \tfrac{n}{2} &\ge \tfrac{n}{4} \lg n,\quad n \ge 4 \\[1em]
    c &= \tfrac{1}{4} \\
    n_0 &= 4 \\
  \end{aligned}
\]

Example: Compare $x^{\lg x}$ and $(\lg x)^x$.

\[
  \begin{gathered}
    \begin{aligned}
          \text{let}~~ x &= 2^y, &&\p{{}={}} x^{\lg x} & &\p{{}={}} (\lg x)^x         \h4 \\
      \text{and}~~ \lg x &= y.   &&     =    (2^y)^y   & &     =    (y)^{2^y}         \h4 \\
                         &       &&     =    2^{y^2}   & &     =    (2^{\lg y})^{2^y} \h4 \\
                         &       &&                    & &     =    2^{2^y \lg y }    \h4 \\
    \end{aligned} \\
    y^2 \lll 2^y \lg y \h4 \\
  \end{gathered}
\]
