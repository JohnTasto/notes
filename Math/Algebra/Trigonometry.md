# Trigonometry

## Values

\[
  \begin{array}{cc|cccccc}
    \text{deg} &   \text{rad}   &        \sin θ       &        \cos θ       &        \tan θ       &         \csc θ       &         \sec θ       &        \cot θ       \\
      \qquad   &     \qquad     &        \qquad       &        \qquad       &        \qquad       &         \qquad       &         \qquad       &        \qquad       \\
     0\degree  &        0       &          0          &          1          &          0          &           -          &           1          &          -          \\[1em]
    30\degree  &  \dfrac{π}{6}  &    \dfrac{1}{2}     & \dfrac{\sqrt{3}}{2} & \dfrac{\sqrt{3}}{3} &           2          & \dfrac{2\sqrt{3}}{3} &       \sqrt{3}      \\[1em]
    45\degree  &  \dfrac{π}{4}  & \dfrac{\sqrt{2}}{2} & \dfrac{\sqrt{2}}{2} &          1          &       \sqrt{2}       &       \sqrt{2}       &          1          \\[1em]
    60\degree  &  \dfrac{π}{3}  & \dfrac{\sqrt{3}}{2} &    \dfrac{1}{2}     &       \sqrt{3}      & \dfrac{2\sqrt{3}}{3} &           2          & \dfrac{\sqrt{3}}{3} \\[1.5em]
    90\degree  &  \dfrac{π}{2}  &          1          &          0          &          -          &           1          &           -          &          0
  \end{array}
\]

## Radians to Degrees

\[
  \begin{array}{rcrcrcrc}
      0\degree =& \kern{-.75em}         0        &
     90\degree =& \kern{-.75em} \dfrac{  π}{2} &
    180\degree =& \kern{-.75em}          π     &
    270\degree =& \kern{-.75em} \dfrac{ 3π}{2} \\[1.5em]
     30\degree =& \kern{-.75em} \dfrac{  π}{6} &
    120\degree =& \kern{-.75em} \dfrac{ 2π}{3} &
    210\degree =& \kern{-.75em} \dfrac{ 7π}{6} &
    300\degree =& \kern{-.75em} \dfrac{ 5π}{3} \\[1.5em]
     45\degree =& \kern{-.75em} \dfrac{  π}{4} &
    135\degree =& \kern{-.75em} \dfrac{ 3π}{4} &
    225\degree =& \kern{-.75em} \dfrac{ 5π}{4} &
    315\degree =& \kern{-.75em} \dfrac{ 7π}{4} \\[1.5em]
     60\degree =& \kern{-.75em} \dfrac{  π}{3} &
    150\degree =& \kern{-.75em} \dfrac{ 5π}{6} &
    240\degree =& \kern{-.75em} \dfrac{ 4π}{3} &
    330\degree =& \kern{-.75em} \dfrac{11π}{6} \\[1.5em]
     90\degree =& \kern{-.75em} \dfrac{  π}{2} &
  ~~180\degree =& \kern{-.75em}          π     &
  ~~270\degree =& \kern{-.75em} \dfrac{ 3π}{2} &
  ~~360\degree =& \kern{-.75em}         2π
  \end{array}
\]

## Definitions

### SOHCAHTOA

\[
  \begin{aligned}
    \sin θ &=   \frac{\text{opposite}}{\text{hypotenuse}} = y          &
    \csc θ &= \frac{\text{hypotenuse}}{\text{opposite}}                \\[1.5em]
    \cos θ &=   \frac{\text{adjacent}}{\text{hypotenuse}} = x          &
    \sec θ &= \frac{\text{hypotenuse}}{\text{adjacent}}                \\[1.5em]
    \tan θ &=   \frac{\text{opposite}}{\text{adjacent}} = \text{slope} &
    \cot θ &=   \frac{\text{adjacent}}{\text{opposite}}
  \end{aligned}
\]

### Circle

