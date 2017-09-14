# Require statements

\[
  \rlap{\phantom{\require{enclose}}}
  \rlap{\phantom{\require{cancel}}}
\]

# Shortcuts
<!-- Because \kern does not scale AT ALL with \tiny, adding \kern, '\,', '\:', or '\;' in front of cgroup  -->
<!-- contents will appear to have no effect. Theses spaces inside \tiny{\phantom} grow at the same rate as -->
<!-- the contents, rather than at the half rate of everything else. '~', \phantom, and \Space still work,  -->
<!-- the latter of which is used to make a replacement \Kern that does scale.                              -->
\[
  \newcommand \h [1] {{ \tiny \raise 1ex \Rule{0em}{#1ex}{#1ex} }}
  \newcommand \H [1] {{ \tiny \raise 1ex \Rule{0em}{#1em}{#1em} }}
  \newcommand  \p [1] {  \phantom{#1} }
  \newcommand \hp [1] { \hphantom{#1} }
  \newcommand \vp [1] { \vphantom{#1} }
  \newcommand \Kern  [1] { \Space{ #1}{0em}{0em} }
  \newcommand \Strut [1] { \Space{0em}{ #1}{ #1} }
  \newcommand \lgrow  [2] { \rlap {#2} { \kern{#1} } }
  \newcommand \lgrowp [2] { \rlap {#2} {   \hp{#1} } }
  \newcommand \rgrow  [2] { { \kern{#1} } \llap {#2} }
  \newcommand \rgrowp [2] { {   \hp{#1} } \llap {#2} }
  \newcommand \cgrow  [2] { {\tiny\Kern{#1}} \llap { \rlap {#2} { \hp{\tiny {#2}} } } {\tiny\Kern{#1}} }
  \newcommand \cgrowp [2] {   \hp{\tiny{#1}} \llap { \rlap {#2} { \hp{\tiny {#2}} } }   \hp{\tiny{#1}} }
  \newcommand \cem [2] { \cgrow{#1em}{#2} }
  \newcommand \ng [2] { \overline{\vp{#1}{#2}} }
  \newcommand \c  [1] { \cancel      {#1} }
  \newcommand \ct [2] { \cancelto{#2}{#1} }
  \newcommand  \drv [2] {  \frac {\d #1} {\d #2} }
  \newcommand \tdrv [2] { \tfrac {\d #1} {\d #2} }
  \newcommand \ddrv [2] { \dfrac {\d #1} {\d #2} }
  \newcommand  \part [2] {  \frac {\partial #1} {\partial #2} }
  \newcommand \tpart [2] { \tfrac {\partial #1} {\partial #2} }
  \newcommand \dpart [2] { \dfrac {\partial #1} {\partial #2} }
  \newcommand \d  { ~\mathsf{d} }
  \newcommand \ds { \d s }
  \newcommand \dt { \d t }
  \newcommand \du { \d u }
  \newcommand \dv { \d v }
  \newcommand \dx { \d x }
  \newcommand \dy { \d y }
  \newcommand \O  { \text{O} }
\]

# Test Bed

\[
  \begin{aligned}
    & \tiny \kern{10mm} {n({n^2 \over 2} + 1) \over 2} \\[-1em]
    & \text{some stuff} \cgrow{6em}{{n({n^2 \over 2} + 1) \over 2}} \ng|{ay} ~\text{some more stuff} \\[1em]
    & \tiny abcabc \\[-1em]
    & abcabc \\[1em]
  \end{aligned}
\]

\[
  \begin{aligned}
    & \tiny {n({n^2 \over 2} + 1) \over 2} \h3 \\
    & \text{some stuff} \cgrow{6em}{{n(n + 1) \over 2}} \text{some more stuff} \bigg(\frac{1}{2} \h7 \bigg) \\
    & \text{some stuff} \cgrow{6em}{{n(n + 1) \over 2}} \text{some more stuff} \bigg(\frac{1}{2} \H9 \bigg) \\
    & \tiny abcabc \\
    & abcabc \\
  \end{aligned}
\]
