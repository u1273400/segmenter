
## Linearization

Many physical systems are linear within some limited range.  However, as the operating range is increased without limit (i.e. stretching of a spring beyond its elastic limit) they become non-linear

Electrical and mechanical elements are often linear over large range of variable, while this is not usually the case for themral or fluidic elements.

### Linear System

A system is defined to be linear when two relations are satisfied between the system excitation (i.e. its input x(t)) and its corresponding response (i.e. its output y(t))

1. **Principle of Superposition**: For to excitations and their corresponding resposes $\{x_1(t),y_1(t)\}$ and $\{x_2(t),y_2(t)\}$ the folloing is a necessary for linearity, which is that a third excitation $\{x_1(t)+x_2(t)\}$ should result in a response $\{y_1(t)+y_2(t)\}$ 

2. **Property of Homogeneity:** For a given excitation and response {x(t),y(t)}, if the excitation is multliplied by a constant $\beta$ then the response should be equal to $\beta y$.

#### Example
- $y=x^2$ is not linear since it does not satisfy the principle of superposition.
- $y=mx+c$ is not linear since it does not satisfy the property of homogeneity

### Linear Approximation of non-linear systems

This is possible by approximating non-linear system to linear models about some operating point.  Consider y=mx+c to be linear about an operating point $(x_0,y_0)$ for small changes in $\Delta x$ and $\Delta y$.  For example
$$ \begin{aligned} y&=mx+c 
\\ y_0+\Delta y & =mx_0+m\Delta x+c \end{aligned}$$
which satisfies the homogeneity property since
$$\Delta y=m\Delta x $$

### General Linearisation Procedure

The above approach can be generalised to other complex input-output relationship using Taylor series expansion.

For example, let us represent the system excitation-response as a continuous relation as below:

$$y(t)=g(x(t))$$

and chose the operating point to be $x_0$, then we can expand g(.) using Taylor's series expansion as follows:


$$ y=g(x_0)+\frac{dg}{dx}_{|x=x_0}\frac{x-x_0}{1!}+\frac{d^2g}{dx^2}_{|x=x_0}\frac{(x-x_0)^2}{2!}+\dots(1)$$
the slope at the operating point is a constant
$$ \frac{dg}{dx}_{|x=x_0} $$
and it is a good approximate to the curve over the small range $(x-x_0)$ about the operating point.  So if we limit the operation to within with small range, we can truncate the Taylor series in the equation (1) at the term of the first derivative as below:
$$ y=g(x_0)+\frac{dg}{dx}_{|x=x_0}(x-x_0) $$
if we now replace the g(x) terms in the approximation above by their y values, the form approximation becomes apparent and we can see that it is the same as made in previous y=mx+c example.
$$ y=g(x_0)+\frac{dg}{dx}_{|x=x_0}(x-x_0)=y_0+m(x-x_0) $$

we can rearrange the equation above, so the result we want is more obvious
$$ y=y_0+m(x-x_0) $$
$$ y-y_0=m(x-x_0) $$
$$ \Delta=m\Delta x $$

So the general approach is to expand the function using the Taylor expansion and truncate it at the first derivative and limit the variation of x to small values (i.e. $\Delta x$).

This method can be easily extended to functions of more than one variable (i.e. if y were a function of time and temperature, then y wuold be a function of two variables).

### Linearisation Steps
For non-linear systems we must linearize the system so we can find the transfer function.  The first step is to recognise the non-linear component and write the nonlinear differential equation.  Then we linearise a nonlinear equation, we linearize it for a very small signal inputs about a steady-state solution when the small-signal input is equal to zero.  This steady-state solution is called equilibrium and is selected as the second step in the linearisation process.  For example when a pendulum is at rest, it is at equilibrium.  The angular displacement is described by a non-linear differential equation, but it can be expressed with a linear differential equation for small excursions about this equilibrium point.

Next we linearise the nonlinear differential equation, and then we take the Laplace transform of the linearised differential equation, assuming zero initial conditions.  Finally, we separate input and output variables and form the tranfer function.  Let us first see how to linearise a function; later, wewill apply the method to linearisation of a differential equation.
![figure 1](https://selene.hud.ac.uk/u1273400/images/seg_media/c6.PNG)
**Figure 1:** Linearisation about point A.

If we assume a nonlinear system operating at point A, $[x_0,f(x_0)]$ in figure 1 above, small changes in the input can be related to changes in the output about the point by way of the sope of the curve at the point A.  Thus, if the slope of the curve at point A is $m_a$, then small excursions of the input point A, \delta_x, yield small changes inthe output, \delta f(x), related by the sope at point A. Thus,
$$[f(x)-f(x_0)]\approx m_a(x-x_0) - - - -\dots(2) $$
from which
$$ \delta f(x)\approx m_a\delta x - - - - \dots(3) $$
and
$$ f(x) \approx f(x_0)+m_a(x-x_0)\approx f(x_0)+m_a\delta x - - - - \dots(4) $$

This relationship is shown graphically in figure 1, where a new set of axes, $\delta x$ and $\delta f(x)$, is created at the point A, and f(x) is approximately equal to $f(x_0), the ordinate of the new origin, plus small excursions, $m_a\delta x$, away from point A.  Let us look at an example.

#### Example 1
Linearize f(x)=5 cos x about $x=\pi/2$.
![figure 2](https://selene.hud.ac.uk/u1273400/images/seg_media/c7.PNG)**Figure 2:** Linearisation of 5 cos x about $x=\pi/2$.

#### Solution
We first find the derivitive of f(x) that is df/dx=-5 sin x.  $x=\pi/2$, the derivative is -5.  Also $f(x_0)=f(\pi/2)=5 cos (\pi/2)=0$.  Thus, from equation (4), the system can be represented as $f(x)=-5\delta x$ for small excursions of x about $\pi/2$.  The process is shown in figure 2, where the cosine curve does inded look like a straight line of slope -5 near $\pi/2$


```R

```
