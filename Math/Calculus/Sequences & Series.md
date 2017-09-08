# Sequences & Series

## Definitions

**Sequence**: an ordered list of real numbers
**Series**: a sum of a sequence


## Arithmetic

\[
  \begin{gathered}
    \{a,~a+d,~a+2d,~a+3d,~...\} \\[1.5em]
    \begin{aligned}
      x_n &= a + (n\!-\!1)d &             &      \text{Explicit}  \\[.5em]
      x_n &= x_{n-1} + d    & \atop\Big\} & \atop\text{Recursive} \\[-1.25em]
      x_1 &= a                                                    \\
    \end{aligned} \\
    \begin{aligned}
      d &= \text{common difference between terms} \\
      a &= \text{first term}
    \end{aligned}
  \end{gathered}
\]

\[
  \begin{aligned}
     s_n &= \sum_{k=1}^n a + (k\!-\!1)d       \\[1.25em]
         &= \phantom{\tfrac{1}{2}n(}
               \phantom{2} a   \phantom{+(n\!-\!1)d} ~~~
          +~~~ \phantom{2} a + \phantom{(n\!-\!2)} d ~~~
          +~~~ \phantom{2} a + \phantom{(n\!-\!} 2 \phantom{)} d ~~~
          +~~~ \ldots ~~~
          +~~~ \phantom{2} a + (n\!-\!1)d      \\
         &= \phantom{\tfrac{1}{2}n(}
               \phantom{2} a + (n\!-\!1)d ~~~
          +~~~ \phantom{2} a + (n\!-\!2)d ~~~
          +~~~ \phantom{2} a + (n\!-\!3)d ~~~
          +~~~ \ldots ~~~
          +~~~ \phantom{2} a                   \\
    2s_n &= \phantom{\tfrac{1}{2}n(}
               2a + (n\!-\!1)d ~~~
          +~~~ 2a + (n\!-\!1)d ~~~
          +~~~ 2a + (n\!-\!1)d ~~~
          +~~~ \ldots ~~~
          +~~~ 2a + (n\!-\!1)d                 \\
         &= \phantom{\tfrac{1}{2}}
                        n(2a + (n\!-\!1)d)    \\[.25em]
     s_n &= \tfrac{1}{2}n(2a + (n\!-\!1)d)    \\[.25em]
         &= \tfrac{1}{2}n(x_1 + x_n)
  \end{aligned}
\]

## Geometric

\[
  \begin{gathered}
    \{a,~ar,~ar^2,~ar^3,~...\} \\[1.5em]
    \begin{aligned}
      x_n &= a r^{n-1} &             &      \text{Explicit}  \\[.5em]
      x_n &= x_{n-1} r & \atop\Big\} & \atop\text{Recursive} \\[-1.25em]
      x_1 &= a                                               \\
    \end{aligned} \\
    \begin{aligned}
      r &= \text{common ratio between terms} \\
      a &= \text{first term \& scale factor}
    \end{aligned}
  \end{gathered}
\]

\[
  \begin{aligned}
           s_n &= \sum_{k=1}^n ar^{k-1} = \sum_{k=0}^{n-1} ar^k              \\[1.25em]
           s_n &=         a +  ar + ar^2 + \ldots + ar^{n-1}                 \\
          rs_n &=\phantom{a +} ar + ar^2 + \ldots + ar^{n-1} + ar^n          \\
    s_n - rs_n &= a - ar^n                                                   \\
    s_n(1 - r) &= a(1-r^n)                                                   \\[.25em]
           s_n &= \frac{a(1 - r^n)}{1 - r}                                   \\[.75em]
               &= \frac{a(r^n - 1)}{r - 1}                                   \\[.75em]
               &= \frac{ar^n - a}{r - 1}                                     \\[.75em]
               &= \frac{x_{n+1} - a}{r - 1}                                  \\[2em]
             s &= \sum_{k=0}^\infty ar^k                                     \\[1.25em]
               &= \lim_{n \to \infty} \sum_{k=0}^n ar^k                      \\[1.25em]
               &= \lim_{n \to \infty} \frac{a(1 - r^{n+1})}{1 - r}           \\[1em]
               &= \frac{a}{1-r} - \lim_{n \to \infty} \frac{ar^{n+1}}{1 - r} \\[1em]
               &= \frac{a}{1-r}                                              \\[2em]
             s &=         a +  ar + ar^2 + \ldots                            \\
            rs &=\phantom{a +} ar + ar^2 + \ldots                            \\
        s - rs &= a                                                          \\
             s &= \frac{a}{1-r}, ~|r| < 1
  \end{aligned}
\]

## $p$-series

\[
  \begin{gathered}
    \{1,~\tfrac{1}{2^p},~\tfrac{1}{3^p},~\tfrac{1}{4^p},~...\} \\[1.5em]
    \begin{aligned}
      x_n &= \frac{1}{n^p} && \text{Explicit} \\
    \end{aligned} \\
    \begin{aligned}
      p > 0
    \end{aligned}
  \end{gathered}
\]

When $p = 1$, this is the harmonic series, which diverges.
When $p > 1$, the $p$-series converges.

## Telescoping Series

Any series where all of the middle terms cancel out.

Example (converging), rewritten using partial fraction expansion:

\[
  \begin{aligned}
    \sum_{n=2}^\infty \frac{-2}{(n+1)(n+2)}
 &= \frac{-2}{3\cdot4} + \frac{-2}{4\cdot5} + \frac{-2}{5\cdot6} + \ldots \\
 &\equiv \\
    \lim_{N\to\infty} \sum_{n=2}^N \frac{-2}{(n+1)(n+2)}
 &= \lim_{N\to\infty} \sum_{n=2}^N \frac{-2}{(n+1)} + \frac{2}{(n+2)} \\
 &= \lim_{N\to\infty}\bigg(-\frac{2}{3}+\frac{2}{4}\bigg) +
    \bigg(-\frac{2}{4}+\frac{2}{5}\bigg) +
    \bigg(-\frac{2}{5}+\frac{2}{6}\bigg) +
    \ldots +
    \bigg(-\frac{2}{N+1}+\frac{2}{N+2}\bigg) \\
  &= \lim_{N\to\infty}-\frac{2}{3} + \frac{2}{N+2} \\
  &= -\frac{2}{3}
  \end{aligned}
\]

Example (diverging):

\[
  \begin{aligned}
    \sum_{n=1}^\infty (-1)^{n-1}
 &= 1 - 1 + 1 - 1 + 1 \ldots     \\[1.5em]
    \sum_{n=1}^N (-1)^{n-1}
 &= \begin{cases}
      \text{$1$ if $N$ odd} \\
      \text{$0$ if $N$ even}
    \end{cases}                  \\[1.5em]
    \lim_{N\to\infty} \sum_{n=1}^N (-1)^{n-1}
 &= \lim_{N\to\infty}
    \begin{cases}
      \text{$1$ if $N$ odd} \\
      \text{$0$ if $N$ even}
    \end{cases}                  \\[1.5em]
 &= \text{DNE}
  \end{aligned}
\]

## Power Series

\[
  \sum_{n=0}^\infty a_n(x-c)^n
\]


## Tests for Convergence

\[
  \mathbb{S} = \{n \in \mathbb{N} ~|~ n \ge k\}
\]

### Divergence Test

Cannot confirm convergence!

\[
  \text{If } \lim_{n\to\infty} a_n \ne 0 \text{, then } \sum_{n=1}^\infty a_n \text{ will diverge.}
\]

### Integral Test

If $f$ is a positive, continuous, monotone decreasing function over $[k, \infty)$, then the series $\sum_{n=k}^\infty f(n)$ is bounded by:

\[
  \int_k^\infty f(x) ~dx ~~~~~\le~~~~~ \sum_{n=k}^\infty f(n) ~~~~~\le~~~~~ f(k) + \int_k^\infty f(x) ~dx
\]

### Convergence Comparison Test

\[
  \text{If}~~~ a_n \ge b_n ~~\forall n \in \mathbb{S} ~~~
  \text{and}~~ \sum_{n=k}^\infty a_n ~~~\text{converges, ~then}~~ \sum_{n=k}^\infty b_n ~~~\text{also converges.}
\]

### Divergence Comparison Test

\[
  \text{If}~~~ a_n \le b_n ~~\forall n \in \mathbb{S} ~~~
  \text{and}~~ \sum_{n=k}^\infty a_n ~~~\text{diverges, ~then}~~ \sum_{n=k}^\infty b_n ~~~\text{also diverges.}
\]

### Limit Comparison Test

\[
  \begin{gathered}
    \text{If}~~~ a_n \ge 0, b_n \gt 0 ~~\forall n \in \mathbb{S} ~~~
    \text{and}~~~ 0 ~\lt~ \lim_{n \to \infty}\frac{a_n}{b_n} ~\lt~ \infty, \\
    \text{then}~~ \sum_{n=k}^\infty a_n ~~~\text{and}~~ \sum_{n=k}^\infty b_n ~~~
    \text{either both converge or both diverge.}
  \end{gathered}
\]

### Ratio Test

\[
  \text{Given}~~ \lim_{n\to\infty} \bigg|\frac{a_{n+1}}{a_n} \bigg| = L, ~~
  \sum_{n=k}^\infty a_n
  \begin{cases}
    \text{converges}     & L < 1 \\
    \text{diverges}      & L > 1 \\
    \text{indeterminate} & L = 1
  \end{cases}
\]

### Root Test

\[
  \text{Given}~~ \lim_{n\to\infty} \sqrt[n]{|a_n|} = L, ~~
  \sum_{n=k}^\infty a_n
  \begin{cases}
    \text{converges}     & L < 1 \\
    \text{diverges}      & L > 1 \\
    \text{indeterminate} & L = 1
  \end{cases}
\]

### Alternating Series Test

Cannot confirm divergence!

\[
  \begin{gathered}
    \text{Given}~~~ a_n = (-1)^nb_n ~~~\text{or}~~~ a_n = (-1)^{n+1}b_n ~~~
    \text{where}~~~ b_n \ge 0 ~\forall n \in \mathbb{S}, \\
    \text{if}~~ \lim_{n\to\infty} b_n = 0 ~~~\text{and}~~~ b_n \ge b_{n+1} ~\forall n \in \mathbb{S}, ~~~
    \text{then}~~ \sum_{n=k}^\infty a_n ~~~ \text{converges.}
  \end{gathered}
\]

### Absolute Convergence Test

\[
  \begin{gathered}
    \text{If}~~ \sum |a_n| ~~~\text{converges, ~then}~~ \sum a_n ~~~\text{converges absolutely.} \\
    \text{If}~~ \sum |a_n| ~~~\text{diverges and}~~ \sum a_n ~~~\text{converges}, ~
    \text{then}~~ \sum a_n ~~~\text{converges conditionally.}
  \end{gathered}
\]

## Estimating Sums

\[
  s = s_k + r_k
\]

### Integral Estimate

If $f$ is a positive, continuous, monotone decreasing function over $[k, \infty)$, then the series $\sum_{n=k}^\infty f(n)$ is bounded by:

\[
  \sum_{n=1}^k f(n) + \int_{k+1}^\infty f(x) ~dx
  ~~~~~\le~~~~~ \sum_{n=1}^\infty f(n) ~~~~~\le~~~~~
  \sum_{n=1}^k f(n) + \int_{k  }^\infty f(x) ~dx
\]

### Alternating Series Estimate

\[
  \begin{gathered}
    \text{Given}~~~ a_n = (-1)^nb_n ~~~\text{or}~~~ a_n = (-1)^{n+1}b_n ~~~
    \text{where}~~~ b_n \ge 0 ~\forall n \in \mathbb{S}, \\
    \text{if}~~ \lim_{n\to\infty} b_n = 0 ~~~\text{and}~~~ b_n \ge b_{n+1} ~\forall n \in \mathbb{S}, ~~~
    \text{then}~~ \\
    \sum_{n=1}^k a_n - |a_{k+1}|
    ~~~~~\le~~~~~ \sum_{n=1}^\infty a_n ~~~~~\le~~~~~
    \sum_{n=1}^k a_n + |a_{k+1}|
  \end{gathered}
\]

## Integrating & Differentiating

The sum/difference rule applies:

\[
  \begin{aligned}
    \frac{d}{dx} \sum_{n=0}^\infty f(x) &= \frac{d}{dx} f(0) + \frac{d}{dx} f(1) + ... \\[1em]
                                        &= \sum_{n=0}^\infty   \frac{d}{dx} f(x)       \\[3em]
    \int         \sum_{n=0}^\infty f(x) &= \int         f(0) + \int         f(1) + ... \\[1em]
                                        &= \sum_{n=0}^\infty   \int         f(x)
  \end{aligned}
\]

## Misc Formulas

If we know a formula for $s_n$ and we want to find the formula for $x_n$:

\[
  x_n = s_n - s_{n-1}
\]
