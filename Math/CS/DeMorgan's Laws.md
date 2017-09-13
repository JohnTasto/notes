# DeMorgan's Laws

Set theory & boolean algebra:
\[
  \begin{aligned}
  \overline{A \cup B} = \overline{A} \cap \overline{B} \h3 \\
  \overline{A \cap B} = \overline{A} \cup \overline{B} \h3 \\
\end{aligned}
\]

Formal language:
\[
\begin{aligned}
  \neg (P \wedge Q) \iff (\neg P) \vee   (\neg Q) \h3 \\
  \neg (P \vee   Q) \iff (\neg P) \wedge (\neg Q) \h3 \\
\end{aligned}
\]

Electrical & computer engineering:
\[
  \begin{aligned}
  \overline{A \cgrowp{{}+{}}{\cdot} B} &\equiv \overline{A} + \overline{B} \h3 \\
  \overline{A + B} &\equiv \overline{A} \cgrowp{{}+{}}{\cdot} \overline{B} \h3 \\
\end{aligned}
\]

Equivalent:

\[
  \begin{array}{ccccccc}
    \times & \cap & \wedge & \text{and} & \text{conjunction} & \text{product} & \text{intersection} \h3 \\
    \hline
    +      & \cup & \vee   & \text{or}  & \text{disjunction} & \text{sum}     & \text{union}        \h3 \\
  \end{array}
\]
