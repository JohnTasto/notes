# Sequences & Series

## Definitions

  - **Sequence**: an ordered list of real numbers
  - **Series**: a sum of a sequence
  - **Interval of Convergence**: domain of x where a power series converges
    - when integrating or differentiating a series, the interval of convergence does not change, *except at the endpoints*.
  - **Radius of Convergence**: half of the interval of convergence

## Fibonacci Sequence

\[
  \begin{gathered}
    \{1,~1,~2,~3,~5,~8,~13,~21,~34,~55,~89,~144,~\ldots\} \\
    \begin{aligned} \\
      F_n &= F_{n-1} + F_{n-2} \\
      F_1 &= 1                 \\
      F_2 &= 1                 &
      \gbrace{1.8em}{\}~} & \gtext{1.8em}{Recurrence relation} \\[1em]
      F_n &= \frac{\varphi^n-\psi^n}{\varphi-\psi} \\[.5em]
          &= \frac{\varphi^n-\psi^n}{\sqrt 5}      &
      \gbrace[1em]{2.8em}{\}~} & \gtext[1em]{2.8em}{Closed form} \\[1em]
    \end{aligned} \\
    \begin{aligned} \\
      \varphi &= \frac{1 + \sqrt{5}}{2} \\
         \psi &= \frac{1 - \sqrt{5}}{2} ~~=~~ 1 - \varphi ~~=~~ - {1 \over \varphi} \\
    \end{aligned} \\
  \end{gathered}
\]

Interesting relationships:

\[
  F_{n}\times F_{n-3} - F_{n-1}\times F_{n-2} = (-1)^n
\]

## Summation identities

See https://en.wikipedia.org/wiki/Summation for a lot more summation identities.

\[
  \begin{aligned}
    \sum_{n=s}^t c\cdot f(n) &= c\cdot \sum_{n=s}^t f(n)                                     \h8 \\
    \sum_{n=s}^t f(n) \pm \sum_{n=s}^{t} g(n) &= \sum_{n=s}^t \left[f(n) \pm g(n)\right]     \h8 \\
    \sum_{i=s}^m a_i\ \cdot \sum_{j=t}^n c_j &= \sum_{i=s}^m\sum_{j=t}^n {a_i}{c_j}          \h8 \\[2em]
    \sum_{n=s}^t f(n) &= \sum_{n=s+p}^{t+p} f(n-p)                                           \h8 \\
    \sum_{n=0}^t f(2n) + \sum_{n=0}^t f(2n+1) &= \sum_{n=0}^{2t+1} f(n)                      \h8 \\[2em]
    \sum_{i=m}^n 1 &= n+1-m                                                                  \h8 \\
    \sum_{i=m}^n j &= (n+1-m)j                                                               \h8 \\
    \sum_{i=m}^n i &= \frac{n(n+1)}{2} - \frac{m(m-1)}{2} = \frac{(n+1-m)(n+m)}{2}
                                                                 && \text{Arithmetic series} \h8 \\
    \sum_{i=0}^n i = \sum_{i=1}^n i &= \frac{n(n+1)}{2}          && \text{Triangle numbers}  \h8 \\
    \sum_{i=0}^n i^2 &= \frac{n(n+1)(2n+1)}{6} = \frac{n^3}{3} + \frac{n^2}{2} + \frac{n}{6} \h8 \\[2em]
    \sum_{i=0}^{n-1} a^i &= \frac{1-a^n}{1-a}, \quad m < n       && \text{Geometric series}  \h8 \\[2em]
    \sum_{i=0}^n {n \choose i} &= 2^n                                                        \h8 \\
    \sum_{i=1}^{n} i{n \choose i} &= n2^{n-1}                                                \h8 \\
    \sum_{i=0}^n {n \choose i}a^{n-i} b^i &= (a + b)^n           && \text{Binomial theorem}  \h8 \\
  \end{aligned}
\]

## Arithmetic Series

