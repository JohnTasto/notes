# Sequences & Series

## Definitions

**Sequence**: an ordered list of real numbers
**Series**: a sum of a sequence


## Arithmetic

### Sequence

\[
  \begin{matrix}
    \{a,~a+d,~a+2d,~a+3d,~...\} \\[1.5em]
    \begin{aligned}
      x_n &= a + d(n - 1) &             &      \text{Explicit}  \\[.5em]
      x_n &= x_{n-1} + d  & \atop\Big\} & \atop\text{Recursive} \\[-1.25em]
      x_1 &= a                                                  \\
    \end{aligned} \\
    \begin{aligned}
      d &= \text{common difference between terms} \\
      a &= \text{first term}
    \end{aligned}
  \end{matrix}
\]

### Series

#### Partial sum

\[
  \begin{aligned}
    s_n &= \sum_{k=1}^n a + d(k-1)      \\[1.25em]
        &= \tfrac{1}{2}n(a + x_n)       \\[.5em]
        &= \tfrac{1}{2}n(2a + d(n - 1))
  \end{aligned}
\]

#### Infinite sum

An infinite arithmetic sequence never converges.


## Geometric

### Sequence

\[
  \begin{matrix}
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
  \end{matrix}
\]


### Series

#### Partial sum

\[
  \begin{aligned}
    s_n &= \sum_{k=1}^n ar^{k-1}     \\[1.25em]
        &= \frac{x_{n+1} - a}{r - 1} \\[.75em]
        &= \frac{a(r^n - 1)}{r - 1}  \\[.75em]
        &= \frac{a(1 - r^n)}{1 - r}
  \end{aligned}
\]

#### Infinite sum

An infinite geometric sum converges when $|r| < 1$.

\[
  \begin{matrix}
    \begin{aligned}
      s &= \sum_{k=0}^\infty ar^k                                     \\[1.25em]
        &= \lim_{n \to \infty} \sum_{k=0}^n ar^k                      \\[1.25em]
        &= \lim_{n \to \infty} \frac{a(1 - r^{n+1})}{1 - r}           \\[1em]
        &= \frac{a}{1-r} - \lim_{n \to \infty} \frac{ar^{n+1}}{1 - r} \\[1em]
        &= \frac{a}{1-r}                                              \\
    \end{aligned} \\
    |r| < 1
  \end{matrix}
\]
