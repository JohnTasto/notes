# Derivatives

## Definition

\[
  \drv{}x f(x) = \lim_{Δx \to 0} {f(x + Δx) - f(x) \over Δx}
\]

## Rules

\[
  \begin{aligned}
      \drv{}{x} (f(x) \pm g(x)) &= f'(x) \pm g'(x)                      && \text{Sum/Difference}  \h7 \\
               \drv{}{x} c f(x) &= cf'(x)                               && \text{Scalar Multiple} \h7 \\
             \drv{}{x} f(x)g(x) &= f'(x)g(x) + f(x)g'(x)                && \text{Product}         \h7 \\
    \drv{}{x} {f(x) \over g(x)} &= {f'(x)g(x) - f(x)g'(x) \over g^2(x)} && \text{Quotient}        \h7 \\
              \drv{}{x} f(g(x)) &= f'(g(x))g'(x)                        && \text{Chain}           \h7 \\
              \drv{}{x} f(g(x)) &= \drv{f(g(x))}{g(x)} \drv{g(x)}{x}    && \text{Chain}           \h7 \\
                     \drv{y}{x} &= \drv{y}{u} \drv{u}{x}, ~~
                                   \begin{aligned}
                                     y &= f(g(x)) = f(u) \\[-.15em]
                                     u &= g(x)           \\[-1.8em]
                                   \end{aligned}                        && \text{Chain}           \h7 \\
  \end{aligned}
\]

## Common Derivatives

\[
  \begin{aligned}
    \drv{}{x}            C &= 0                       & \drv{}{x}          x^n &= nx^{n-1}                 \h7 \\[2em]
    \drv{}{x}          e^x &= e^x                     & \drv{}{x}          a^x &= a^x \ln a                \h7 \\
    \drv{}{x}        \ln x &= {1 \over x} = x^{-1}    & \drv{}{x}     \log_a x &= {1 \over x \ln a}        \h7 \\[2em]
    \drv{}{x}       \sin x &= \cos   x                & \drv{}{x}       \cos x &= -\sin   x                \h7 \\
    \drv{}{x}       \tan x &= \sec^2 x                & \drv{}{x}       \cot x &= -\csc^2 x                \h7 \\
    \drv{}{x}       \sec x &= \sec   x \tan x         & \drv{}{x}       \csc x &= -\csc   x \cot x         \h7 \\[2em]
    \drv{}{x}  \sin^{-1} x &= {1 \over  \sqrt{1-x^2}} & \drv{}{x}  \cos^{-1} x &= -{1 \over  \sqrt{1-x^2}} \h7 \\
    \drv{}{x}  \tan^{-1} x &= {1 \over        1+x^2 } & \drv{}{x}  \cot^{-1} x &= -{1 \over        1+x^2}  \h7 \\
    \drv{}{x}  \sec^{-1} x &= {1 \over x\sqrt{x^2-1}} & \drv{}{x}  \csc^{-1} x &= -{1 \over x\sqrt{x^2-1}} \h7 \\[2em]
    \drv{}{x}      \sinh x &= \cosh x ~??             & \drv{}{x}      \cosh x &= \sinh x ~??              \h7 \\
    \drv{}{x} \sinh^{-1} x &= {1 \over  \sqrt{1+x^2}} & \drv{}{x} \cosh^{-1} x &=  {1 \over  \sqrt{x^2-1}} \h7 \\
  \end{aligned}
\]

## Implicit Differentiation

Implicit differentiation allows taking derivatives of equations without a clear dependant variable.
Pick one variable to differentiate with respect to, then treat all other variables as though they were functions of that one.

Example:

\[
  \begin{aligned}
                                 x^2 + y^2 &= 1             \h4 \\
                     \tdrv{}{x}[x^2 + y^2] &= \tdrv{}{x}[1] \h4 \\
        \tdrv{}{x}[x^2] + \tdrv{}{x} [y^2] &= 0             \h4 \\
    2x + \tdrv{}{y}[y^2] \cdot \tdrv{y}{x} &= 0             \h4 \\
                 2x + 2y \cdot \tdrv{y}{x} &= 0             \h4 \\
                               \tdrv{y}{x} &= -\tfrac{x}{y} \h4 \\
  \end{aligned}
\]

Example:

\[
  \begin{aligned}
                                          (x-y)^2 &= x + y - 1                \h4 \\
                              \tdrv{}{x}[(x-y)^2] &= \tdrv{}{x}[x + y - 1]    \h4 \\
    \tdrv{}{(x-y)}[(x-y)^2] \cdot \tdrv{}{x}[x-y] &= 1 + \tdrv{y}{x}          \h4 \\
                        2(x - y)(1 - \tdrv{y}{x}) &= 1 + \tdrv{y}{x}          \h4 \\
                       (2x - 2y)(1 - \tdrv{y}{x}) &= 1 + \tdrv{y}{x}          \h4 \\
                 (2x - 2y) + (2y - 2x)\tdrv{y}{x} &= 1 + \tdrv{y}{x}          \h4 \\
               (2y - 2x)\tdrv{y}{x} - \tdrv{y}{x} &= 1 - (2x - 2y)            \h4 \\
                         (2y - 2x - 1)\tdrv{y}{x} &= 2y - 2x + 1              \h4 \\
                                      \tdrv{y}{x} &= \tfrac{2y-2x+1}{2y-2x-1} \h4 \\
  \end{aligned}
\]

