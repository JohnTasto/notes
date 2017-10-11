# Recurrence Relations

## Repeated Substitution

### Interest

\[
  \begin{align}
      M(i) &= 1.1\b(M(i-1)\b)                                         \tag{1} \h3 \\
      M(0) &= 100                                                             \h3 \\[1em]
    M(i-1) &= 1.1\b(M(i-2)\b)              && \text{Use (1) to find $M(n-1)$} \h3 \\
      M(i) &= 1.1\bb(1.1\b(M(i-2)\b)\bb)   && \text{Plug $M(n-1)$ into (1)}   \h3 \\
           &= 1.1^2\b(M(i-2)\b)                                       \tag{2} \h3 \\[1em]
    M(i-2) &= 1.1\b(M(i-3)\b)              && \text{Use (1) to find $M(n-2)$} \h3 \\
      M(i) &= 1.1^2\bb(1.1\b(M(i-3)\b)\bb) && \text{Plug $M(n-2)$ into (2)}   \h3 \\
           &= 1.1^3\b(M(i-3)\b)                                       \tag{3} \h3 \\[1em]
    M(i-3) &= 1.1\b(M(i-4)\b)              && \text{Use (1) to find $M(n-3)$} \h3 \\
      M(i) &= 1.1^3\bb(1.1\b(M(i-4)\b)\bb) && \text{Plug $M(n-3)$ into (3)}   \h3 \\
           &= 1.1^4\b(M(i-4)\b)                                               \h3 \\[1em]
      M(i) &= 1.1^rM(i-r)        && \text{Use a new variable to describe pattern} \h3 \\
           &= 1.1^iM(0)          && \text{Choose $r$ that removes $M(i-r):~$ let $r = i$} \h3 \\
           &= 1.1^i(100)         && \text{Substitute base case} \h3 \\
  \end{align}
\]

### Binary Search

\[
  \begin{align}
           T(n) &= 1 + T(\tf{n}2)                                    \tag{1} \h3 \\
           T(1) &= 0                                                         \h3 \\[1em]
     T(\tf{n}2) &= 1 + T(\tf{n}4)     && \text{Use (1) to find $T(\tf{n}2)$} \h3 \\
           T(n) &= 1 + 1 + T(\tf{n}4) && \text{Plug $T(\tf{n}2)$ into (1)}   \h3 \\
                &= r + T(\tf{n}{2^r})                                        \h3 \\[1em]
    \tf{n}{2^r} &= 1     \h3 \\
              n &= 2^r   \h3 \\
              r &= \lg n \h3 \\[1em]
           T(n) &= \lg n \h3 \\
  \end{align}
\]

### Towers of Hanoi

\[
  \begin{align}
        T(n) &= 2T(n-1) + 1 \h3 \\
        T(0) &= 0 \h3 \\[1em]
    T(n-1) &= 2T(n-2) + 1 \h3 \\
        T(n) &= 2\b(2T(n-2) + 1\b) + 1 \h3 \\[1em]
        T(n) &= 2^2T(n-2) + 2 + 1 && \text{Skipping ahead a bit...} \h3 \\
        T(n) &= 2^3T(n-3) + 4 + 2 + 1 \h3 \\
        T(n) &= 2^4T(n-4) + 8 + 4 + 2 + 1 \h3 \\[1em]
        T(n) &= 2^rT(n-r) + 2^{r-1} + 2^{r-2} + \cdots + 1 \h3 \\
        T(n) &= \c{2^nT(n-n)} + 2^{n-1} + 2^{n-2} + \cdots + 1 && \text{Let $r = n$} \h3 \\
        T(n) &=   1+    2 + 4 + \cdots + 2^{n-1} \h3 \\
       2T(n) &=\p{1+{}} 2 + 4 + \cdots + 2^{n-1} + 2^n \h3 \\[1em]
        T(n) &= 2^n - 1 \h3 \\
  \end{align}
\]

### Chinese Ring Puzzle

