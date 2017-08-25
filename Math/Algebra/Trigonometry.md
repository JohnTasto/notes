# Trigonometry

## Values

\[
  \begin{array}{cc|cccccc}
    \text{deg} &  \text{rad}   &    \sin \theta     &    \cos \theta     &    \tan \theta     &     \csc \theta     &     \sec \theta     &    \cot \theta     \\
      \qquad   &    \qquad     &       \qquad       &       \qquad       &       \qquad       &        \qquad       &        \qquad       &       \qquad       \\
     0\degree  &       0       &         0          &         1          &         0          &          -          &          1          &         -          \\[1em]
    30\degree  & \frac{\pi}{6} &    \frac{1}{2}     & \frac{\sqrt{3}}{2} & \frac{\sqrt{3}}{3} &          2          & \frac{2\sqrt{3}}{3} &      \sqrt{3}      \\[1em]
    45\degree  & \frac{\pi}{4} & \frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} &         1          &      \sqrt{2}       &      \sqrt{2}       &         1          \\[1em]
    60\degree  & \frac{\pi}{3} & \frac{\sqrt{3}}{2} &    \frac{1}{2}     &      \sqrt{3}      & \frac{2\sqrt{3}}{3} &          2          & \frac{\sqrt{3}}{3} \\[1.5em]
    90\degree  & \frac{\pi}{2} &         1          &         0          &         -          &          1          &          -          &         0          \\
  \end{array}
\]

## Radians to Degrees

\[
  \begin{aligned}
     0\degree &=             0 &  90\degree &=  \frac{\pi}{2} & 180\degree &=            \pi & 270\degree &=  \frac{3\pi}{2} \\[1em]
    30\degree &= \frac{\pi}{6} & 120\degree &= \frac{2\pi}{3} & 210\degree &= \frac{7\pi}{6} & 300\degree &=  \frac{5\pi}{3} \\[1em]
    45\degree &= \frac{\pi}{4} & 135\degree &= \frac{3\pi}{4} & 225\degree &= \frac{5\pi}{4} & 315\degree &=  \frac{7\pi}{4} \\[1em]
    60\degree &= \frac{\pi}{3} & 150\degree &= \frac{5\pi}{6} & 240\degree &= \frac{4\pi}{3} & 330\degree &= \frac{11\pi}{6} \\[1em]
    90\degree &= \frac{\pi}{2} & 180\degree &=            \pi & 270\degree &= \frac{3\pi}{2} & 360\degree &=            2\pi \\
  \end{aligned}
\]

## Definitions

### SOHCAHTOA

\[
  \begin{aligned}
    \sin \theta &= \frac{\text{opposite}}{\text{hypotenuse}} = y & \csc \theta &= \frac{\text{hypotenuse}}{\text{opposite}} \\[1.5em]
    \cos \theta &= \frac{\text{adjacent}}{\text{hypotenuse}} = x & \sec \theta &= \frac{\text{hypotenuse}}{\text{adjacent}} \\[1.5em]
    \tan \theta &= \frac{\text{opposite}}{\text{adjacent}} = \text{slope}  & \cot \theta &= \frac{\text{adjacent}}{\text{opposite}} \\
  \end{aligned}
\]

### Circle

\[
  \begin{matrix}
    \sin \theta = \frac{y}{r} & \csc \theta = \frac{r}{y} \\[1.5em]
    \cos \theta = \frac{x}{r} & \sec \theta = \frac{r}{x} \\[1.5em]
    \tan \theta = \frac{y}{x} & \cot \theta = \frac{x}{y} \\
  \end{matrix}
\]

## Identities

### Pythagorean

\[
  \begin{aligned}
    \sin^2 \theta + \cos^2 \theta &= 1 \\
    \tan^2 \theta + 1 &= \sec^2 \theta \\
    \cot^2 \theta + 1 &= \csc^2 \theta \\
  \end{aligned}
\]

### Reciprocal

\[
  \begin{matrix}
    \sin x = \frac{1}{\csc x} & \csc x = \frac{1}{\sin x} \\[1.5em]
    \cos x = \frac{1}{\sec x} & \sec x = \frac{1}{\cos x} \\[1.5em]
    \tan x = \frac{1}{\cot x} & \cot x = \frac{1}{\tan x} \\
  \end{matrix}
\]

