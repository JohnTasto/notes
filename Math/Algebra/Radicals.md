# Radicals

## Rules

\[
  \begin{matrix}
    \begin{aligned}
                     \kern{4em} & \kern{8em}                       && \kern{12em}                       \\
                  \sqrt[n]{a^n} &= |a|                    ,~n \in \mathbb{E}                            \\[.25em]
                  \sqrt[n]{a^n} &= \phantom{|}a\phantom{|},~n \in \mathbb{O}                            \\[.25em]
                 \sqrt[mn]{a^n} &= \sqrt[m]{a}                     &&                                   \\[2em]
                   \sqrt[n]{ab} &= \sqrt[n]{a} \cdot \sqrt[n]{b}   && \text{Root of Product}            \\[.75em]
          \sqrt[n]{\frac{a}{b}} &= \frac{\sqrt[n]{a}}{\sqrt[n]{b}} && \text{Root of Quotient}           \\[1.25em]
                  \sqrt[n]{a^m} &= (\sqrt[n]{a})^m                 && \text{Root of Power}              \\[.75em]
          \sqrt[n]{\sqrt[m]{a}} &= \sqrt[nm]{a}                    && \text{Root of Root}               \\[2em]
         \sqrt[n]{a}\sqrt[m]{b} &= \sqrt[mn]{a^mb^n}               && \text{Product of Roots}           \\
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
