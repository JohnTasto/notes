# Trigonometry

## Values

\[
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
        0°     &       0      &   0    &   1    &   0    &   -    &   1    &   -    \h7 \\
       30°     & \dfrac{π}{6} &  \aob  & \rcob  & \rcoc  &   2    & \brcoc &  \rc   \h7 \\
       45°     & \dfrac{π}{4} & \rbob  & \rbob  &   1    &  \rb   &  \rb   &   1    \h7 \\
       60°     & \dfrac{π}{3} & \rcob  &  \aob  &  \rc   & \brcoc &   2    & \rcoc  \h7 \\
       90°     & \dfrac{π}{2} &   1    &   0    &   -    &   1    &   -    &   0    \h7 \\
  \end{array}
\]

## Radians to Degrees

\[
  \begin{array}{rcrcrcrc}
      0° =& \kern{-.75em}          0     &
     90° =& \kern{-.75em} \dfrac{  π}{2} &
    180° =& \kern{-.75em}          π     &
    270° =& \kern{-.75em} \dfrac{ 3π}{2} \h7 \\
     30° =& \kern{-.75em} \dfrac{  π}{6} &
    120° =& \kern{-.75em} \dfrac{ 2π}{3} &
    210° =& \kern{-.75em} \dfrac{ 7π}{6} &
    300° =& \kern{-.75em} \dfrac{ 5π}{3} \h7 \\
     45° =& \kern{-.75em} \dfrac{  π}{4} &
    135° =& \kern{-.75em} \dfrac{ 3π}{4} &
    225° =& \kern{-.75em} \dfrac{ 5π}{4} &
    315° =& \kern{-.75em} \dfrac{ 7π}{4} \h7 \\
     60° =& \kern{-.75em} \dfrac{  π}{3} &
    150° =& \kern{-.75em} \dfrac{ 5π}{6} &
    240° =& \kern{-.75em} \dfrac{ 4π}{3} &
    330° =& \kern{-.75em} \dfrac{11π}{6} \h7 \\
     90° =& \kern{-.75em} \dfrac{  π}{2} &
  ~~180° =& \kern{-.75em}          π     &
  ~~270° =& \kern{-.75em} \dfrac{ 3π}{2} &
  ~~360° =& \kern{-.75em}         2π     \h7 \\
  \end{array}
\]

## Definitions

### SOHCAHTOA

\[
  \begin{aligned}
    \sin θ &=   {\text{opposite} \over \text{hypotenuse}} = y          &
    \csc θ &= {\text{hypotenuse} \over \text{opposite}} \h7 \\
    \cos θ &=   {\text{adjacent} \over \text{hypotenuse}} = x          &
    \sec θ &= {\text{hypotenuse} \over \text{adjacent}} \h7 \\
    \tan θ &=   {\text{opposite} \over \text{adjacent}} = \text{slope} &
    \cot θ &=   {\text{adjacent} \over \text{opposite}} \h7 \\
  \end{aligned}
\]

### Circle

\[
  \begin{aligned}
    \sin θ &= {y \over r}  &  \csc θ &= {r \over y} \h7 \\
    \cos θ &= {x \over r}  &  \sec θ &= {r \over x} \h7 \\
    \tan θ &= {y \over x}  &  \cot θ &= {x \over y} \h7 \\
  \end{aligned}
\]

## Identities

### Pythagorean

\[
  \begin{aligned}
    \sin^2 θ + \cos^2 θ &= 1 \h4 \\
    \tan^2 θ + 1 &= \sec^2 θ \h4 \\
    \cot^2 θ + 1 &= \csc^2 θ \h4 \\
  \end{aligned}
\]

### Reciprocal

\[
  \begin{aligned}
    \sin x &= {1 \over \csc x}  &  \csc x &= {1 \over \sin x} \h7 \\
    \cos x &= {1 \over \sec x}  &  \sec x &= {1 \over \cos x} \h7 \\
    \tan x &= {1 \over \cot x}  &  \cot x &= {1 \over \tan x} \h7 \\
  \end{aligned}
\]

### Quotient

\[
  \begin{aligned}
    \sin x &= {\tan x \over \sec x}  &  \csc x &= {\cot x \over \cos x} \h7 \\
    \cos x &= {\cot x \over \csc x}  &  \sec x &= {\tan x \over \sin x} \h7 \\
    \tan x &= {\sin x \over \cos x}  &  \cot x &= {\cos x \over \sin x} \h7 \\
  \end{aligned}
\]

### Cofunction

The value of a trig function of an angle equals the value of the cofunction of the complement of the angle.

\[
  \begin{aligned}
    \sin \Big({π \over 2} - x \Big) &= \cos x & \cos \Big({π \over 2} - x \Big) &= \sin x \h7 \\
    \tan \Big({π \over 2} - x \Big) &= \cot x & \cot \Big({π \over 2} - x \Big) &= \tan x \h7 \\
    \sec \Big({π \over 2} - x \Big) &= \csc x & \csc \Big({π \over 2} - x \Big) &= \sec x \h7 \\
  \end{aligned}
\]

### Symmetries

#### Even/Odd

\[
  \begin{aligned}
    \sin(-x) &=    - \sin x & \csc(-x) &=    - \csc x && \text{Odd}  \h4 \\
    \cos(-x) &= \p{-}\cos x & \sec(-x) &= \p{-}\sec x && \text{Even} \h4 \\
    \tan(-x) &=    - \tan x & \cot(-x) &=    - \cot x && \text{Odd}  \h4 \\
  \end{aligned}
\]