```
  chineseRing(n)
    chineseRing(n-2)
    remove hardest ring
    chineseRingReverse(n-2)
    chineseRing(n-1)
```
note: each iteration is a consecutive grey code
\[
  \begin{aligned}
    \heading[3em]{From algorithm:} \\
        T(1) &= 1 \\
        T(2) &= 2 \\
        T(n) &= T(n-1) + 2T(n-2) + 1 \\[1em]
    \heading[3em]{Hypotheses from table:} \\
        T(n) &\? \begin{cases}
          2T(n-1)     & n \in \mathbb{E} \\
          2T(n-1) + 1 & n \in \mathbb{O} \\
        \end{cases} \\[1em]
    \heading[3em]{To prove hypotheses by induction, assume:} \\
    T(n-1) &= \begin{cases}
          2T(n-2)     & n{-}1 \in \mathbb{E} \\
          2T(n-2) + 1 & n{-}1 \in \mathbb{O} \\
        \end{cases} \\[1em]
    \heading[3em]{For $n \in \mathbb{E}$:} \\
        T(n) &= T(n-1) + \ct{2T(n-2) + 1}{T(n-1)} \\
            &= 2T(n-1) && \qed \\[1em]
    \heading[3em]{For $n \in \mathbb{O}$:} \\
        T(n) &= T(n-1) + \ct{2T(n-2)}{T(n-1)} + 1 \\
            &= 2T(n-1) + 1 && \qed \\[1em]
    \heading[3em]{Solve recurrence equation for $n \in \mathbb{E}$:} \\
        T(n) &= 2\b(2T(n-2) + 1\b)                   && \hs{\text{drop one level down}} \\
            &= 4T(n-2) + 2                           && \hs{\text{now just use this for evens}} \\[1em]
        T(n) &= 4\b(4T(n-4) + 2\b) + 2               && \hs{\text{now start dropping two levels}} \\
            &= 4^2T(n-4) + 4 \cdot 2 + 2 \\[1em]
        T(n) &= 4^2\b(4T(n-6) + 2\b) + 4 \cdot 2 + 2 && \hs{\text{two more levels}} \\
            &= 4^3T(n-6) + 4^2 \cdot 2 + 4 \cdot 2 + 2 \\[1em]
        T(n) &= \hs{4^rT(n-2r) + 2(1 + 4 + 4^2 + \cdots + 4^{r-1})} \\[1em]
          x &=        1 +   4 + 4^2 + \cdots + 4^{r-1} \\
         4x &= \hs{\p{1 +{}}4 + 4^2 + \cdots + 4^{r-1} + 4^r} \\
         3x &= 4^r - 1 \\
          x &= \tf{4^r - 1}{3} \\[1em]
     n - 2r &= 2 \\
          r &= \tf{n - 2}{2} \\[1em]
        T(n) &= 4^{n-2 \/ 2}(2) + 2\({4^{n-2 \/ 2} - 1 \/ 3}) \\
            &= \tf23(2^n - 1) \\[1em]
    \heading[3em]{Solve recurrence equation for $n \in \mathbb{O}$:} \\
        T(n) &= 2\b(2T(n-2)\b) + 1 \\
            &= 4T(n-2) + 1 \\
            & \cdots \\
            &= \tf13(2^{n+1} - 1)
  \end{aligned}
  \begin{gathered}
    \qquad \begin{array}{c|c}
      n & T(n) \\
      \hline
      1 & 1 \\
      2 & 2 \\
      3 & 5 \\
      4 & 10 \\
      5 & 21 \\
      6 & 42 \\
      7 & 85 \\
      8 & 170 \\
    \end{array} \\
    \Strut{26em} \\
  \end{gathered}
\]

## Master Theorem

\[
  T(n) = aT(\tf{n}{b}) + f(n) \\[1em]
  \begin{aligned}
    T(n) &= Θ(n^{\log_b a}) &&
    \text{if } f(n) = \O(n^{\log_b a - ϵ}) \h4 \\
    T(n) &= Θ(n^{\log_b a} \lg n) &&
    \text{if } f(n) = Θ(n^{\log_b a}) \h4 \\
    T(n) &= Θ(f(n)) &&
    \text{if } f(n) = Ω(n^{\log_b a + ϵ}),
    \text{and } af(\tf{n}{b}) \le cf(n) \text{ for all sufficiently large } n \h4 \\
  \end{aligned} \\[3em]
  \text{where } ϵ > 0 \text{ and } c < 1 \\
\]

## Variable Substitution

\[
  \begin{aligned}
    T(n) &= 2T(n-1) + 1 \\[1em]
    S(n) &= T(n) + 1 \\
    T(n) &= S(n) - 1 &&
    \gtext{1em}{Substitute} \\[1em]
    S(n) - 1 &= 2\b(S(n - 1) - 1 \b) + 1 \\
    S(n) &= 2S(n - 1) \\[1em]
    S(n) &= 2^n \\[1em]
    T(n) &= 2^n - 1 \\
  \end{aligned}
\]

## Guess and Prove by Induction

\[
  \begin{aligned}
    T(n) &\le T(\tf{n}{5}) + T(\tf{7n}{10}) + 15n \\
    T(n \le 5) &\le 5 \\[1em]
    T(n) &\? Kn \\[1em]
    T(\tf{n}{5}) &\le \tf{Kn}{5} \\
    T(\tf{7n}{10}) &\le \tf{7Kn}{10} \\[1em]
    T(n) &\le \tf{Kn}{5} + \tf{7Kn}{10} + 15n \\
    &= \tf{9Kn}{10} + 15n \\[1em]
    \tf{9Kn}{10} + 15n &\?[\le] Kn \\
    \tf{9K}{10} + 15 &\?[\le] K \\
    150 &\le K
  \end{aligned}
\]

## Linear Homogeneous Equations

