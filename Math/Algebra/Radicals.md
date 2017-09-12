# Radicals

## Rules

\[
  \newcommand\bs{\vpppp}
  \newcommand\ls{\vpp}
  \begin{aligned}
             \sqrt[n]{a^n} &= |a|                    , ~n \in \mathbb{E}                 \ls \\
             \sqrt[n]{a^n} &= \phantom{|}a\phantom{|}, ~n \in \mathbb{O}                 \ls \\
            \sqrt[mn]{a^n} &= \sqrt[m]{a}                     &&                         \ls \\[1em]
              \sqrt[n]{ab} &= \sqrt[n]{a} \cdot \sqrt[n]{b}   && \text{Root of Product}  \bs \\
       \sqrt[n]{a \over b} &= {\sqrt[n]{a} \over \sqrt[n]{b}} && \text{Root of Quotient} \bs \\
             \sqrt[n]{a^m} &= (\sqrt[n]{a})^m                 && \text{Root of Power}    \bs \\
     \sqrt[n]{\sqrt[m]{a}} &= \sqrt[nm]{a}                    && \text{Root of Root}     \bs \\[1em]
    \sqrt[n]{a}\sqrt[m]{b} &= \sqrt[mn]{a^mb^n}               && \text{Product of Roots} \bs \\
  \end{aligned}
\]

## Rationalizing the Denominator

\[
  \begin{matrix}
    \begin{aligned}
           {a \over \sqrt{b}} &= {a \over \sqrt{b}} \cdot {\sqrt{b} \over \sqrt{b}}                                  \bs \\
                              &= {a\sqrt{b} \over b}                \bs \\[1em]
       {a \over b\pm\sqrt{c}} &= {a \over b\pm\sqrt{c}} \cdot {b\mp\sqrt{c} \over b\mp\sqrt{c}}                      \bs \\
                              &= {ab\mp a\sqrt{c} \over b^2-c}      \bs \\[1em]
{a \over \sqrt{b}\pm\sqrt{c}} &= {a \over \sqrt{b}\pm\sqrt{c}} \cdot {\sqrt{b}\mp\sqrt{c} \over \sqrt{b}\mp\sqrt{c}} \bs \\
                              &= {a\sqrt{b}\mp a\sqrt{c} \over b-c} \bs \\[3em]
        {a \over \sqrt[n]{b}} &= {a \over \sqrt[n]{b}} \cdot {\sqrt[n]{b^{n-1}} \over \sqrt[n]{b^{n-1}}}             \bs \\
                              &= {a \sqrt[n]{b^{n-1}} \over b}      \bs \\[1em]
      {a \over \sqrt[n]{b^m}} &= {a \over \sqrt[n]{b^m}} \cdot {\sqrt[n]{b^{n-m}} \over \sqrt[n]{b^{n-m}}}           \bs \\
                              &= {a \sqrt[n]{b^{n-m}} \over b}      \bs \\[1em]
      {a \over b-\sqrt[n]{c}} &= {a \over b-\sqrt[n]{c}} \cdot \frac
        {(b^{n-1}\sqrt[n]{c^0} + b^{n-2}\sqrt[n]{c^1} + \ldots + b^1\sqrt[n]{c^{n-2}} + b^0\sqrt[n]{c^{n-1}})}
        {(b^{n-1}\sqrt[n]{c^0} + b^{n-2}\sqrt[n]{c^1} + \ldots + b^1\sqrt[n]{c^{n-2}} + b^0\sqrt[n]{c^{n-1}})}       \bs \\
                              &= \frac
        {a(b^{n-1}\sqrt[n]{c^0} + b^{n-2}\sqrt[n]{c^1} + \ldots + b^1\sqrt[n]{c^{n-2}} + b^0\sqrt[n]{c^{n-1}})}
        {b^n - c}                                                   \bs \\
    \end{aligned} \\
    a > 0, b > 0, c > 0 \ls \\
  \end{matrix}
\]

Some random example
\[
  \begin{aligned}
      & -13\sqrt{x^3} + 2\sqrt{y^5} + 5x\sqrt{x} - 8y^2\sqrt{y}                           \ls \\
    = & -13\sqrt{x^2 \cdot x} + 2\sqrt{y^2 \cdot y^2 \cdot y} + 5x\sqrt{x} - 8y^2\sqrt{y} \ls \\
    = & -13\sqrt{x^2}\sqrt{x} + 2\sqrt{y^2}\sqrt{y^2}\sqrt{y} + 5x\sqrt{x} - 8y^2\sqrt{y} \ls \\
    = & -13(x)\sqrt{x} + 2(y)(y)\sqrt{y} + 5x\sqrt{x} - 8y^2\sqrt{y}                      \ls \\
    = & -13x\sqrt{x} + 2y^2\sqrt{y} + 5x\sqrt{x} - 8y^2\sqrt{y}                           \ls \\
    = & -13x\sqrt{x} + 5x\sqrt{x} + 2y^2\sqrt{y} - 8y^2\sqrt{y}                           \ls \\
    = & -8x\sqrt{x} + 6y^2\sqrt{y}                                                        \ls \\
  \end{aligned}
\]
