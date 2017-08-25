# DeMorgan's Laws

Set theory & boolean algebra:
\[
  \begin{aligned}
  \overline{A \cup B} = \overline{A} \cap \overline{B} \\
  \overline{A \cap B} = \overline{A} \cup \overline{B} \\
\end{aligned}
\]

Formal language:
\[
\begin{aligned}
  \neg (P \wedge Q) \Longleftrightarrow (\neg P) \vee (\neg Q) \\
  \neg (P \vee Q) \Longleftrightarrow (\neg P) \wedge (\neg Q) \\
\end{aligned}
\]

Electrical & computer engineering:
\[
  \begin{aligned}
  \overline{A \cdot B} &\equiv \overline{A} + \overline{B} \\
  \overline{A + B} &\equiv \overline{A} \cdot \overline{B} \\
\end{aligned}
\]

Equivalent:

|                  |        |          |     |             |         |              |
| ---------------- | ------ | -------- | --- | ----------- | ------- | ------------ |
| $\times$ $\cdot$ | $\cap$ | $\wedge$ | and | conjunction | product | intersection |
| $+$              | $\cup$ | $\vee$   | or  | disjunction | sum     | union        |
