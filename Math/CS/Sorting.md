# Sorting

Best case: $Θ(n \log n)$

# Bubble sort

Example:

\[
  \begin{array}{cccc}
    1 & 2 & 3 & 4 \h3 \\[.5em]
    \hline
     \bl8  & \bl6 & \bl2 & \bl2 \h3 \\
     \bl6  & \bl2 & \bl6 &    5 \h3 \\
     \bl2  & \bl8 &    5 &    6 \h3 \\
   \bl{10} &    5 &    8 &    8 \h3 \\
        5  &   10 &   10 &   10 \h3 \\
  \end{array}
\]

Time complexity:

\[
  f(n) = (n-1) + (n-2) + (n-3) + \ldots + 1 = \frac{n(n-1)}{2} = \frac{n^2}{2} - \frac{n}{2}
\]

\[
  \begin{gathered}
    c = 1, x_0 = 0: \\[.5em]
    \forall n \geq \mathbf{0}, f(n) \leq \mathbf{1}n^2 \implies \text{O}(n^2) \\[1em]
    \text{pick } c = \tfrac{1}{3}: \\[.5em]
    \begin{aligned}
      \tfrac{n^2}{2} - \tfrac{n}{2} &\ge \tfrac{1}{3}n^2 \\
      \tfrac{n^2}{6} - \tfrac{n}{2} &\ge 0 \\
                           n^2 - 3n &\ge 0 \\
                           n(n - 3) &\ge 0 \\
                                  n &\ge 3 \\
    \end{aligned} \\[.5em]
    \forall n \geq \mathbf{3}, f(n) \geq \mathbf{\tfrac{1}{3}}n^2 \implies \Omega(n^2) \\
  \end{gathered}
\]