\[
  \begin{matrix}
    \sin θ = \dfrac{y}{r} & \csc θ = \dfrac{r}{y} \\[1.5em]
    \cos θ = \dfrac{x}{r} & \sec θ = \dfrac{r}{x} \\[1.5em]
    \tan θ = \dfrac{y}{x} & \cot θ = \dfrac{x}{y}
  \end{matrix}
\]

## Identities

### Pythagorean

\[
  \begin{aligned}
    \sin^2 θ + \cos^2 θ &= 1 \\
    \tan^2 θ + 1 &= \sec^2 θ \\
    \cot^2 θ + 1 &= \csc^2 θ
  \end{aligned}
\]

### Reciprocal

\[
  \begin{matrix}
    \sin x = \dfrac{1}{\csc x} & \csc x = \dfrac{1}{\sin x} \\[1.5em]
    \cos x = \dfrac{1}{\sec x} & \sec x = \dfrac{1}{\cos x} \\[1.5em]
    \tan x = \dfrac{1}{\cot x} & \cot x = \dfrac{1}{\tan x}
  \end{matrix}
\]

### Quotient

\[
  \begin{matrix}
    \sin x = \dfrac{\tan x}{\sec x} & \csc x = \dfrac{\cot x}{\cos x} \\[1.5em]
    \cos x = \dfrac{\cot x}{\csc x} & \sec x = \dfrac{\tan x}{\sin x} \\[1.5em]
    \tan x = \dfrac{\sin x}{\cos x} & \cot x = \dfrac{\cos x}{\sin x}
  \end{matrix}
\]

### Cofunction

The value of a trig function of an angle equals the value of the cofunction of the complement of the angle.

\[
  \begin{aligned}
    \sin \left(\frac{π}{2} - x \right) &= \cos x & \cos \left(\frac{π}{2} - x \right) &= \sin x \\[1.5em]
    \tan \left(\frac{π}{2} - x \right) &= \cot x & \cot \left(\frac{π}{2} - x \right) &= \tan x \\[1.5em]
    \sec \left(\frac{π}{2} - x \right) &= \csc x & \csc \left(\frac{π}{2} - x \right) &= \sec x
  \end{aligned}
\]

### Symmetries

#### Even/Odd

\[
  \begin{aligned}
    \sin(-x) &=          - \sin x & \csc(-x) &=          - \csc x && \text{Odd}  \\
    \cos(-x) &= \phantom{-}\cos x & \sec(-x) &= \phantom{-}\sec x && \text{Even} \\
    \tan(-x) &=          - \tan x & \cot(-x) &=          - \cot x && \text{Odd}
  \end{aligned}
\]

#### Periodicity

\[
  \begin{aligned}
    \sin(x +          2 π) &= \sin x & \csc(x +          2 π) = \csc x \\
    \cos(x +          2 π) &= \cos x & \sec(x +          2 π) = \sec x \\
    \tan(x + \phantom{2}π) &= \tan x & \cot(x + \phantom{2}π) = \cot x
  \end{aligned}
\]

### Sum/Difference

\[
  \begin{aligned}
    \sin(x + y) &= \sin x \cos y + \cos x \sin y \\
    \sin(x - y) &= \sin x \cos y - \cos x \sin y \\[1em]
    \cos(x + y) &= \cos x \cos y - \sin x \sin y \\
    \cos(x - y) &= \cos x \cos y + \sin x \sin y \\[1em]
    \tan(x + y) &= \frac{\tan x + \tan y}{1 - \tan x \tan y} \\[1em]
    \tan(x - y) &= \frac{\tan x - \tan y}{1 + \tan x \tan y}
  \end{aligned}
\]

### Half Angle

