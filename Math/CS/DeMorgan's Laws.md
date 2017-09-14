# DeMorgan's Laws

Set theory & boolean algebra:
\[
  \begin{aligned}
  \ng|{A \cup B} = \ng|A \cap \ng|B \h3 \\
  \ng|{A \cap B} = \ng|A \cup \ng|B \h3 \\
\end{aligned}
\]

Formal language:
\[
\begin{aligned}
  \neg (P \land Q) \iff (\neg P) \lor  (\neg Q) \h3 \\
  \neg (P \lor  Q) \iff (\neg P) \land (\neg Q) \h3 \\
\end{aligned}
\]

Electrical & computer engineering:
\[
  \begin{aligned}
  \ng|{A \cgrowp{{}+{}}{\cdot} B} &\equiv \ng|A + \ng|B \h3 \\
  \ng|{A + B} &\equiv \ng|A \cgrowp{{}+{}}{\cdot} \ng|B \h3 \\
\end{aligned}
\]

Equivalent:

\[
  \begin{array}{ccccccc}
    \times & \cap & \land & \text{and} & \text{conjunction} & \text{product} & \text{intersection} \h3 \\
    \hline
    +      & \cup & \lor  & \text{or}  & \text{disjunction} & \text{sum}     & \text{union}        \h3 \\
  \end{array}
\]
