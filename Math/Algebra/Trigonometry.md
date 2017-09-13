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
        0°     &       0      &   0    &   1    &   0    &   -    &   1    &   -    \BG \\
       30°     & \dfrac{π}{6} &  \aob  & \rcob  & \rcoc  &   2    & \brcoc &  \rc   \BG \\
       45°     & \dfrac{π}{4} & \rbob  & \rbob  &   1    &  \rb   &  \rb   &   1    \BG \\
       60°     & \dfrac{π}{3} & \rcob  &  \aob  &  \rc   & \brcoc &   2    & \rcoc  \BG \\
       90°     & \dfrac{π}{2} &   1    &   0    &   -    &   1    &   -    &   0    \BG \\
  \end{array}
\]

## Radians to Degrees

\[
  \begin{array}{rcrcrcrc}
      0° =& \kern{-.75em}          0     &
     90° =& \kern{-.75em} \dfrac{  π}{2} &
    180° =& \kern{-.75em}          π     &
    270° =& \kern{-.75em} \dfrac{ 3π}{2} \BG \\
     30° =& \kern{-.75em} \dfrac{  π}{6} &
    120° =& \kern{-.75em} \dfrac{ 2π}{3} &
    210° =& \kern{-.75em} \dfrac{ 7π}{6} &
    300° =& \kern{-.75em} \dfrac{ 5π}{3} \BG \\
     45° =& \kern{-.75em} \dfrac{  π}{4} &
    135° =& \kern{-.75em} \dfrac{ 3π}{4} &
    225° =& \kern{-.75em} \dfrac{ 5π}{4} &
    315° =& \kern{-.75em} \dfrac{ 7π}{4} \BG \\
     60° =& \kern{-.75em} \dfrac{  π}{3} &
    150° =& \kern{-.75em} \dfrac{ 5π}{6} &
    240° =& \kern{-.75em} \dfrac{ 4π}{3} &
    330° =& \kern{-.75em} \dfrac{11π}{6} \BG \\
     90° =& \kern{-.75em} \dfrac{  π}{2} &
  ~~180° =& \kern{-.75em}          π     &
  ~~270° =& \kern{-.75em} \dfrac{ 3π}{2} &
  ~~360° =& \kern{-.75em}         2π     \BG \\
  \end{array}
\]

## Definitions

### SOHCAHTOA

\[
  \begin{aligned}
    \sin θ &=   {\text{opposite} \over \text{hypotenuse}} = y          &
    \csc θ &= {\text{hypotenuse} \over \text{opposite}} \BG \\
    \cos θ &=   {\text{adjacent} \over \text{hypotenuse}} = x          &
    \sec θ &= {\text{hypotenuse} \over \text{adjacent}} \BG \\
    \tan θ &=   {\text{opposite} \over \text{adjacent}} = \text{slope} &
    \cot θ &=   {\text{adjacent} \over \text{opposite}} \BG \\
  \end{aligned}
\]

### Circle

\[
  \begin{aligned}
    \sin θ &= {y \over r}  &  \csc θ &= {r \over y} \BG \\
    \cos θ &= {x \over r}  &  \sec θ &= {r \over x} \BG \\
    \tan θ &= {y \over x}  &  \cot θ &= {x \over y} \BG \\
  \end{aligned}
\]

## Identities

### Pythagorean

\[
  \begin{aligned}
    \sin^2 θ + \cos^2 θ &= 1 \Bg \\
    \tan^2 θ + 1 &= \sec^2 θ \Bg \\
    \cot^2 θ + 1 &= \csc^2 θ \Bg \\
  \end{aligned}
\]

### Reciprocal

\[
  \begin{aligned}
    \sin x &= {1 \over \csc x}  &  \csc x &= {1 \over \sin x} \BG \\
    \cos x &= {1 \over \sec x}  &  \sec x &= {1 \over \cos x} \BG \\
    \tan x &= {1 \over \cot x}  &  \cot x &= {1 \over \tan x} \BG \\
  \end{aligned}
\]

### Quotient

\[
  \begin{aligned}
    \sin x &= {\tan x \over \sec x}  &  \csc x &= {\cot x \over \cos x} \BG \\
    \cos x &= {\cot x \over \csc x}  &  \sec x &= {\tan x \over \sin x} \BG \\
    \tan x &= {\sin x \over \cos x}  &  \cot x &= {\cos x \over \sin x} \BG \\
  \end{aligned}
\]

### Cofunction

The value of a trig function of an angle equals the value of the cofunction of the complement of the angle.

\[
  \begin{aligned}
    \sin \Big({π \over 2} - x \Big) &= \cos x & \cos \Big({π \over 2} - x \Big) &= \sin x \BG \\
    \tan \Big({π \over 2} - x \Big) &= \cot x & \cot \Big({π \over 2} - x \Big) &= \tan x \BG \\
    \sec \Big({π \over 2} - x \Big) &= \csc x & \csc \Big({π \over 2} - x \Big) &= \sec x \BG \\
  \end{aligned}
\]

### Symmetries

#### Even/Odd

\[
  \begin{aligned}
    \sin(-x) &=    - \sin x & \csc(-x) &=    - \csc x && \text{Odd}  \Bg \\
    \cos(-x) &= \p{-}\cos x & \sec(-x) &= \p{-}\sec x && \text{Even} \Bg \\
    \tan(-x) &=    - \tan x & \cot(-x) &=    - \cot x && \text{Odd}  \Bg \\
  \end{aligned}
\]