## Partial Derivatives

Definition (for $x$ direction):

\[
  \part{}{x} f(x, y, \ldots) = \lim_{h \to 0} {f(x + h, y, \ldots) - f(x, y, \ldots) \over h}
\]

Notation:

\[
  \begin{aligned}
    (f_x)_x &= f_{xx} = \part{}{x} \part{f}{x} = \;\part{^2 f}{x^2}         \h7 \\
    (f_y)_x &= f_{yx} = \part{}{x} \part{f}{y} =   \part{^2 f}{x\partial y} \h7 \\
    (f_x)_y &= f_{xy} = \part{}{y} \part{f}{x} =   \part{^2 f}{y\partial x} \h7 \\
    (f_y)_y &= f_{yy} = \part{}{y} \part{f}{y} = \;\part{^2 f}{y^2}         \h7 \\
  \end{aligned}
\]

To calculate a partial derivative, choose which variable to differentiate with respect to, then treat all other variables as though they are constants.

## Gradient

The gradient vector function, $\nabla f$, points towards higher values of $f$.

\[
  \nabla f =
  \begin{bmatrix}
    \dpart{f}{x}   \h7 \\
    \dpart{f}{y}   \h7 \\
    ~~~~\vdots~~~~ \h7 \\
  \end{bmatrix}
\]

## Directional Derivatives

Definition:

\[
  \nabla_{\vec{v}}f(\vec{x}) = \lim_{h \to 0} {f(\vec{x} + h \vec{v}) - f(\vec{x}) \over h}
\]

Notation:

\[
  \nabla_{\vec{v}}f ~~=~~ \part{f}{\vec{v}} ~~=~~ f'_{\vec{v}} ~~=~~ D_{\vec{v}}f ~~=~~ \partial_{\vec{v}}f
\]

Formula:

\[
  \nabla_{\vec{v}}f ~~~~=~~~~
  v_1\part{f}{x} + v_2\part{f}{y} + \cdots ~~~~=~~~~
  \begin{bmatrix}
    \part{f}{x}  \h5 \\
    \part{f}{y}  \h5 \\
    ~~~\vdots~~~ \h5 \\
  \end{bmatrix}
  \cdot
  \begin{bmatrix}
    v_1        \h5 \\
    v_2        \h5 \\
    ~~\vdots~~ \h5 \\
  \end{bmatrix} ~~~~=~~~~
  \nabla f \cdot \vec{v}
\]

To find the actual slope of $f$ in the direction of $\vec{v}$, either:
  1. make sure $\vec{v}$ is a unit vector in the above formula, or
  2. divide the result of the above formula by the magnitude of $\vec{v}$: ${\nabla_{\vec{v}}f \over \|\vec{v}\|}$

## Curvature

\[
  \begin{aligned}
    \vec{s}(t) &= \begin{bmatrix}
      s_{\hat{i}}(t)       \h5 \\ s_{\hat{j}}(t)       \h5 \\ ~~~~\vdots~~~~ \h5 \\
    \end{bmatrix}
    && \text{position of vector valued function}     \\[.5em]
    \vec{s}\,'(t) &= \drv{\vec{s}}{t} = \begin{bmatrix}
      \drv{s_{\hat{i}}}{t} \h5 \\ \drv{s_{\hat{j}}}{t} \h5 \\ ~~~~\vdots~~~~ \h5 \\
    \end{bmatrix}
    && \text{velocity / tangent}                     \\[.5em]
    \hat{T}(t) &= {\vec{s}\,' \over \|\vec{s}\,'\|}
    && \text{unit tangent vector}                \h7 \\
    & \p{{}={}} {\Bigg\| \drv{\hat{T}}{t} \Bigg\|}
    && \text{curvature, scaled by velocity}      \h7 \\
    κ(t) &= \Bigg\| \drv{\hat{T}}{s} \Bigg\|
    = {\Bigg\| \ddrv{\hat{T}}{t} \Bigg\| \over \Bigg\| \ddrv{\vec{s}}{t} \Bigg\|}
    && \text{curvature}                          \h7 \\
    R(t) &= {1 \over κ}
    && \text{radius}                             \h7 \\[2em]
    κ(t) &= {x'y'' - x''y' \over (x'^2 + y'^2)^\frac32}
    && \text{curvature of a curve on a plane}    \h7 \\
    κ(x) &= {y'' \over (1 +  y'^2)^\frac32}
    && \text{curvature of a graph, $y = f(x)$}   \h7 \\
  \end{aligned}
\]
