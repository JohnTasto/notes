# Bubble sort

Example:

|    1     |    2    |    3    |    4    |
| :------: | :-----: | :-----: | :-----: |
| _**8**_  | _**6**_ | _**2**_ | _**2**_ |
| _**6**_  | _**2**_ | _**6**_ |    5    |
| _**2**_  | _**8**_ |    5    |    6    |
| _**10**_ |    5    |    8    |    8    |
|    5     |   10    |   10    |   10    |

Time complexity:

\[
  f(n) = (n-1) + (n-2) + (n-3) + \ldots + 1 = \frac{n(n-1)}{2} = \frac{n^2}{2} - \frac{n}{2}
\]

\[
  \begin{matrix}
    c = 1, x_0 = 0: \\
    \forall n \geq \mathbf{0}, f(n) \leq \mathbf{1}n^2 \Longrightarrow \text{O}(n^2)
  \end{matrix}
\]

\[
  \begin{matrix}
    \text{pick } c = \tfrac{1}{3}: \\[.2em]
    \begin{aligned}
      \tfrac{n^2}{2} - \tfrac{n}{2} & \geq \tfrac{1}{3}n^2 \\[.2em]
      \tfrac{n^2}{6} - \tfrac{n}{2} & \geq 0 \\[.2em]
      n^2 - 3n & \geq 0 \\
      n(n - 3) & \geq 0 \\
      n & \geq 3 \\
    \end{aligned} \\
    \forall n \geq \mathbf{3}, f(n) \geq \mathbf{\tfrac{1}{3}}n^2 \Longrightarrow \Omega(n^2)
  \end{matrix}
\]