\[
  \begin{gathered}
    \{a,~a+d,~a+2d,~a+3d,~\ldots\} \\
    \begin{aligned} \\
      x_n &= a + (n{-}1)d && \text{Closed form} \\[1em]
      x_n &= x_{n-1} + d  \\
      x_1 &= a            &
      \gbrace{1.1em}{\}~} & \gtext{1.1em}{Recurrence relation} \\[1em]
    \end{aligned} \\
    \begin{aligned} \\
      d &= \text{common difference between terms} \\
      a &= \text{first term}                      \\
    \end{aligned} \\
  \end{gathered}
\]

\[
  \begin{aligned}
     s_n &= \sum_{k=1}^n a + (k{-}1)d          \h7 \\
         &= \p{\tfrac12n(}
               \p{2} a\p{{}+   (n{-} 0   ) d} ~~~
          +~~~ \p{2} a     +\p{(n{-} 1   )}d  ~~~
          +~~~ \p{2} a     +\p{(n{-}}2\p{)}d  ~~~
          +~~~ \cdots ~~~
          +~~~ \p{2} a     +   (n{-} 1   ) d  \h4 \\
         &= \p{\tfrac12n(}
               \p{2} a     +   (n{-} 1   ) d  ~~~
          +~~~ \p{2} a     +   (n{-} 2   ) d  ~~~
          +~~~ \p{2} a     +   (n{-} 3   ) d  ~~~
          +~~~ \cdots ~~~
          +~~~ \p{2} a                        \h4 \\
    2s_n &= \p{\tfrac12n(}
                  2  a     +   (n{-} 1   ) d  ~~~
          +~~~    2  a     +   (n{-} 1   ) d  ~~~
          +~~~    2  a     +   (n{-} 1   ) d  ~~~
          +~~~ \cdots ~~~
          +~~~    2  a     +   (n{-} 1   ) d  \h4 \\
         &= \p{\tfrac12}
                        n(2a + (n{-} 1   ) d) \h4 \\
     s_n &= \tfrac12n(2a + (n{-} 1   ) d) \h4 \\
         &= \tfrac12n(x_1 + x_n)          \h4 \\
  \end{aligned}
\]

## Geometric Series

\[
  \begin{gathered}
    \{a,~ar,~ar^2,~ar^3,~\ldots\} \\
    \begin{aligned} \\
      x_n &= a r^{n-1} && \text{Closed form} \\[1em]
      x_n &= x_{n-1} r \\
      x_1 &= a         &
      \gbrace{1.1em}{\}~} & \gtext{1.1em}{Recurrence relation} \\[1em]
    \end{aligned} \\
    \begin{aligned} \\
      r &= \text{common ratio between terms} \\
      a &= \text{first term & scale factor}  \\
    \end{aligned} \\
  \end{gathered}
\]

\[
  \begin{aligned} \\
           s_n &= \sum_{k=1}^n ar^{k-1} = \sum_{k=0}^{n-1} ar^k              \h7 \\
           s_n &=    a +     ar + ar^2 + \cdots + ar^{n-1}                   \h4 \\
          rs_n &= \p{a + {}} ar + ar^2 + \cdots + ar^{n-1} + ar^n            \h4 \\
    s_n - rs_n &= a - ar^n                                                   \h4 \\
    s_n(1 - r) &= a(1-r^n)                                                   \h4 \\
           s_n &= {a(1 - r^n) \over 1 - r}                                   \h7 \\
               &= {a(r^n - 1) \over r - 1}                                   \h7 \\
               &= {ar^n - a \over r - 1}                                     \h7 \\
               &= {x_{n+1} - a \over r - 1}                                  \h7 \\[2em]
             s &= \sum_{k=0}^\infty ar^k                                     \h7 \\
               &= \lim_{n \to \infty} \sum_{k=0}^n ar^k                      \h7 \\
               &= \lim_{n \to \infty} {a(1 - r^{n+1}) \over 1 - r}           \h7 \\
               &= {a \over 1-r} - \lim_{n \to \infty} {ar^{n+1} \over 1 - r} \h7 \\
               &= {a \over 1-r}                                              \h7 \\[2em]
             s &=    a +     ar + ar^2 + \cdots                              \h4 \\
            rs &= \p{a + {}} ar + ar^2 + \cdots                              \h4 \\
        s - rs &= a                                                          \h4 \\
             s &= {a \over 1-r}, ~|r| < 1                                    \h4 \\
  \end{aligned}
\]

## $p$-series

\[
  \begin{gathered}
    \{1,~\tfrac{1}{2^p},~\tfrac{1}{3^p},~\tfrac{1}{4^p},~\ldots\} \\
    \begin{aligned} \\
      x_n &= \frac{1}{n^p} && \text{Closed form} \\
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
 &= 1 - 1 + 1 - 1 + 1 \cdots     \h7 \\
    \sum_{n=1}^N (-1)^{n-1}
 &= \begin{cases}
      \text{$1$ if $N$ odd} \\
      \text{$0$ if $N$ even}
    \end{cases}                  \h7 \\
    \lim_{N\to\infty} \sum_{n=1}^N (-1)^{n-1}
 &= \lim_{N\to\infty}
    \begin{cases}
      \text{$1$ if $N$ odd} \\
      \text{$0$ if $N$ even}
    \end{cases}                  \h7 \\
 &= \text{DNE}                   \h7 \\
  \end{aligned}
\]

## Power Series

\[
  \sum_{n=0}^\infty a_n(x-c)^n
\]

### Taylor & Maclaurin Series

A Maclaurin series is a Taylor series where $c = 0$.

\[
  \begin{aligned}
    P^n(c) &= f^n(c), ~\forall n \in \mathbb{N}         \h7 \\
    P(x) &= f(c) + f'(c)(x-c) + f''(c){1\over2}(x-c)^2 + f'''(c){1\over2\cdot3}(x-c)^3 +
            f^4(c){1\over2\cdot3\cdot4}(x-c)^4 + \cdots \h7 \\
         &= \sum_{n=0}^\infty f^n(c){(x-c)^n \over n!}  \h7 \\
  \end{aligned}
\]

#### Remainder / Error

\[
  \begin{aligned}
     P_{n,c}(x) &= f(c) + f'(c){(x-c) \over 1!} + f''(c){(x-c)^2 \over 2!} + f'''(c){(x-c)^3 \over 3!} + \cdots +
               f^n(c){(x-c)^n \over n!} \h7 \\
     E_{n,c}(x) &= f(x) - P_{n,c}(x)    \h7 \\
  \end{aligned}
\]

##### Taylor's Remainder Theorem / Lagrange Error Bound

\[
  \begin{gathered}
    \text{If}~~ |f^{n+1}(x)| \le M ~~\text{for an open interval containing $c$ and $x$,} \h4 \\
    \text{then}~~ |E_{n,c}(x)| \le {M(x - c)^{n+1} \over (n+1)!} \h7 \\
  \end{gathered}
\]

#### Common Maclaurin Series

\[
  \begin{aligned}
                e^{x} &= \sum^\infty_{n=0} {x^n \over n!}
                     &&= 1 + x + {x^2 \over 2!} + {x^3 \over 3!} + \cdots   \h7 \\
             \ln(1-x) &= \sum^\infty_{n=1} -{x^n \over n}
                     &&= -x - {x^2 \over 2} - {x^3 \over 3} - \cdots
                      && |x| < 1                                            \h7 \\
             \ln(1+x) &= \sum^\infty_{n=1} (-1)^{n+1}{x^n \over n}
                     &&= x - {x^2 \over 2} + {x^3 \over 3} - \cdots
                      && |x| < 1                                            \h7 \\[2em]
        {1 \over 1-x} &= \sum^\infty_{n=0} x^n
                      && \text{Geometric series}
                      && |x| < 1                                            \h7 \\
    {1 \over (1-x)^2} &= \sum^\infty_{n=1} nx^{n-1}
                    &&&& |x| < 1                                            \h7 \\
    {1 \over (1-x)^3} &= \sum^\infty_{n=2} {(n-1)n \over 2} x^{n-2}
                    &&&& |x| < 1                                            \h7 \\[2em]
              (1+x)^α &= \sum_{n=0}^\infty \binom{α}{n} x^n
                    &&&& |x| < 1, α \in \mathbb{C}                          \h7 \\[2em]
               \sin x &= \sum^\infty_{n=0} {(-1)^n \over (2n+1)!} x^{2n+1}
                     &&= x - {x^3 \over 6} + {x^5 \over 120} - \cdots       \h7 \\
               \cos x &= \sum^\infty_{n=0} {(-1)^n \over (2n)!} x^{2n}
                     &&= 1 - {x^2 \over 2} + {x^4 \over 24} - \cdots        \h7 \\
               \tan x &= \sum^\infty_{n=1} {B_{2n} (-4)^n \left(1-4^n\right) \over (2n)!} x^{2n-1}
                     &&= x + {x^3 \over 3} + {2 x^5 \over 15} + \cdots
                      && |x| < {π \over 2}, ~B_k = \text{Bernoulli numbers} \h7 \\
               \sec x &= \sum^\infty_{n=0} {(-1)^n E_{2n} \over (2n)!} x^{2n}
                     &&= 1 + {x^2 \over 2} + {5x^4 \over 24} + \cdots
                      && |x| < {π \over 2}, ~E_k = \text{Euler numbers}     \h7 \\
          \sin^{-1} x &= \sum^\infty_{n=0} {(2n)! \over 4^n (n!)^2 (2n+1)} x^{2n+1}
                     &&= x + {x^3 \over 6} + {3x^5 \over 40} + \cdots
                      && |x| \le 1                                          \h7 \\
          \cos^{-1} x &= {π \over 2}-\arcsin x
                     &&= {π \over 2} - x - {x^3 \over 6} - {3x^5 \over 40} + \cdots
                      && |x| \le 1                                          \h7 \\
          \tan^{-1} x &= \sum^\infty_{n=0} {(-1)^n \over 2n+1} x^{2n+1}
                     &&= x -{x^3 \over 3} + {x^5 \over 5} + \cdots
                      && |x| \le 1, ~x \neq \pm i                           \h7 \\[2em]
              \sinh x &= \sum^\infty_{n=0} {1 \over (2n+1)!} x^{2n+1}
                     &&= x + {x^3 \over 3!} + {x^5 \over 5!} + \cdots       \h7 \\
              \cosh x &= \sum^\infty_{n=0} {1 \over (2n)!} x^{2n}
                     &&= 1 + {x^2 \over 2!} + {x^4 \over 4!} + \cdots       \h7 \\
              \tanh x &= \sum^\infty_{n=1} {B_{2n} 4^n \left(4^n-1\right) \over (2n)!} x^{2n-1}
                     &&= x - {x^3 \over 3} + {2x^5 \over 15}-{17x^7 \over 315} + \cdots
                      && |x| < {π \over 2}, ~B_k = \text{Bernoulli numbers} \h7 \\
         \sinh^{-1} x &= \sum^\infty_{n=0} {(-1)^n (2n)! \over 4^n (n!)^2 (2n+1)} x^{2n+1}
                    &&&& |x| \le 1                                          \h7 \\
         \tanh^{-1} x &= \sum^\infty_{n=0} {1 \over 2n+1} x^{2n+1}
                    &&&& |x| \le 1, ~x \neq \pm 1                           \h7 \\
  \end{aligned}
\]


Notice Euler's formula here: $e^{ix} = \cos x + i \sin x$! Plug in $x = π$ for Euler's identity: $e^{iπ} + 1 = 0$

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
    \text{and}~~~ 0 ~\lt~ \lim_{n \to \infty} {a_n \over b_n} ~\lt~ \infty, \h4 \\
    \text{then}~~~ \sum_{n=k}^\infty a_n ~~~\text{and}~~~ \sum_{n=k}^\infty b_n ~~~
    \text{either both converge or both diverge.} \h7 \\
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
    \text{where}~~~ b_n \ge 0 ~\forall n \in \mathbb{S}, \h4 \\
    \text{if}~~ \lim_{n\to\infty} b_n = 0 ~~~\text{and}~~~ b_n \ge b_{n+1} ~\forall n \in \mathbb{S}, ~~~
    \text{then}~~~ \sum_{n=k}^\infty a_n ~~~ \text{converges.} \h7 \\
  \end{gathered}
\]

### Absolute Convergence Test

\[
  \begin{gathered}
    \text{If}~~~ \sum |a_n| ~~~\text{converges, then}~~~ \sum a_n ~~~\text{converges absolutely.} \h4 \\
    \text{If}~~~ \sum |a_n| ~~~\text{diverges and}~~~ \sum a_n ~~~\text{converges}, ~
    \text{then}~~~ \sum a_n ~~~\text{converges conditionally.} \h4 \\
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
    \text{where}~~~ b_n \ge 0 ~\forall n \in \mathbb{S}, \h4 \\
    \text{if}~~ \lim_{n\to\infty} b_n = 0 ~~~\text{and}~~~ b_n \ge b_{n+1} ~\forall n \in \mathbb{S}, ~~~
    \text{then}~~ \h4 \\
    \sum_{n=1}^k a_n - |a_{k+1}|
    ~~~~~\le~~~~~ \sum_{n=1}^\infty a_n ~~~~~\le~~~~~
    \sum_{n=1}^k a_n + |a_{k+1}| \h7 \\
  \end{gathered}
\]

## Integrating & Differentiating

The sum/difference rule applies:

\[
  \begin{aligned}
    \drv{x} \sum_{n=0}^\infty f(x) &= \drv{x} f(0) + \drv{x} f(1) + \cdots \h7 \\
                              &= \sum_{n=0}^\infty   \drv{x} f(x)          \h7 \\[1em]
    \int    \sum_{n=0}^\infty f(x) &= \int    f(0) + \int    f(1) + \cdots \h7 \\
                              &= \sum_{n=0}^\infty   \int    f(x)          \h7 \\
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

## Example: Interval of Convergence

What is the interval of convergence of $\sum_{n=1}^\infty {x^n \over n5^n}$?

\[
  \begin{aligned}
    \lim_{n \to \infty} \left| {{x^{n+1} \over (n+1)5^{n+1}} \over {x^n \over n5^n}} \right|
    &= \lim_{n \to \infty} \left| {x^{n+1} \over (n+1)5^{n+1}} \cdot {n5^n \over x^n} \right| \\
    &= \lim_{n \to \infty} \left| {x\c{x^n} \over 5(n+1)\c{5^n}} \cdot {n\c{5^n} \over \c{x^n}} \right| \\
    &= \lim_{n \to \infty} \left| {x n \over 5n + 5} \right| \\
    &= \lim_{n \to \infty} \left| {x \over 5 + \ct{5 \over n}{0}} \right| \\
    &= \left| {x \over 5} \right| \\[1em]
    & -1 < {x \over 5} < 1 \\
    & -5 < x < 5 \\[1em]
    \sum_{n=1}^\infty {\c{(5)^n} \over n \c{5^n}}
    &= \sum_{n=1}^\infty {1 \over n} \\
    &= \sum_{n=1}^\infty {1 \over n^1} \\
    & ~~\text{diverges - harmonic series} \\[1em]
    \sum_{n=1}^\infty {(-5)^n \over n 5^n}
    &= \sum_{n=1}^\infty {(-1)^n\c{(5)^n} \over n \c{5^n}} \\
    &= \sum_{n=1}^\infty {1 \over n} \\
    &= \sum_{n=1}^\infty {(-1)^n \over n} \\
    & ~~\text{converges - alternating series test} \\[1em]
    \text{Interval of Convergence} &= -5 \le x \lt 5
  \end{aligned}
\]

## Example: Power Series From $\cos x$

\[
  \begin{aligned}
    g(x) &= \cos x \approx 1 - {x^2 \over 2!} + {x^4 \over 4!} - {x^6 \over 6!} + {x^8 \over 8!} - \cdots \\
    f(x) &= x^3 \cos x^2 \\
         &= x^3g(x^2) \\
         &\approx x^3\(1 - {(x^2)^2 \over 2!} + {(x^2)^4 \over 4!} - {(x^2)^6 \over 6!} + {(x^2)^8 \over 8!} - \cdots) \\
         &\approx x^3\(1 - {x^4 \over 2!} + {x^8 \over 4!} - {x^{12} \over 6!} + {x^{16} \over 8!} - \cdots) \\
         &\approx x^3 - {x^7 \over 2!} + {x^{11} \over 4!} - {x^{15} \over 6!} + {x^{19} \over 8!} - \cdots \\
  \end{aligned}
\]

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
