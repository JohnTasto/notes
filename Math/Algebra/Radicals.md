# Radicals

## Rules

\[
  \begin{aligned}
                    \sqrt[n]{a^n} &= |a|        , ~n \in \mathbb{E}                                 \h3 \\
                    \sqrt[n]{a^n} &= \p{|}a\p{|}, ~n \in \mathbb{O}                                 \h3 \\
                   \sqrt[mn]{a^n} &= \vrt[m]{a^n}{a}                     &&                         \h3 \\[1em]
                     \sqrt[n]{ab} &= \vrt[n]{b}{a} \cdot \hrt[n]{a}{b}   && \text{Root of Product}  \h6 \\
    \vrt[n]{b \over b}{a \over b} &= {\vrt[n]{b}{a} \over \hrt[n]{a}{b}} && \text{Root of Quotient} \h6 \\
                    \sqrt[n]{a^m} &= (\vrt[n]{a^m}{a})^m                 && \text{Root of Power}    \h6 \\
      \vrt[n]{a^|}{\vrt[m]{b}{a}} &= \vrt[nm]{b}{a}                      && \text{Root of Root}     \h6 \\[1em]
     \vrt[n]{b^n}{a}\rt[m]{^m}{b} &= \sqrt[mn]{a^mb^n}                   && \text{Product of Roots} \h6 \\
  \end{aligned}
\]

## Rationalizing the Denominator

\[
  \begin{matrix}
    \begin{aligned}
           {a \over \sqrt{b}} &= {a \over \sqrt{b}} \cdot {\sqrt{b} \over \sqrt{b}}                                  \h8 \\
                              &= {a\sqrt{b} \over b}                \h8 \\[1em]
       {a \over b\pm\sqrt{c}} &= {a \over b\pm\sqrt{c}} \cdot {b\mp\sqrt{c} \over b\mp\sqrt{c}}                      \h8 \\
                              &= {ab\mp a\sqrt{c} \over b^2-c}      \h8 \\[1em]
{a \over \sqrt{b}\pm\sqrt{c}} &= {a \over \sqrt{b}\pm\sqrt{c}} \cdot {\sqrt{b}\mp\sqrt{c} \over \sqrt{b}\mp\sqrt{c}} \h8 \\
                              &= {a\sqrt{b}\mp a\sqrt{c} \over b-c} \h8 \\[3em]
        {a \over \sqrt[n]{b}} &= {a \over \sqrt[n]{b}} \cdot {\sqrt[n]{b^{n-1}} \over \sqrt[n]{b^{n-1}}}             \h8 \\
                              &= {a \sqrt[n]{b^{n-1}} \over b}      \h8 \\[1em]
      {a \over \sqrt[n]{b^m}} &= {a \over \sqrt[n]{b^m}} \cdot {\sqrt[n]{b^{n-m}} \over \sqrt[n]{b^{n-m}}}           \h8 \\
                              &= {a \sqrt[n]{b^{n-m}} \over b}      \h8 \\[1em]
      {a \over b-\sqrt[n]{c}} &= {a \over b-\sqrt[n]{c}} \cdot \frac
        {(b^{n-1}\sqrt[n]{c^0} + b^{n-2}\sqrt[n]{c^1} + \ldots + b^1\sqrt[n]{c^{n-2}} + b^0\sqrt[n]{c^{n-1}})}
        {(b^{n-1}\sqrt[n]{c^0} + b^{n-2}\sqrt[n]{c^1} + \ldots + b^1\sqrt[n]{c^{n-2}} + b^0\sqrt[n]{c^{n-1}})}       \h8 \\
                              &= \frac
        {a(b^{n-1}\sqrt[n]{c^0} + b^{n-2}\sqrt[n]{c^1} + \ldots + b^1\sqrt[n]{c^{n-2}} + b^0\sqrt[n]{c^{n-1}})}
        {b^n - c}                                                   \h8 \\
    \end{aligned} \\
    a > 0, b > 0, c > 0 \h3 \\
  \end{matrix}
\]

Some random example
\[
  \begin{aligned}
      & -13\sqrt{x^3} + 2\sqrt{y^5} + 5x\sqrt{x} - 8y^2\sqrt{y}                           \h5 \\
    = & -13\sqrt{x^2 \cdot x} + 2\sqrt{y^2 \cdot y^2 \cdot y} + 5x\sqrt{x} - 8y^2\sqrt{y} \h5 \\
    = & -13\sqrt{x^2}\sqrt{x} + 2\sqrt{y^2}\sqrt{y^2}\sqrt{y} + 5x\sqrt{x} - 8y^2\sqrt{y} \h5 \\
    = & -13(x)\sqrt{x} + 2(y)(y)\sqrt{y} + 5x\sqrt{x} - 8y^2\sqrt{y}                      \h5 \\
    = & -13x\sqrt{x} + 2y^2\sqrt{y} + 5x\sqrt{x} - 8y^2\sqrt{y}                           \h5 \\
    = & -13x\sqrt{x} + 5x\sqrt{x} + 2y^2\sqrt{y} - 8y^2\sqrt{y}                           \h5 \\
    = & -8x\sqrt{x} + 6y^2\sqrt{y}                                                        \h5 \\
  \end{aligned}
\]
