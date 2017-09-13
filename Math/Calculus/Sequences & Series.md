# Sequences & Series

## Definitions

**Sequence**: an ordered list of real numbers
**Series**: a sum of a sequence

See https://en.wikipedia.org/wiki/Summation for a list of summation identities.

## Arithmetic

\[
  \begin{gathered}
    \{a,~a+d,~a+2d,~a+3d,~\ldots\} \\
    \begin{aligned} \\
      x_n &= a + (n{-}1)d &                      &      \text{Explicit}  \\[1em]
    \end{aligned} \\
    \begin{aligned} \\
      d &= \text{common difference between terms} \\
      a &= \text{first term}                      \\
    \end{aligned} \\
  \end{gathered}
\]

\[
  \begin{aligned}
     s_n &= \sum_{k=1}^n a + (k{-}1)d          \BG \\
         &= \p{\tfrac12n(}
               \p{2} a\p{{}+   (n{-} 0   ) d} ~~~
          +~~~ \p{2} a     +\p{(n{-} 1   )}d  ~~~
          +~~~ \p{2} a     +\p{(n{-}}2\p{)}d  ~~~
          +~~~ \cdots ~~~
          +~~~ \p{2} a     +   (n{-} 1   ) d  \Bg \\
         &= \p{\tfrac12n(}
               \p{2} a     +   (n{-} 1   ) d  ~~~
          +~~~ \p{2} a     +   (n{-} 2   ) d  ~~~
          +~~~ \p{2} a     +   (n{-} 3   ) d  ~~~
          +~~~ \cdots ~~~
          +~~~ \p{2} a                        \Bg \\
    2s_n &= \p{\tfrac12n(}
                  2  a     +   (n{-} 1   ) d  ~~~
          +~~~    2  a     +   (n{-} 1   ) d  ~~~
          +~~~    2  a     +   (n{-} 1   ) d  ~~~
          +~~~ \cdots ~~~
          +~~~    2  a     +   (n{-} 1   ) d  \Bg \\
         &= \p{\tfrac12}
                        n(2a + (n{-} 1   ) d) \Bg \\
     s_n &= \tfrac12n(2a + (n{-} 1   ) d) \Bg \\
         &= \tfrac12n(x_1 + x_n)          \Bg \\
  \end{aligned}
\]

## Geometric

\[
  \begin{gathered}
    \{a,~ar,~ar^2,~ar^3,~\ldots\} \\
    \begin{aligned} \\
      x_n &= a r^{n-1} &                     &      \text{Explicit}  \\[1em]
      x_n &= x_{n-1} r & \atop\smash{\Big\}} & \atop\text{Recursive} \\[-5em]
      x_1 &= a                                                       \\
    \end{aligned} \\
    \begin{aligned} \\
      r &= \text{common ratio between terms} \\
      a &= \text{first term & scale factor} \\
    \end{aligned} \\
  \end{gathered}
\]

\[
  \begin{aligned} \\
           s_n &= \sum_{k=1}^n ar^{k-1} = \sum_{k=0}^{n-1} ar^k              \BG \\
           s_n &=    a +     ar + ar^2 + \cdots + ar^{n-1}                   \Bg \\
          rs_n &= \p{a + {}} ar + ar^2 + \cdots + ar^{n-1} + ar^n            \Bg \\
    s_n - rs_n &= a - ar^n                                                   \Bg \\
    s_n(1 - r) &= a(1-r^n)                                                   \Bg \\
           s_n &= {a(1 - r^n) \over 1 - r}                                   \BG \\
               &= {a(r^n - 1) \over r - 1}                                   \BG \\
               &= {ar^n - a \over r - 1}                                     \BG \\
               &= {x_{n+1} - a \over r - 1}                                  \BG \\[2em]
             s &= \sum_{k=0}^\infty ar^k                                     \BG \\
               &= \lim_{n \to \infty} \sum_{k=0}^n ar^k                      \BG \\
               &= \lim_{n \to \infty} {a(1 - r^{n+1}) \over 1 - r}           \BG \\
               &= {a \over 1-r} - \lim_{n \to \infty} {ar^{n+1} \over 1 - r} \BG \\
               &= {a \over 1-r}                                              \BG \\[2em]
             s &=    a +     ar + ar^2 + \cdots                              \Bg \\
            rs &= \p{a + {}} ar + ar^2 + \cdots                              \Bg \\
        s - rs &= a                                                          \Bg \\
             s &= {a \over 1-r}, ~|r| < 1                                    \Bg \\
  \end{aligned}
\]

## $p$-series

\[
  \begin{gathered}
    \{1,~\tfrac{1}{2^p},~\tfrac{1}{3^p},~\tfrac{1}{4^p},~\ldots\} \\
    \begin{aligned} \\
      x_n &= \frac{1}{n^p} && \text{Explicit} \\
    \end{aligned} \\
    \begin{aligned} \\
      p > 0 \\
    \end{aligned} \\
  \end{gathered}
\]

When $p = 1$, this is the harmonic series, which diverges.
When $p > 1$, the $p$-series converges.

## Telescoping Series

Any series where all of the middle terms cancel out.

Example (converging), rewritten using partial fraction expansion:

\[
  \begin{aligned}
    \sum_{n=2}^\infty {-2 \over (n+1)(n+2)}
 &= {-2 \over 3\cdot4} + {-2 \over 4\cdot5} + {-2 \over 5\cdot6} + \cdots \\
 &\equiv \\
    \lim_{N\to\infty} \sum_{n=2}^N {-2 \over (n+1)(n+2)}
 &= \lim_{N\to\infty} \sum_{n=2}^N {-2 \over (n+1)} + {2 \over (n+2)} \\
 &= \lim_{N\to\infty}
    \bigg(-\frac23+\frac24\bigg) +
    \bigg(-\frac24+\frac25\bigg) +
    \bigg(-\frac25+\frac26\bigg) +
    \cdots +
    \bigg(-{2 \over N+1}+{2 \over N+2}\bigg) \\
  &= \lim_{N\to\infty}-\frac23 + {2 \over N+2} \\
  &= -\frac23
  \end{aligned}
\]

Example (diverging):

\[
  \begin{aligned}
    \sum_{n=1}^\infty (-1)^{n-1}
 &= 1 - 1 + 1 - 1 + 1 \cdots     \BG \\
    \sum_{n=1}^N (-1)^{n-1}
 &= \begin{cases}
      \text{$1$ if $N$ odd} \\
      \text{$0$ if $N$ even}
    \end{cases}                  \BG \\
    \lim_{N\to\infty} \sum_{n=1}^N (-1)^{n-1}
 &= \lim_{N\to\infty}
    \begin{cases}
      \text{$1$ if $N$ odd} \\
      \text{$0$ if $N$ even}
    \end{cases}                  \BG \\
 &= \text{DNE}                   \BG \\
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
  \text{If}~~ \lim_{n\to\infty} a_n \ne 0, ~~
  \text{then}~~ \sum_{n=1}^\infty a_n ~~\text{diverges.}
\]

### Integral Test

If $f$ is a positive, continuous, monotone decreasing function over $[k, \infty)$, then the series $\sum_{n=k}^\infty f(n)$ is bounded by:

\[
  \int_k^\infty f(x) ~dx ~~~~~\le~~~~~ \sum_{n=k}^\infty f(n) ~~~~~\le~~~~~ f(k) + \int_k^\infty f(x) ~dx
\]

### Convergence Comparison Test

\[
  \text{If}~~~ a_n \ge b_n ~~\forall n \in \mathbb{S} ~~~
  \text{and}~~~ \sum_{n=k}^\infty a_n ~~~\text{converges, then}~~~ \sum_{n=k}^\infty b_n ~~~\text{also converges.}
\]

### Divergence Comparison Test

\[
  \text{If}~~~ a_n \le b_n ~~\forall n \in \mathbb{S} ~~~
  \text{and}~~~ \sum_{n=k}^\infty a_n ~~~\text{diverges, then}~~~ \sum_{n=k}^\infty b_n ~~~\text{also diverges.}
\]

### Limit Comparison Test

\[
  \begin{gathered}
    \text{If}~~~ a_n \ge 0, b_n \gt 0 ~~\forall n \in \mathbb{S} ~~~
    \text{and}~~~ 0 ~\lt~ \lim_{n \to \infty} {a_n \over b_n} ~\lt~ \infty, \Bg \\
    \text{then}~~~ \sum_{n=k}^\infty a_n ~~~\text{and}~~~ \sum_{n=k}^\infty b_n ~~~
    \text{either both converge or both diverge.} \Bg \\
  \end{gathered}
\]

### Ratio Test

\[
  \text{Given}~~ \lim_{n\to\infty} \bigg|{a_{n+1} \over a_n} \bigg| = L, ~~
  \sum_{n=k}^\infty a_n
  \begin{cases}
    \text{converges}     & L < 1 \\
    \text{diverges}      & L > 1 \\
    \text{indeterminate} & L = 1 \\
  \end{cases}
\]

### Root Test

\[
  \text{Given}~~ \lim_{n\to\infty} \sqrt[n]{|a_n|} = L, ~~
  \sum_{n=k}^\infty a_n
  \begin{cases}
    \text{converges}     & L < 1 \\
    \text{diverges}      & L > 1 \\
    \text{indeterminate} & L = 1 \\
  \end{cases}
\]

### Alternating Series Test

Cannot confirm divergence!

\[
  \begin{gathered}
    \text{Given}~~~ a_n = (-1)^nb_n ~~~\text{or}~~~ a_n = (-1)^{n+1}b_n ~~~
    \text{where}~~~ b_n \ge 0 ~\forall n \in \mathbb{S}, \Bg \\
    \text{if}~~ \lim_{n\to\infty} b_n = 0 ~~~\text{and}~~~ b_n \ge b_{n+1} ~\forall n \in \mathbb{S}, ~~~
    \text{then}~~~ \sum_{n=k}^\infty a_n ~~~ \text{converges.} \Bg \\
  \end{gathered}
\]

### Absolute Convergence Test

\[
  \begin{gathered}
    \text{If}~~~ \sum |a_n| ~~~\text{converges, then}~~~ \sum a_n ~~~\text{converges absolutely.} \Bg \\
    \text{If}~~~ \sum |a_n| ~~~\text{diverges and}~~~ \sum a_n ~~~\text{converges}, ~
    \text{then}~~~ \sum a_n ~~~\text{converges conditionally.} \Bg \\
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
    \text{where}~~~ b_n \ge 0 ~\forall n \in \mathbb{S}, \Bg \\
    \text{if}~~ \lim_{n\to\infty} b_n = 0 ~~~\text{and}~~~ b_n \ge b_{n+1} ~\forall n \in \mathbb{S}, ~~~
    \text{then}~~ \Bg \\
    \sum_{n=1}^k a_n - |a_{k+1}|
    ~~~~~\le~~~~~ \sum_{n=1}^\infty a_n ~~~~~\le~~~~~
    \sum_{n=1}^k a_n + |a_{k+1}| \BG \\
  \end{gathered}
\]

## Integrating & Differentiating

The sum/difference rule applies:

\[
  \begin{aligned}
    \drv{}x \sum_{n=0}^\infty f(x) &= \drv{}x f(0) + \drv{}x f(1) + \cdots \BG \\
                              &= \sum_{n=0}^\infty   \drv{}x f(x)          \BG \\[1em]
    \int    \sum_{n=0}^\infty f(x) &= \int    f(0) + \int    f(1) + \cdots \BG \\
                              &= \sum_{n=0}^\infty   \int    f(x)          \BG \\
  \end{aligned}
\]

## Sum of $n$ Squares

https://www.khanacademy.org/math/calculus-home/series-calc/series-basics-challenge/v/sum-of-n-squares-1
https://www.khanacademy.org/math/calculus-home/series-calc/series-basics-challenge/v/sum-n-squares-2
https://www.khanacademy.org/math/calculus-home/series-calc/series-basics-challenge/v/alternate-sum-of-n-squares-formula

\[
  \sum_{i=0}^n i^2 = \tfrac13n^3 + \tfrac12n^2 + \tfrac16n = {n(n+1)(2n+1) \over 6}
\]

## Misc Formulas

If we know a formula for $s_n$ and we want to find the formula for $x_n$:

\[
  x_n = s_n - s_{n-1}
\]
