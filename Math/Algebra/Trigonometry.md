# Trigonometry

## Values

\[
  \newcommand\bs{\vpppp}
  \newcommand\ls{\vpp}
  \newcommand\rbob {\dfrac{ \sqrt{2}}{2}}
  \newcommand\rcob {\dfrac{ \sqrt{3}}{2}}
  \newcommand\rb   {        \sqrt{2}    }
  \newcommand\rc   {        \sqrt{3}    }
  \newcommand\rcoc {\dfrac{ \sqrt{3}}{3}}
  \newcommand\brcoc{\dfrac{2\sqrt{3}}{3}}
  \newcommand\aob  {\dfrac       {1} {2}}
  \begin{array}{cc|cccccc}
    \text{deg} &  \text{rad}  & \sin θ & \cos θ & \tan θ & \csc θ & \sec θ & \cot θ     \\[-1em]
      \qquad   &    \qquad    & \qquad & \qquad & \qquad & \qquad & \qquad & \qquad     \\[-1em]
        0°     &       0      &   0    &   1    &   0    &   -    &   1    &   -    \bs \\
       30°     & \dfrac{π}{6} &  \aob  & \rcob  & \rcoc  &   2    & \brcoc &  \rc   \bs \\
       45°     & \dfrac{π}{4} & \rbob  & \rbob  &   1    &  \rb   &  \rb   &   1    \bs \\
       60°     & \dfrac{π}{3} & \rcob  &  \aob  &  \rc   & \brcoc &   2    & \rcoc  \bs \\
       90°     & \dfrac{π}{2} &   1    &   0    &   -    &   1    &   -    &   0    \bs \\
  \end{array}
\]

## Radians to Degrees

\[
  \begin{array}{rcrcrcrc}
      0° =& \kern{-.75em}          0     &
     90° =& \kern{-.75em} \dfrac{  π}{2} &
    180° =& \kern{-.75em}          π     &
    270° =& \kern{-.75em} \dfrac{ 3π}{2} \bs \\
     30° =& \kern{-.75em} \dfrac{  π}{6} &
    120° =& \kern{-.75em} \dfrac{ 2π}{3} &
    210° =& \kern{-.75em} \dfrac{ 7π}{6} &
    300° =& \kern{-.75em} \dfrac{ 5π}{3} \bs \\
     45° =& \kern{-.75em} \dfrac{  π}{4} &
    135° =& \kern{-.75em} \dfrac{ 3π}{4} &
    225° =& \kern{-.75em} \dfrac{ 5π}{4} &
    315° =& \kern{-.75em} \dfrac{ 7π}{4} \bs \\
     60° =& \kern{-.75em} \dfrac{  π}{3} &
    150° =& \kern{-.75em} \dfrac{ 5π}{6} &
    240° =& \kern{-.75em} \dfrac{ 4π}{3} &
    330° =& \kern{-.75em} \dfrac{11π}{6} \bs \\
     90° =& \kern{-.75em} \dfrac{  π}{2} &
  ~~180° =& \kern{-.75em}          π     &
  ~~270° =& \kern{-.75em} \dfrac{ 3π}{2} &
  ~~360° =& \kern{-.75em}         2π     \bs \\
  \end{array}
\]

## Definitions

### SOHCAHTOA

\[
  \begin{aligned}
    \sin θ &=   {\text{opposite} \over \text{hypotenuse}} = y          &
    \csc θ &= {\text{hypotenuse} \over \text{opposite}} \bs \\
    \cos θ &=   {\text{adjacent} \over \text{hypotenuse}} = x          &
    \sec θ &= {\text{hypotenuse} \over \text{adjacent}} \bs \\
    \tan θ &=   {\text{opposite} \over \text{adjacent}} = \text{slope} &
    \cot θ &=   {\text{adjacent} \over \text{opposite}} \bs \\
  \end{aligned}
\]

### Circle

