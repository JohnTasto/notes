# Derivatives

## Definition

\[
  \frac{d}{dx} f(x) = \lim_{Δx \to 0} \frac{f(x + Δx) - f(x)}{Δx}
\]

## Rules

\[
  \begin{aligned}
        \frac{d}{dx} f(x) \pm g(x) &= f'(x) \pm g'(x)                          && \text{Sum/Difference}  \\[1em]
               \frac{d}{dx} c f(x) &= cf'(x)                                   && \text{Scalar Multiple} \\[1em]
             \frac{d}{dx} f(x)g(x) &= f'(x)g(x) + f(x)g'(x)                    && \text{Product}         \\[1em]
    \frac{d}{dx} \frac{f(x)}{g(x)} &= \frac{f'(x)g(x) - f(x)g'(x)}{g^2(x)}     && \text{Quotient}        \\[1em]
              \frac{d}{dx} f(g(x)) &= f'(g(x))g'(x)                            && \text{Chain}           \\[1em]
              \frac{d}{dx} f(g(x)) &= \frac{d f(g(x))}{dg(x)} \frac{dg(x)}{dx} && \text{Chain}           \\[1em]
                     \frac{dy}{dx} &= \frac{dy}{du} \frac{du}{dx},~~
                                              \begin{aligned}
                                                y &= f(g(x)) = f(u) \\[-.15em]
                                                u &= g(x)           \\[-1.8em]
                                              \end{aligned}                    && \text{Chain}
  \end{aligned}
\]

## Common Derivatives

\[
  \begin{aligned}
    \frac{d}{dx}            C &= 0                       & \frac{d}{dx}          x^n &= nx^{n-1}                 \\[3em]
    \frac{d}{dx}          e^x &= e^x                     & \frac{d}{dx}          a^x &= a^x \ln a                \\[1em]
    \frac{d}{dx}        \ln x &= \frac{1}{x} = x^{-1}    & \frac{d}{dx}     \log_a x &= \frac{1}{x \ln a}        \\[3em]
    \frac{d}{dx}       \sin x &= \cos   x                & \frac{d}{dx}       \cos x &= -\sin   x                \\[1em]
    \frac{d}{dx}       \tan x &= \sec^2 x                & \frac{d}{dx}       \cot x &= -\csc^2 x                \\[1em]
    \frac{d}{dx}       \sec x &= \sec   x \tan x         & \frac{d}{dx}       \csc x &= -\csc   x \cot x         \\[3em]
    \frac{d}{dx}  \sin^{-1} x &= \frac{1}{ \sqrt{1-x^2}} & \frac{d}{dx}  \cos^{-1} x &= -\frac{1}{ \sqrt{1-x^2}} \\[1em]
    \frac{d}{dx}  \tan^{-1} x &= \frac{1}{       1+x^2 } & \frac{d}{dx}  \cot^{-1} x &= -\frac{1}{       1+x^2}  \\[1em]
    \frac{d}{dx}  \sec^{-1} x &= \frac{1}{x\sqrt{x^2-1}} & \frac{d}{dx}  \csc^{-1} x &= -\frac{1}{x\sqrt{x^2-1}} \\[3em]
    \frac{d}{dx}      \sinh x &= \cosh x ~??             & \frac{d}{dx}      \cosh x &= \sinh x ~??              \\[1em]
    \frac{d}{dx} \sinh^{-1} x &= \frac{1}{\sqrt{1+x^2}}  & \frac{d}{dx} \cosh^{-1} x &= \frac{1}{\sqrt{x^2-1}}
  \end{aligned}
\]

## Implicit Differentiation

Implicit differentiation allows taking derivatives of equations without a clear dependant variable.
Pick one variable to differentiate with respect to, then treat all other variables as though they were functions of that one.

Example:

\[
  \begin{aligned}
                                       x^2 + y^2 &= 1                \\[.25em]
                        \tfrac{d}{dx}[x^2 + y^2] &= \tfrac{d}{dx}[1] \\[.5em]
        \tfrac{d}{dx}[x^2] + \tfrac{d}{dx} [y^2] &= 0                \\[.5em]
    2x + \tfrac{d}{dy}[y^2] \cdot \tfrac{dy}{dx} &= 0                \\[.5em]
                    2x + 2y \cdot \tfrac{dy}{dx} &= 0                \\[.5em]
                                  \tfrac{dy}{dx} &= -\tfrac{x}{y}
  \end{aligned}
\]

Example:

\[
  \begin{aligned}
                                                (x-y)^2 &= x + y - 1                \\[.25em]
                                 \tfrac{d}{dx}[(x-y)^2] &= \tfrac{d}{dx}[x + y - 1] \\[.5em]
    \tfrac{d}{d(x-y)}[(x-y)^2] \cdot \tfrac{d}{dx}[x-y] &= 1 + \tfrac{dy}{dx}       \\[.5em]
                           2(x - y)(1 - \tfrac{dy}{dx}) &= 1 + \tfrac{dy}{dx}       \\[.5em]
                          (2x - 2y)(1 - \tfrac{dy}{dx}) &= 1 + \tfrac{dy}{dx}       \\[.5em]
                    (2x - 2y) + (2y - 2x)\tfrac{dy}{dx} &= 1 + \tfrac{dy}{dx}       \\[.5em]
               (2y - 2x)\tfrac{dy}{dx} - \tfrac{dy}{dx} &= 1 - (2x - 2y)            \\[.5em]
                            (2y - 2x - 1)\tfrac{dy}{dx} &= 2y - 2x + 1              \\[.5em]
                                         \tfrac{dy}{dx} &= \tfrac{2y-2x+1}{2y-2x-1}
  \end{aligned}
\]