\[
  \begin{aligned}
    \heading[3em]{Given recurrence equation} \h3 \\[.5em]
    a_n &= c_1a_{n-1} + c_2a_{n-2} + \cdots + c_ka_{n-k} \h3 \\[.5em]
    \heading[3em]{and roots $r_1 \ldots r_k$ of the characteristic equation} \h3 \\[.5em]
    0 &= r^k - c_1r^{k-1} - c_2r^{k-2} - \cdots - c_k, \h3 \\[.5em]
    \heading[3em]{the closed form solution when $r_1 \ldots r_k$ are all distinct is} \h3 \\[.5em]
    a_n &= α_1r_1^n + α_2r_2^n + \cdots + α_kr_k^n \h3 \\[.5em]
    \heading[3em]{where $α_1 \ldots α_k$ are the solutions to the system of equations resulting} \h3 \\
    \heading[3em]{from substituting in $k$ initial values.} \h3 \\[1em]
    \heading[3em]{The general closed form solution when any roots $r_1 \ldots r_k$ are repeated is} \h3 \\[.5em]
    a_n &=             (α_{1,1} + α_{1,2}n^1 + α_{1,3}n^2 + \cdots + α_{1,m_1}n^{m_1 - 1})r_1^n \h3 \\
        &\pc{{}={}}{+} (α_{2,1} + α_{2,2}n^1 + α_{2,3}n^2 + \cdots + α_{2,m_2}n^{m_2 - 1})r_2^n \h3 \\
        &\pc{{}={}}{+} \cdots \h3 \\
        &\pc{{}={}}{+} (α_{k,1} + α_{k,2}n^1 + α_{k,3}n^2 + \cdots + α_{k,m_k}n^{m_k - 1})r_k^n \h3 \\[.5em]
    \heading[3em]{where $m_1 \ldots m_k$ is the multiplicity of each root $r_1 \ldots r_k$.} \h3 \\
  \end{aligned}
\]

## Linear Nonhomogeneous Equations

\[
  \begin{aligned}
    \heading[3em]{Given recurrence equation} \h3 \\[.5em]
    a_n &= c_1a_{n-1} + c_2a_{n-2} + \cdots + c_ka_{n-k} + F(n) \h3 \\[.5em]
    \heading[3em]{where $F(n)$ is the product of a polynomial and an exponential} \h3 \\[.5em]
    F(n) &= P(n) \cdot s^n \h3 \\[.5em]
    \heading[3em]{and roots $r_1 \ldots r_k$ of the characteristic equation} \h3 \\[.5em]
    0 &= r^k - c_1r^{k-1} - c_2r^{k-2} - \cdots - c_k, \h3 \\[.5em]
    \heading[3em]{the particular solution is} \h3 \\[.5em]
    a_n^{(p)} &= n^m(p_tn^t + p_{t-1}n^{t-1} + \cdots + p_1n + p_0)s^n \\[.5em]
    \heading[3em]{where $m$ is the number of times $s$ appears in $r_1 \ldots r_k$,} \h3 \\
    \heading[3em]{$\phantom{\text{where }}\pc{m}{t}$ is the degree of polynomial $P(n)$,} \h3 \\
    \heading[3em]{$\pc{\text{where }m}{~p_1 \ldots p_t}$ are coefficients found by substituting the particular} \h3 \\
    \heading[3em]{$\phantom{\text{where }m}$ solution into the recurrence equation,} \h3 \\[.5em]
    \heading[3em]{and the general solution is the sum of the particular solution and} \h3 \\
    \heading[3em]{the solution to $a_n - F(n)$.} \h3 \\
  \end{aligned}
\]

Example

\[
  \begin{align}
    a_n &= a_{n-1} + n && \text{Triangle numbers} \tag{1} \\
    a_0 &= 0 \\
    a_1 &= 1 \\[1em]
    a_n &= a_{n-1} + n1^n && \text{Linear nonhomogeneous equation} \\[1em]
    0 &= r - 1 && \text{Characteristic equation} \\[1em]
    \heading[3em]{The characteristic equation has one root, $1$, which happens to} \\
    \heading[3em]{equal $s$, so $m = 1$ because $s$ is in $r_1 \ldots r_k$ once.} \\[1em]
    a_n^{(p)} &= n^1(p_0 + p_1n)1^n \\
    &= p_0n + p_1n^2 \tag{2} \\[1em]
    a_n &= p_0(n - 1) + p_1(n - 1)^2 + n && \text{Substitute (2) into (1)} \\
    &= p_0n - p_0 + p_1n^2 - 2p_1n + p_1 + n \\[1em]
    \c{p_0n} + \c{p_1n^2} &= \c{p_0n} - p_0 + \c{p_1n^2} - 2p_1n + p_1 + n \\
    0 &= - p_0 - 2p_1n + p_1 + n \\
    0 &= (1 - 2p_1)n + (p_1 - p_0) && \text{Now set each term to $0$???} \\[1em]
    p_0 &= \tf12 \\
    p_1 &= \tf12 \\[1em]
    a_n &= \tf12n + \tf12n^2 && \text{Substitute $p_0$ and $p_1$ into (2)} \\
    &= \tf{n(n+1)}2 && \text{Particular solution} \\
  \end{align}
\]