\[
  \begin{aligned}
    \sin θ &= {y \over r}  &  \csc θ &= {r \over y} \bs \\
    \cos θ &= {x \over r}  &  \sec θ &= {r \over x} \bs \\
    \tan θ &= {y \over x}  &  \cot θ &= {x \over y} \bs \\
  \end{aligned}
\]

## Identities

### Pythagorean

\[
  \begin{aligned}
    \sin^2 θ + \cos^2 θ &= 1 \ls \\
    \tan^2 θ + 1 &= \sec^2 θ \ls \\
    \cot^2 θ + 1 &= \csc^2 θ \ls \\
  \end{aligned}
\]

### Reciprocal

\[
  \begin{aligned}
    \sin x &= {1 \over \csc x}  &  \csc x &= {1 \over \sin x} \bs \\
    \cos x &= {1 \over \sec x}  &  \sec x &= {1 \over \cos x} \bs \\
    \tan x &= {1 \over \cot x}  &  \cot x &= {1 \over \tan x} \bs \\
  \end{aligned}
\]

### Quotient

\[
  \begin{aligned}
    \sin x &= {\tan x \over \sec x}  &  \csc x &= {\cot x \over \cos x} \bs \\
    \cos x &= {\cot x \over \csc x}  &  \sec x &= {\tan x \over \sin x} \bs \\
    \tan x &= {\sin x \over \cos x}  &  \cot x &= {\cos x \over \sin x} \bs \\
  \end{aligned}
\]

### Cofunction

The value of a trig function of an angle equals the value of the cofunction of the complement of the angle.

\[
  \begin{aligned}
    \sin \Big({π \over 2} - x \Big) &= \cos x & \cos \Big({π \over 2} - x \Big) &= \sin x \bs \\
    \tan \Big({π \over 2} - x \Big) &= \cot x & \cot \Big({π \over 2} - x \Big) &= \tan x \bs \\
    \sec \Big({π \over 2} - x \Big) &= \csc x & \csc \Big({π \over 2} - x \Big) &= \sec x \bs \\
  \end{aligned}
\]

### Symmetries

#### Even/Odd

\[
  \begin{aligned}
    \sin(-x) &=    - \sin x & \csc(-x) &=    - \csc x && \text{Odd}  \ls \\
    \cos(-x) &= \p{-}\cos x & \sec(-x) &= \p{-}\sec x && \text{Even} \ls \\
    \tan(-x) &=    - \tan x & \cot(-x) &=    - \cot x && \text{Odd}  \ls \\
  \end{aligned}
\]

#### Periodicity

\[
  \begin{aligned}
    \sin(x +    2 π) &= \sin x & \csc(x +    2 π) = \csc x \ls \\
    \cos(x +    2 π) &= \cos x & \sec(x +    2 π) = \sec x \ls \\
    \tan(x + \p{2}π) &= \tan x & \cot(x + \p{2}π) = \cot x \ls \\
  \end{aligned}
\]

### Sum/Difference

\[
  \begin{aligned}
    \sin(x + y) &= \sin x \cos y + \cos x \sin y \ls \\
    \sin(x - y) &= \sin x \cos y - \cos x \sin y \ls \\[1em]
    \cos(x + y) &= \cos x \cos y - \sin x \sin y \ls \\
    \cos(x - y) &= \cos x \cos y + \sin x \sin y \ls \\[1em]
    \tan(x + y) &= {\tan x + \tan y \over 1 - \tan x \tan y} \bs \\
    \tan(x - y) &= {\tan x - \tan y \over 1 + \tan x \tan y} \bs \\
  \end{aligned}
\]

### Half Angle

\[
  \begin{aligned}
    \sin{x \over 2} &= \pm \sqrt{{1 - \cos x \over 2}}          \bs \\
    \cos{x \over 2} &= \pm \sqrt{{1 + \cos x \over 2}}          \bs \\
    \tan{x \over 2} &= \pm \sqrt{{1 - \cos x \over 1 + \cos x}} \bs \\
                    &= {\sin x \over 1 + \cos x}                \bs \\
                    &= {1 - \cos x \over \sin x}                \bs \\
  \end{aligned}
\]

### Double Angle