#### Periodicity

\[
  \begin{aligned}
    \sin(x +    2 π) &= \sin x & \csc(x +    2 π) = \csc x \Bg \\
    \cos(x +    2 π) &= \cos x & \sec(x +    2 π) = \sec x \Bg \\
    \tan(x + \p{2}π) &= \tan x & \cot(x + \p{2}π) = \cot x \Bg \\
  \end{aligned}
\]

### Sum/Difference

\[
  \begin{aligned}
    \sin(x + y) &= \sin x \cos y + \cos x \sin y \Bg \\
    \sin(x - y) &= \sin x \cos y - \cos x \sin y \Bg \\[1em]
    \cos(x + y) &= \cos x \cos y - \sin x \sin y \Bg \\
    \cos(x - y) &= \cos x \cos y + \sin x \sin y \Bg \\[1em]
    \tan(x + y) &= {\tan x + \tan y \over 1 - \tan x \tan y} \BG \\
    \tan(x - y) &= {\tan x - \tan y \over 1 + \tan x \tan y} \BG \\
  \end{aligned}
\]

### Half Angle

\[
  \begin{aligned}
    \sin{x \over 2} &= \pm \sqrt{{1 - \cos x \over 2}}          \BG \\
    \cos{x \over 2} &= \pm \sqrt{{1 + \cos x \over 2}}          \BG \\
    \tan{x \over 2} &= \pm \sqrt{{1 - \cos x \over 1 + \cos x}} \BG \\
                    &= {\sin x \over 1 + \cos x}                \BG \\
                    &= {1 - \cos x \over \sin x}                \BG \\
  \end{aligned}
\]

### Double Angle

\[
  \begin{aligned}
    \sin 2x &= 2 \sin x \cos x               \Bg \\[1em]
    \cos 2x &= \cos^2 x - \sin^2 x           \Bg \\
            &= 1 - 2 \sin^2 x                \Bg \\
            &= 2 \cos^2 x - 1                \Bg \\[1em]
    \tan 2x &= {2 \tan x \over 1 - \tan^2 x} \BG \\
  \end{aligned}
\]

### Triple Angle

\[
  \begin{aligned}
    \sin 3x &=  \p{-}3 \sin x - 4 \sin^3 x                       \Bg \\
    \cos 3x &=     - 3 \cos x + 4 \cos^3 x                       \Bg \\
    \tan 3x &= \p{-}{3 \tan x -   \tan^3 x \over 1 - 3 \tan^2 x} \BG \\
  \end{aligned}
\]

### Product to Sum

\[
  \begin{aligned}
    \cos x \cos y &= \tfrac12 ~[~     \cos(x - y) +     \cos(x + y) ~] \Bg \\
    \sin x \sin y &= \tfrac12 ~[~     \cos(x - y) -     \cos(x + y) ~] \Bg \\
    \sin x \cos y &= \tfrac12 ~[~ \;\!\sin(x - y) + \;\!\sin(x + y) ~] \Bg \\
  \end{aligned}
\]

### Sum to Product

\[
  \begin{aligned}
    \sin x + \sin y &= \p{-}2 \sin \Big({x + y \over 2} \Big) \cos \Big( {x - y \over 2} \Big) \BG \\
    \sin x - \sin y &= \p{-}2 \cos \Big({x + y \over 2} \Big) \sin \Big( {x - y \over 2} \Big) \BG \\
    \cos x + \cos y &= \p{-}2 \cos \Big({x + y \over 2} \Big) \cos \Big( {x - y \over 2} \Big) \BG \\
    \cos x - \cos y &=    - 2 \sin \Big({x + y \over 2} \Big) \sin \Big( {x - y \over 2} \Big) \BG \\
  \end{aligned}
\]

### Square to Linear

\[
  \begin{aligned}
    \sin^2 x = {1 - \cos 2x \over 2}           \BG \\
    \cos^2 x = {1 + \cos 2x \over 2}           \BG \\
    \tan^2 x = {1 - \cos 2x \over 1 + \cos 2x} \BG \\
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
    a^2 &= b^2 + c^2 - 2bc\cos A \Bg \\
    b^2 &= c^2 + a^2 - 2ca\cos B \Bg \\
    c^2 &= a^2 + b^2 - 2ab\cos C \Bg \\
  \end{aligned}
\]

### Area of a Triangle

\[
  \begin{aligned}
    \text{Given} & \Bg \\
               s &= {a + b + c \over 2} = \text{semiperimeter,} \BG \\
               l &= \text{length of side of equilateral triangle,} \Bg \\
               r &= \text{inradius,} \Bg \\
               R &= \text{radius of circumcircle,} \Bg \\[2em]
     \text{Area} &= \tfrac12bh \BG \\
                 &= \tfrac12ab \sin C = \tfrac12bc \sin A = \tfrac12ca \sin B \Bg \\
                 &= \sqrt{s(s - a)(s - b)(s - c)} && \text{Heron's Formula} \BG \\
                 &= rs \Bg \\
                 &= {abc \over 4R} \BG \\
  \end{aligned}
\]