### Ratio

\[
  \begin{aligned}
    \tan x &= \frac{\sin x}{\cos x} \\[1.5em]
    \cot x &= \frac{\cos x}{\sin x} \\
  \end{aligned}
\]

### Even/Odd

\[
  \begin{aligned}
    \sin(-x) &= -\sin x & \csc(-x) &= -\csc x \\
    \cos(-x) &= -\cos x & \sec(-x) &= -\sec x \\
    \tan(-x) &= -\tan x & \cot(-x) &= -\cot x \\
  \end{aligned}
\]

### Cofunction

The value of a trig function of an angle equals the value of the cofunction of the complement of the angle.

\[
  \begin{aligned}
    \sin \left(\frac{\pi}{2} - x \right) &= \cos x & \cos \left(\frac{\pi}{2} - x \right) &= \sin x \\[1.5em]
    \tan \left(\frac{\pi}{2} - x \right) &= \cot x & \cot \left(\frac{\pi}{2} - x \right) &= \tan x \\[1.5em]
    \sec \left(\frac{\pi}{2} - x \right) &= \csc x & \csc \left(\frac{\pi}{2} - x \right) &= \sec x \\
  \end{aligned}
\]

### Periodicity

\[
  \begin{aligned}
    \sin(x + 2\pi) &= \sin x & \csc(x + 2\pi) = \csc x \\
    \cos(x + 2\pi) &= \cos x & \sec(x + 2\pi) = \sec x \\
    \tan(x +  \pi) &= \sin x & \cot(x +  \pi) = \cot x \\
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
    \tan(x - y) &= \frac{\tan x - \tan y}{1 + \tan x \tan y} \\
  \end{aligned}
\]

### Double Angle

\[
  \begin{aligned}
    \sin 2x &= 2 \sin x \cos x               \\[1em]
    \cos 2x &= \cos^2 x - \sin^2 x           \\
            &= 1 - 2 \sin^2 x                \\
            &= 2 \cos^2 x - 1                \\[1em]
    \tan 2x &= \frac{2 \tan x}{1 - \tan^2 x} \\
  \end{aligned}
\]

### Half Angle

\[
  \begin{aligned}
    \sin\frac{x}{2} &= \pm \sqrt{\frac{1 - \cos x}{2}} & \sin^2 x = \frac{1 - \cos 2x}{2} \\[1em]
    \cos\frac{x}{2} &= \pm \sqrt{\frac{1 + \cos x}{2}} & \sin^2 x = \frac{1 + \cos 2x}{2} \\[1em]
    \tan\frac{x}{2} &= \pm \sqrt{\frac{1 - \cos x}{1 + \cos x}} \\[1em]
                    &= \frac{\sin x}{1 + \cos x} \\[1em]
                    &= \frac{1 - \cos x}{\sin x} \\
  \end{aligned}
\]

### Product to Sum

\[
  \begin{aligned}
    \cos x \cos y &= \tfrac{1}{2} ~[~ \cos(x + y) + \cos(x - y) ~] \\[.5em]
    \sin x \sin y &= \tfrac{1}{2} ~[~ \cos(x - y) - \cos(x + y) ~] \\[.5em]
    \sin x \cos y &= \tfrac{1}{2} ~[~ \sin(x + y) + \sin(x - y) ~] \\
  \end{aligned}
\]

### Sum to Product

\[
  \begin{aligned}
    \sin x + \sin y &= 2 \sin \left(\frac{x + y}{2} \right) \cos \left( \frac{x - y}{2} \right) \\[1.5em]
    \sin x - \sin y &= 2 \cos \left(\frac{x + y}{2} \right) \sin \left( \frac{x - y}{2} \right) \\[1.5em]
    \cos x + \cos y &= 2 \cos \left(\frac{x + y}{2} \right) \cos \left( \frac{x - y}{2} \right) \\[1.5em]
    \cos x - \cos y &= -2 \sin \left(\frac{x + y}{2} \right) \sin \left( \frac{x - y}{2} \right) \\
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
    c^2 &= a^2 + b^2 - 2ab\cos C \\
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
                 &= \frac{abc}{4R} \\
  \end{aligned}
\]