#### Periodicity

\[
  \begin{aligned}
    \sin(x +    2 π) &= \sin x & \csc(x +    2 π) = \csc x \h4 \\
    \cos(x +    2 π) &= \cos x & \sec(x +    2 π) = \sec x \h4 \\
    \tan(x + \p{2}π) &= \tan x & \cot(x + \p{2}π) = \cot x \h4 \\
  \end{aligned}
\]

### Sum/Difference

\[
  \begin{aligned}
    \sin(x + y) &= \sin x \cos y + \cos x \sin y \h4 \\
    \sin(x - y) &= \sin x \cos y - \cos x \sin y \h4 \\[1em]
    \cos(x + y) &= \cos x \cos y - \sin x \sin y \h4 \\
    \cos(x - y) &= \cos x \cos y + \sin x \sin y \h4 \\[1em]
    \tan(x + y) &= {\tan x + \tan y \over 1 - \tan x \tan y} \h7 \\
    \tan(x - y) &= {\tan x - \tan y \over 1 + \tan x \tan y} \h7 \\
  \end{aligned}
\]

### Half Angle

\[
  \begin{aligned}
    \sin{x \over 2} &= \pm \sqrt{{1 - \cos x \over 2}}          \h7 \\
    \cos{x \over 2} &= \pm \sqrt{{1 + \cos x \over 2}}          \h7 \\
    \tan{x \over 2} &= \pm \sqrt{{1 - \cos x \over 1 + \cos x}} \h7 \\
                    &= {\sin x \over 1 + \cos x}                \h7 \\
                    &= {1 - \cos x \over \sin x}                \h7 \\
  \end{aligned}
\]

### Double Angle

\[
  \begin{aligned}
    \sin 2x &= 2 \sin x \cos x               \h4 \\[1em]
    \cos 2x &= \cos^2 x - \sin^2 x           \h4 \\
            &= 1 - 2 \sin^2 x                \h4 \\
            &= 2 \cos^2 x - 1                \h4 \\[1em]
    \tan 2x &= {2 \tan x \over 1 - \tan^2 x} \h7 \\
  \end{aligned}
\]

### Triple Angle

\[
  \begin{aligned}
    \sin 3x &=  \p{-}3 \sin x - 4 \sin^3 x                       \h4 \\
    \cos 3x &=     - 3 \cos x + 4 \cos^3 x                       \h4 \\
    \tan 3x &= \p{-}{3 \tan x -   \tan^3 x \over 1 - 3 \tan^2 x} \h7 \\
  \end{aligned}
\]

### Product to Sum

\[
  \begin{aligned}
    \cos x \cos y &= \tfrac12 ~[~     \cos(x - y) +     \cos(x + y) ~] \h4 \\
    \sin x \sin y &= \tfrac12 ~[~     \cos(x - y) -     \cos(x + y) ~] \h4 \\
    \sin x \cos y &= \tfrac12 ~[~ \;\!\sin(x - y) + \;\!\sin(x + y) ~] \h4 \\
  \end{aligned}
\]

### Sum to Product

\[
  \begin{aligned}
    \sin x + \sin y &= \p{-}2 \sin \Big({x + y \over 2} \Big) \cos \Big( {x - y \over 2} \Big) \h7 \\
    \sin x - \sin y &= \p{-}2 \cos \Big({x + y \over 2} \Big) \sin \Big( {x - y \over 2} \Big) \h7 \\
    \cos x + \cos y &= \p{-}2 \cos \Big({x + y \over 2} \Big) \cos \Big( {x - y \over 2} \Big) \h7 \\
    \cos x - \cos y &=    - 2 \sin \Big({x + y \over 2} \Big) \sin \Big( {x - y \over 2} \Big) \h7 \\
  \end{aligned}
\]

### Square to Linear

\[
  \begin{aligned}
    \sin^2 x = {1 - \cos 2x \over 2}           \h7 \\
    \cos^2 x = {1 + \cos 2x \over 2}           \h7 \\
    \tan^2 x = {1 - \cos 2x \over 1 + \cos 2x} \h7 \\
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
    a^2 &= b^2 + c^2 - 2bc\cos A \h4 \\
    b^2 &= c^2 + a^2 - 2ca\cos B \h4 \\
    c^2 &= a^2 + b^2 - 2ab\cos C \h4 \\
  \end{aligned}
\]

### Area of a Triangle

\[
  \begin{aligned}
    \text{Given} & \h4 \\
               s &= {a + b + c \over 2} = \text{semiperimeter,} \h7 \\
               l &= \text{length of side of equilateral triangle,} \h4 \\
               r &= \text{inradius,} \h4 \\
               R &= \text{radius of circumcircle,} \h4 \\[2em]
     \text{Area} &= \tfrac12bh \h7 \\
                 &= \tfrac12ab \sin C = \tfrac12bc \sin A = \tfrac12ca \sin B \h4 \\
                 &= \sqrt{s(s - a)(s - b)(s - c)} && \text{Heron's Formula} \h7 \\
                 &= rs \h4 \\
                 &= {abc \over 4R} \h7 \\
  \end{aligned}
\]

