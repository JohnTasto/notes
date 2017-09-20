# Init

\[
  \rlap{\phantom{\require{enclose}}}
  \rlap{\phantom{\require{cancel}}}
\]

<!-- Because \kern does not scale AT ALL with \tiny, adding \kern, '\,', '\:', or '\;' in front of cgroup  -->
<!-- contents will appear to have no effect. Theses spaces inside \tiny{\phantom} grow at the same rate as -->
<!-- the contents, rather than at the half rate of everything else. '~', \phantom, and \Space still work,  -->
<!-- the latter of which is used to make a replacement \Kern that does scale.                              -->
<!-- Defining both \dev\|... and \def\||... causes \| not to work for some reason! -->
<!-- \def\/#1/#2/{\frac{#1}{#2}}: cool idea, doesn't work so well in practice -->
\[
  \newcommand \h [1] {{ \tiny \raise 1ex \Rule{0em}{#1ex}{#1ex} }}
  \newcommand \H [1] {{ \tiny \raise 1ex \Rule{0em}{#1em}{#1em} }}
  \\
  \newcommand  \p [1] {  \phantom{#1} }
  \newcommand \hp [1] { \hphantom{#1} }
  \newcommand \vp [1] { \vphantom{#1} }
  \\
  \newcommand \Kern  [1] { \Space{ #1}{0em}{0em} }
  \newcommand \Strut [1] { \Space{0em}{ #1}{ #1} }
  \\
  \newcommand \hsmash [1] { \rlap {#1} {           } }
  \newcommand \hs [1] { \hsmash{#1} }
  \\
  \newcommand \klgrow [2] { \rlap {#2} { \kern{#1} } }
  \newcommand \plgrow [2] { \rlap {#2} {   \hp{#1} } }
  \newcommand \krgrow [2] { { \kern{#1} } \llap {#2} }
  \newcommand \prgrow [2] { {   \hp{#1} } \llap {#2} }
  \newcommand \kcgrow [2] { {\tiny\Kern{#1}} \llap { \rlap {#2} { \hp{\tiny {#2}} } } {\tiny\Kern{#1}} }
  \newcommand \pcgrow [2] {   \hp{\tiny{#1}} \llap { \rlap {#2} { \hp{\tiny {#2}} } }   \hp{\tiny{#1}} }
  \newcommand \kc [2] { \kcgrow{#1}{#2} }
  \newcommand \pc [2] { \pcgrow{#1}{#2} }
  \\
  \newcommand \vc [1] { \vcenter{#1} }
  \\
  \newcommand \cem [2] { \kcgrow{#1em}{#2} }
  \\
  \newcommand \heading [2] [0em] { \moveleft #1 \hsmash{ \text{#2} } }
  \\
  \newcommand \grouplabel [3] [0em] { \smash{\lower1ex\lower#1\raise#2{#3}} }
  \newcommand \grouptext  [3] [0em] { \grouplabel[#1]{#2}{                               \text{#3} } }
  \newcommand \groupbrace [3] [0em] { \grouplabel[#1]{#2}{ \left. \raise.5ex{\Strut{#2}} \right#3  } }
  \newcommand \glabel [3] [0em] { \grouplabel[#1]{#2}{#3} }
  \newcommand \gtext  [3] [0em] { \grouptext [#1]{#2}{#3} }
  \newcommand \gbrace [3] [0em] { \groupbrace[#1]{#2}{#3} }
  \\
  \\
  \newcommand  \rt [3] [] { \sqrt[#1] {\vphantom{#2}\pcgrow{#2}{#3}} }
  \newcommand \hrt [3] [] { \sqrt[#1] {             \pcgrow{#2}{#3}} }
  \newcommand \vrt [3] [] { \sqrt[#1] {\vphantom{#2}           {#3}} }
  \\
  \\
  \def\(#1){\left(#1\right)}
  \def\[#1]{\left[#1\right]}
  \def\<#1>{\left<#1\right>}
  \\
  \\
  \newcommand \d [1] [] { ~\mathsf{d} #1 }
  \newcommand \ds { \d s }
  \newcommand \dt { \d t }
  \newcommand \du { \d u }
  \newcommand \dv { \d v }
  \newcommand \dx { \d x }
  \newcommand \dy { \d y }
  \\
  \newcommand  \drv [2] [] {  \frac {\d #1} {\d #2} }
  \newcommand \tdrv [2] [] { \tfrac {\d #1} {\d #2} }
  \newcommand \ddrv [2] [] { \dfrac {\d #1} {\d #2} }
  \\
  \newcommand  \part [2] [] {  \frac {\partial #1} {\partial #2} }
  \newcommand \tpart [2] [] { \tfrac {\partial #1} {\partial #2} }
  \newcommand \dpart [2] [] { \dfrac {\partial #1} {\partial #2} }
  \\
  \\
  \newcommand \/ { \over }
  \newcommand \tf [2] { \tfrac{#1}{#2} }
  \newcommand \df [2] { \dfrac{#1}{#2} }
  \\
  \\
  \newcommand \c  [1] { \cancel      {#1} }
  \newcommand \ct [2] { \cancelto{#2}{#1} }
  \\
  \newcommand \ng [2] { \overline{\vp{#1}{#2}} }
  \\
  \newcommand \O { \text{O} }
  \newcommand \? { \stackrel{?}{=} }
  \newcommand \qed { \blacksquare }
  \\
  \\
  \newcommand \rd [1] { \color{##FF3610}{#1} }
  \newcommand \or [1] { \color{##FF8c00}{#1} }
  \newcommand \yl [1] { \color{##dFC700}{#1} }
  \newcommand \gr [1] { \color{##65CD32}{#1} }
  \newcommand \cy [1] { \color{##20B2AA}{#1} }
  \newcommand \bl [1] { \color{##548CED}{#1} }
  \newcommand \pr [1] { \color{##7B68EE}{#1} }
  \newcommand \br [1] { \color{##964C20}{#1} }
  \newcommand \sl [1] { \color{##778899}{#1} }
\]

# Examples

`\pcgrow` (phantom center grow):
\[
  \text{Some aligned stuff, }\text{some replaceable stuff, }\text{some more aligned stuff} \\
  \text{Some aligned stuff, }
  \pcgrow{\text{some replaceable stuff, }}{\text{centered replacement, }}
  \text{some more aligned stuff} \\
\]

`\heading`, `\hsmash`:
\[
  \begin{aligned}
    \heading[2em]{Headings don't affect &s} \\
    y &= \hsmash{\text{Some long equation that doesn't affect &s}} \\
      &= x^2 + 2 & \leftarrow \text{an & is right there}
  \end{aligned}
\]

`\groupbrace`, `grouptext`, `grouplabel`:
\[
  \begin{aligned} \\
                 x &= y^2              && \text{normal text} \\
      \text{gizmo} &= \text{doohickey} \\
    \text{whatsit} &= \text{whatwhatg} \\
        \text{now} &= \text{later}     &
    \groupbrace{1.8em}{\}~} & \grouptext{1.8em}{group text} \\
  \end{aligned} \kern{4em}
  \begin{aligned} \\
                 x &= y^2              && \text{normal text} \\
      \text{gizmo} &= \text{doohickey} \\
    \text{whatsit} &= \text{whatwhatg} \\
        \text{now} &= \text{later}     &
    \groupbrace{1.8em}{\}~} & \grouplabel{1.8em}{\!\begin{aligned}
      & \text{arbitrary}   \\
      & \text{group label} \\
    \end{aligned}} \\
  \end{aligned} \\
\]

`\rt`, `\hrt`, `\vrt`:
\[
  \sqrt[n]{ab} = \vrt[n]{b}{a} \cdot \hrt[n]{a}{b}
\]

`\()`,`\[]`,`\<>`:
\[
  \(\[\<5 \/ 3>])
\]

`\drv`, `\part`, `\d`:
\[
  \drv{x} x^2,
  \part{x} xy^2,
  \int x^2 \dx
\]

`\/`, `\tf`, `\df`:
\[
  {5 \/ 3}
  \tf53
  \df53
\]

`\c`, `\ct`:
\[
  5\c{(1)} + \ct{1 - 1}{0}
\]

`\ng`:
\[
  \ng|{A \cup B} = \ng|A \cap \ng|B \h3
\]

`\O`, `\?`, `\qed`:
\[
  \O, \?, \qed
\]

<!-- Colors based on OrangeRed, DarkOrange, Gold, YellowGreen/LimeGreen, LightSeaGreen, CornflowerBlue,    -->
<!-- MediumSlateBlue, Sienna/SaddleBrown, and LightSlateGray.                                              -->
colors:
\[
  \rd{\text{rd}}~
  \or{\text{or}}~
  \yl{\text{yl}}~
  \gr{\text{gr}}~
  \cy{\text{cy}}~
  \bl{\text{bl}}~
  \pr{\text{pr}}~
  \br{\text{br}}~
  \sl{\text{sl}}~
\]
