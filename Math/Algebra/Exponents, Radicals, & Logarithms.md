# Exponents, Radicals, & Logarithms

## Rules

### Exponents

\[
  \begin{matrix}
    \begin{aligned}
                     \kern{4em} & \kern{8em}                       && \kern{12em}                       \\
                            a^1 &= a                               &&                                   \\[.25em]
                            a^0 &= 1                               && a \neq 0                          \\[2em]
                         (ab)^n &= a^n b^n                         && \text{Power of Product}           \\[.5em]
     \left(\frac{a}{b}\right)^n &= \frac{a^n}{b^n}                 && \text{Power of Quotient}          \\[1em]
                        (a^m)^n &= a^{mn}                          && \text{Power of Power}             \\[2em]
                        a^m b^n &= a^{m+n}                         && \text{Product of Powers}          \\[.5em]
                \frac{a^m}{a^n} &= a^{m-n}                         && \text{Quotient of Powers}         \\[2em]
                         a^{-n} &= \frac{1}{a^n}                   && \text{Negative Power}             \\[1em]
                  a^\frac{m}{n} &= \sqrt[n]{a^m}                   && \text{Fractional Power}           \\[1em]
                  a^\frac{1}{n} &= \sqrt[n]{a}                     && \text{Reciprocal Power}           \\
    \end{aligned} \\
    \begin{aligned}
      n &\in \mathbb{Z}
    \end{aligned}
  \end{matrix}
\]

### Radicals

\[
  \begin{matrix}
    \begin{aligned}
                     \kern{4em} & \kern{8em}                       && \kern{12em}                       \\
                  \sqrt[n]{a^n} &= |a|                    ,~n \in \mathbb{E}                 \\[.25em]
                  \sqrt[n]{a^n} &= \phantom{|}a\phantom{|},~n \in \mathbb{O}                  \\[.25em]
                 \sqrt[mn]{a^n} &= \sqrt[m]{a}                     &&                                   \\[2em]
                   \sqrt[n]{ab} &= \sqrt[n]{a} \cdot \sqrt[n]{b}   && \text{Root of Product}            \\[.75em]
          \sqrt[n]{\frac{a}{b}} &= \frac{\sqrt[n]{a}}{\sqrt[n]{b}} && \text{Root of Quotient}           \\[1.25em]
                  \sqrt[n]{a^m} &= (\sqrt[n]{a})^m                 && \text{Root of Power}              \\[.75em]
          \sqrt[n]{\sqrt[m]{a}} &= \sqrt[nm]{a}                    && \text{Root of Root}               \\[2em]
         \sqrt[n]{a}\sqrt[m]{b} &= \sqrt[mn]{a^mb^n}               && \text{Product of Roots}           \\
    \end{aligned}
  \end{matrix}
\]

### Logarithms

\[
  \begin{matrix}
    \begin{aligned}
                     \kern{4em} & \kern{8em}                       && \kern{12em}                       \\
                    \log_a b = c &\equiv a^c = b                   && \text{Definition}                 \\[2em]
                       \log_a a &= 1                               &&                                   \\[.25em]
                       \log_a 1 &= 0                               && a > 0                             \\[.25em]
                     \log_a a^n &= n                               &&                                   \\[.25em]
                   a^{\log_a b} &= b                               &&                                   \\[2em]
                    \log_a (bc) &= \log_a b + \log_a c             && \text{Log of Product}             \\[1em]
              \log_a\frac{b}{c} &= \log_a b - \log_a c             && \text{Log of Quotient}            \\[1em]
              \log_a\frac{1}{c} &= -\log_a c                       && \text{Log of Reciprocal}          \\[1.5em]
                     \log_a b^m &= m \log_a b                      && \text{Log of Power}               \\[1.25em]
            \log_a\sqrt[n]{b^m} &= \frac{m}{n}\log_a b             && \text{Log of Fractional Exponent} \\[1em]
              \log_a\sqrt[n]{b} &= \frac{1}{n}\log_a b             && \text{Log of Root}                \\[2em]
                       \log_a b &= \frac{\log_c b}{\log_c a}       && \text{Change of Base}             \\[1em]
                       \log_a b &= \frac{1}{\log_b a}              && \text{Change of Base}             \\
    \end{aligned} \\
    \begin{aligned}
      a, b &> 0 \\
         a &\neq 1
    \end{aligned}
  \end{matrix}
\]