\[
  \begin{aligned}
    \sin 2x &= 2 \sin x \cos x               \ls \\[1em]
    \cos 2x &= \cos^2 x - \sin^2 x           \ls \\
            &= 1 - 2 \sin^2 x                \ls \\
            &= 2 \cos^2 x - 1                \ls \\[1em]
    \tan 2x &= {2 \tan x \over 1 - \tan^2 x} \bs \\
  \end{aligned}
\]

### Triple Angle

\[
  \begin{aligned}
    \sin 3x &=  \p{-}3 \sin x - 4 \sin^3 x                       \ls \\
    \cos 3x &=     - 3 \cos x + 4 \cos^3 x                       \ls \\
    \tan 3x &= \p{-}{3 \tan x -   \tan^3 x \over 1 - 3 \tan^2 x} \bs \\
  \end{aligned}
\]

### Product to Sum

\[
  \begin{aligned}
    \cos x \cos y &= \tfrac12 ~[~     \cos(x - y) +     \cos(x + y) ~] \ls \\
    \sin x \sin y &= \tfrac12 ~[~     \cos(x - y) -     \cos(x + y) ~] \ls \\
    \sin x \cos y &= \tfrac12 ~[~ \;\!\sin(x - y) + \;\!\sin(x + y) ~] \ls \\
  \end{aligned}
\]

### Sum to Product

\[
  \begin{aligned}
    \sin x + \sin y &= \p{-}2 \sin \Big({x + y \over 2} \Big) \cos \Big( {x - y \over 2} \Big) \bs \\
    \sin x - \sin y &= \p{-}2 \cos \Big({x + y \over 2} \Big) \sin \Big( {x - y \over 2} \Big) \bs \\
    \cos x + \cos y &= \p{-}2 \cos \Big({x + y \over 2} \Big) \cos \Big( {x - y \over 2} \Big) \bs \\
    \cos x - \cos y &=    - 2 \sin \Big({x + y \over 2} \Big) \sin \Big( {x - y \over 2} \Big) \bs \\
  \end{aligned}
\]

### Square to Linear

\[
  \begin{aligned}
    \sin^2 x = {1 - \cos 2x \over 2}           \bs \\
    \cos^2 x = {1 + \cos 2x \over 2}           \bs \\
    \tan^2 x = {1 - \cos 2x \over 1 + \cos 2x} \bs \\
  \end{aligned}
\]

## Other formulas

### Reference Triangle

```viz {engine="neato"}
graph Triangle {
  bgcolor="transparent";

	node [color=invis, shape=circle, fontcolor=grey80, fontsize=20]; A; B; C;

  edge [color=grey40, style=bold, fontcolor=grey80, fontsize=20];
  A -- B [label="c", len=4.00];
  B -- C [label="a", len=3.00];
  C -- A [label="b", len=2.00];
}
```

### Law of Sines

\[
  {\sin A \over a} = {\sin B \over b} = {\sin C \over c}
\]

### Law of Cosines

\[
  \begin{aligned}
    a^2 &= b^2 + c^2 - 2bc\cos A \ls \\
    b^2 &= c^2 + a^2 - 2ca\cos B \ls \\
    c^2 &= a^2 + b^2 - 2ab\cos C \ls \\
  \end{aligned}
\]

### Area of a Triangle

\[
  \begin{aligned}
    \text{Given} & \ls \\
               s &= {a + b + c \over 2} = \text{semiperimeter,} \bs \\
               l &= \text{length of side of equilateral triangle,} \ls \\
               r &= \text{inradius,} \ls \\
               R &= \text{radius of circumcircle,} \ls \\[2em]
     \text{Area} &= \tfrac12bh \bs \\
                 &= \tfrac12ab \sin C = \tfrac12bc \sin A = \tfrac12ca \sin B \ls \\
                 &= \sqrt{s(s - a)(s - b)(s - c)} && \text{Heron's Formula} \bs \\
                 &= rs \ls \\
                 &= {abc \over 4R} \bs \\
  \end{aligned}
\]