\[
  \begin{aligned}
    \sin\frac{x}{2} &= \pm \sqrt{\frac{1 - \cos x}{2}}          \\[1em]
    \cos\frac{x}{2} &= \pm \sqrt{\frac{1 + \cos x}{2}}          \\[1em]
    \tan\frac{x}{2} &= \pm \sqrt{\frac{1 - \cos x}{1 + \cos x}} \\[1em]
                    &= \frac{\sin x}{1 + \cos x}                \\[1em]
                    &= \frac{1 - \cos x}{\sin x}
  \end{aligned}
\]

### Double Angle

\[
  \begin{aligned}
    \sin 2x &= 2 \sin x \cos x               \\[1em]
    \cos 2x &= \cos^2 x - \sin^2 x           \\
            &= 1 - 2 \sin^2 x                \\
            &= 2 \cos^2 x - 1                \\[1em]
    \tan 2x &= \frac{2 \tan x}{1 - \tan^2 x}
  \end{aligned}
\]

### Triple Angle

\[
  \begin{aligned}
    \sin 3x &=       \phantom{-}3 \sin x - 4 \sin^3 x                  \\[1em]
    \cos 3x &=                - 3 \cos x + 4 \cos^3 x                  \\[.5em]
    \tan 3x &= \phantom{-}\frac{3 \tan x -   \tan^3 x}{1 - 3 \tan^2 x}
  \end{aligned}
\]

### Product to Sum

\[
  \begin{aligned}
    \cos x \cos y &= \tfrac{1}{2} ~[~     \cos(x - y) +     \cos(x + y) ~] \\[.5em]
    \sin x \sin y &= \tfrac{1}{2} ~[~     \cos(x - y) -     \cos(x + y) ~] \\[.5em]
    \sin x \cos y &= \tfrac{1}{2} ~[~ \;\!\sin(x - y) + \;\!\sin(x + y) ~]
  \end{aligned}
\]

### Sum to Product

\[
  \begin{aligned}
    \sin x + \sin y &= \phantom{-}2 \sin \left(\frac{x + y}{2} \right) \cos \left( \frac{x - y}{2} \right) \\[1.5em]
    \sin x - \sin y &= \phantom{-}2 \cos \left(\frac{x + y}{2} \right) \sin \left( \frac{x - y}{2} \right) \\[1.5em]
    \cos x + \cos y &= \phantom{-}2 \cos \left(\frac{x + y}{2} \right) \cos \left( \frac{x - y}{2} \right) \\[1.5em]
    \cos x - \cos y &=          - 2 \sin \left(\frac{x + y}{2} \right) \sin \left( \frac{x - y}{2} \right)
  \end{aligned}
\]

### Square to Linear

\[
  \begin{aligned}
    \sin^2 x = \frac{1 - \cos 2x}{2} \\[1em]
    \cos^2 x = \frac{1 + \cos 2x}{2} \\[1em]
    \tan^2 x = \frac{1 - \cos 2x}{1 + \cos 2x}
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
  \frac{\sin A}{a} = \frac{\sin B}{b} = \frac{\sin C}{c}
\]

### Law of Cosines

\[
  \begin{aligned}
    a^2 &= b^2 + c^2 - 2bc\cos A \\
    b^2 &= c^2 + a^2 - 2ca\cos B \\
    c^2 &= a^2 + b^2 - 2ab\cos C
  \end{aligned}
\]

### Area of a Triangle

\[
  \begin{aligned}
    \text{Given} & \\
               s &= \frac{a + b + c}{2} = \text{semiperimeter,} \\[.5em]
               l &= \text{length of side of equilateral triangle,} \\
               r &= \text{inradius,} \\
               R &= \text{radius of circumcircle,} \\[2em]
     \text{Area} &= \tfrac{1}{2}bh \\[.5em]
                 &= \tfrac{1}{2}ab \sin C = \tfrac{1}{2}bc \sin A = \tfrac{1}{2}ca \sin B \\[.5em]
                 &= \sqrt{s(s - a)(s - b)(s - c)} && \text{Heron's Formula} \\[.5em]
                 &= rs \\[0em]
                 &= \frac{abc}{4R}
  \end{aligned}
\]