## Rationalizing the Denominator

\[
  \begin{matrix}
    \begin{aligned}
           \frac{a}{\sqrt{b}} &= \frac{a}{\sqrt{b}} \cdot \frac{\sqrt{b}}{\sqrt{b}} \\[1em]
                              &= \frac{a\sqrt{b}}{b} \\[1.5em]
       \frac{a}{b\pm\sqrt{c}} &= \frac{a}{b\pm\sqrt{c}} \cdot \frac{b\mp\sqrt{c}}{b\mp\sqrt{c}} \\[1em]
                              &= \frac{ab\mp a\sqrt{c}}{b^2-c} \\[1.5em]
\frac{a}{\sqrt{b}\pm\sqrt{c}} &= \frac{a}{\sqrt{b}\pm\sqrt{c}} \cdot \frac{\sqrt{b}\mp\sqrt{c}}{\sqrt{b}\mp\sqrt{c}} \\[1em]
                              &= \frac{a\sqrt{b}\mp a\sqrt{c}}{b-c} \\[4em]
        \frac{a}{\sqrt[n]{b}} &= \frac{a}{\sqrt[n]{b}} \cdot \frac{\sqrt[n]{b^{n-1}}}{\sqrt[n]{b^{n-1}}} \\[1em]
                              &= \frac{a \sqrt[n]{b^{n-1}}}{b} \\[1.5em]
      \frac{a}{\sqrt[n]{b^m}} &= \frac{a}{\sqrt[n]{b^m}} \cdot \frac{\sqrt[n]{b^{n-m}}}{\sqrt[n]{b^{n-m}}} \\[1em]
                              &= \frac{a \sqrt[n]{b^{n-m}}}{b} \\[1.5em]
      \frac{a}{b-\sqrt[n]{c}} &= \frac{a}{b-\sqrt[n]{c}} \cdot \frac
        {(b^{n-1}\sqrt[n]{c^0} + b^{n-2}\sqrt[n]{c^1} + \ldots + b^1\sqrt[n]{c^{n-2}} + b^0\sqrt[n]{c^{n-1}})}
        {(b^{n-1}\sqrt[n]{c^0} + b^{n-2}\sqrt[n]{c^1} + \ldots + b^1\sqrt[n]{c^{n-2}} + b^0\sqrt[n]{c^{n-1}})} \\[1em]
                              &= \frac
        {a(b^{n-1}\sqrt[n]{c^0} + b^{n-2}\sqrt[n]{c^1} + \ldots + b^1\sqrt[n]{c^{n-2}} + b^0\sqrt[n]{c^{n-1}})}
        {b^n - c} \\[1.5em]
    \end{aligned} \\
    a > 0, b > 0, c > 0
  \end{matrix}
\]

Some random example
\[
  \begin{aligned}
      & -13\sqrt{x^3} + 2\sqrt{y^5} + 5x\sqrt{x} - 8y^2\sqrt{y} \\
    = & -13\sqrt{x^2 \cdot x} + 2\sqrt{y^2 \cdot y^2 \cdot y} + 5x\sqrt{x} - 8y^2\sqrt{y} \\
    = & -13\sqrt{x^2}\sqrt{x} + 2\sqrt{y^2}\sqrt{y^2}\sqrt{y} + 5x\sqrt{x} - 8y^2\sqrt{y} \\
    = & -13(x)\sqrt{x} + 2(y)(y)\sqrt{y} + 5x\sqrt{x} - 8y^2\sqrt{y} \\
    = & -13x\sqrt{x} + 2y^2\sqrt{y} + 5x\sqrt{x} - 8y^2\sqrt{y} \\
    = & -13x\sqrt{x} + 5x\sqrt{x} + 2y^2\sqrt{y} - 8y^2\sqrt{y} \\
    = & -8x\sqrt{x} + 6y^2\sqrt{y} \\
  \end{aligned}
\]