## Partial Derivatives

Definition (for $x$ direction):

\[
  \frac{\partial}{\partial x} f(x, y, \ldots) = \lim_{h \to 0} \frac{f(x + h, y, \ldots) - f(x, y, \ldots)}{h}
\]

Notation:

\[
  \begin{aligned}
    (f_x)_x &= f_{xx} =
    \frac{\partial}{\partial x} \frac{\partial f}{\partial x} = \;\frac{\partial^2 f}{\partial x^2} \\[1.5em]
    (f_y)_x &= f_{yx} =
    \frac{\partial}{\partial x} \frac{\partial f}{\partial y} = \frac{\partial^2 f}{\partial x \partial y} \\[1.5em]
    (f_x)_y &= f_{xy} =
    \frac{\partial}{\partial y} \frac{\partial f}{\partial x} = \frac{\partial^2 f}{\partial y \partial x} \\[1.5em]
    (f_y)_y &= f_{yy} =
    \frac{\partial}{\partial y} \frac{\partial f}{\partial y} = \;\frac{\partial^2 f}{\partial y^2}
  \end{aligned}
\]

To calculate a partial derivative, choose which variable to differentiate with respect to, then treat all other variables as though they are constants.

## Gradient

The gradient vector function, $\nabla f$, points towards higher values of $f$.

\[
  \nabla f =
  \begin{bmatrix}
    \dfrac{\partial f}{\partial x} \\[1.5em]
    \dfrac{\partial f}{\partial y} \\[2.5em]
    ~~~~\vdots~~~~
  \end{bmatrix}
\]

## Directional Derivatives

Definition:

\[
  \nabla_{\vec{v}}f(\vec{x}) = \lim_{h \to 0} \frac{f(\vec{x} + h \vec{v}) - f(\vec{x})}{h}
\]

Notation:

\[
  \nabla_{\vec{v}}f ~~=~~
  \frac{\partial f}{\partial \vec{v}} ~~=~~
  f'_{\vec{v}} ~~=~~
  D_{\vec{v}}f ~~=~~
  \partial_{\vec{v}}f
\]

Formula:

\[
  \nabla_{\vec{v}}f ~~~~=~~~~
  v_1\frac{\partial f}{\partial x} + v_2\frac{\partial f}{\partial y} + \ldots ~~~~=~~~~
  \begin{bmatrix}
    \frac{\partial f}{\partial x} \\[1em]
    \frac{\partial f}{\partial y} \\[1em]
    ~~~\vdots~~~
  \end{bmatrix}
  \cdot
  \begin{bmatrix}
    v_1 \\[1em]
    v_2 \\[1em]
    ~~\vdots~~
  \end{bmatrix} ~~~~=~~~~
  \nabla f \cdot \vec{v}
\]

To find the actual slope of $f$ in the direction of $\vec{v}$, either:
  1. make sure $\vec{v}$ is a unit vector in the above formula, or
  2. divide the result of the above formula by the magnitude of $\vec{v}$: $\frac{\nabla_{\vec{v}}f}{\Vert\vec{v}\Vert}$


## Curvature

\[
  \begin{aligned}
    \vec{s}(t) &= \begin{bmatrix}
      s_{\hat{i}}(t) \\[1em] s_{\hat{j}}(t) \\[1em] ~~~~\vdots~~~~
    \end{bmatrix}
    && \text{position of vector valued function} \\[2.75em]
    \vec{s}\,'(t) &= \frac{d\vec{s}}{dt} = \begin{bmatrix}
      \frac{ds_{\hat{i}}}{dt} \\[1em] \frac{ds_{\hat{j}}}{dt} \\[1em] ~~~~\vdots~~~~
    \end{bmatrix}
    && \text{velocity / tangent} \\[3.25em]
    \hat{T}(t) &= \frac{\vec{s}\,'}{\Vert\vec{s}\,'\Vert}
    && \text{unit tangent vector} \\[1.5em]
    & \phantom{=} {\Bigg\Vert \dfrac{d\hat{T}}{dt} \Bigg\Vert}
    && \text{curvature, scaled by velocity} \\[1.5em]
    κ(t) &= \Bigg\Vert\frac{d\hat{T}}{ds}\Bigg\Vert
    = \frac{\Bigg\Vert\dfrac{d\hat{T}}{dt}\Bigg\Vert}{\Bigg\Vert\dfrac{d\vec{s}}{dt}\Bigg\Vert}
    && \text{curvature} \\[2.75em]
    R(t) &= \frac{1}{κ}
    && \text{radius} \\[4em]
    κ(t) &= \frac{x'y'' - x''y'}{(x'^2 + y'^2)^\frac{3}{2}}
    && \text{curvature of a curve on a plane} \\[1.5em]
    κ(x) &= \frac{y''}{(1 +  y'^2)^\frac{3}{2}}
    && \text{curvature of a graph, $y = f(x)$}
  \end{aligned}
\]
