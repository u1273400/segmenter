
### Converting a Transfer Function to a State Space
It is sometimes required to express the transfer function of a system in state variable notation.  This may be necessary if, for example, we wish to control a system with a known transfer functionusing 'state variable feedback control'.

*
At first a set of state variables, called phase variables, where each subsequent state variable is defiend to be the derivative of the previous state.  The general nth-order, linear differential equation with consant coefficients is evaluated in state space phase variable form as follows. We will later apply this representation to transfer functions.
*

*
Consider the differential equation
*
$$ \frac{d^ny}{dt^n}+a_{n-1}\frac{d^{n-1y}}{dt^{n-1}}+\dots+a_{1}\frac{dy}{dt}+a_0y=b_0u - - - - \dots(1)$$

*
A convenient way to choose state variables is to choose the output, y(t), and its (n-1) derivatives as the state variables.  This choice is called the phase-variable choice.  Choosing the state variables, x<sub>i</sub>, we get
*

$$\begin{matrix}
x_1=y - - - -\dots(2a)\\
x_2=\frac{dy}{dt} - - - -\dots(2b)\\
x_3=\frac{d^2y}{dt^2} - - - -\dots(2c)\\
\vdots \\
x_n=\frac{d^{n-1}y}{dt^{n-1}} - - - -\dots(2d)
\end{matrix} $$

and differentiating both sides yields
$$\begin{matrix}
\dot{x}_1=\frac{dy}{dt} - - - -\dots(3a)\\
\dot{x}_2=\frac{d^2y}{dt^2} - - - -\dots(3b)\\
\dot{x}_3=\frac{d^3y}{dt^3} - - - -\dots(3c)\\
\vdots \\
\dot{x}_n=\frac{d^{n}y}{dt^{n}} - - - -\dots(3d)
\end{matrix} $$

where the dot above the x signifies differentiation with respect to time.

Substituting the definitions of equestions (2) into (3)
$$\begin{matrix}
\dot{x}_1=x_2 - - - -\dots(4a)\\
\dot{x}_2=x_3 - - - -\dots(4b)\\
\vdots \\
\dot{x}_{n-1}=x_n - - - -\dots(4c)
\end{matrix} $$

and therefore equation (1) becomes
$$ \dot{x}_n=-a_0x_1-a_1x_2\dots-a_{n-1}x_n+b_0u - - - - \dots(5) $$

In vector matrix form equation (5) becomes
$$
\begin{bmatrix}\dot{x}_1\\ \dot{x}_2\\ \dot{x}_3\\ \vdots\\ \dot{x}_{n-1}\\ \dot{x}_n \end{bmatrix}=
\begin{bmatrix}
0 & 1 & 0 & 0 & \dots & 0 \\
0 & 0 & 1 & 0 & \dots & 0 \\
0 & 0 & 0 & 1 & \dots & 0 \\
\vdots \\
0 & 0 & 0 & 0 & \dots & 1 \\
-a_0&-a_1&-a_2&-a_3&\dots&-a_{n-1}
\end{bmatrix}
\begin{bmatrix}x_1\\ x_2\\ x_3\\ \vdots\\ x_{n-1}\\ x_n \end{bmatrix}+
\begin{bmatrix}0 \\ 0 \\ 0 \\ \vdots\\ 0 \\ b_0 \end{bmatrix}u
\dots(6)$$

*Equation (6) is the phase-variable form of the state equations.  This form is easily recognized by the unique pattern of 1's and 0's and the negative coefficients of the differential equation written in reverse order in the last for of the system matrix.*

*Finally, since the solution to the differential iequation is y(t), or x<sub>1</sub>, the output equation is*

$$ y=\begin{bmatrix}1 & 0 & 0 & \dots  & 0 \end{bmatrix}
\begin{bmatrix}x_1 \\ x_2 \\ x_3 \\ \vdots \\ x_{n-1} \\ x_n \end{bmatrix} - - - -\dots(7) $$

*In summary, then to convert a transfer function into equation in state, we first convert the transfer function to a differential equation by cross-multiplying and taking the inverse Laplace function, assuming zero initial conditions.  Then we represent the differential equation in state phase variable form.*

The methods used to convert a transfer function to state variable notation depends on whether or not there is a polynomial in s in the numerator, as illustrated by the following examples.

#### METHOD 1:  NO POLYNOMIAL IN s IN THE NUMERATOR
For this case, for an nth order system, we choose the state variables x<sub>1</sub> and x<sub>n</sub> as the system output and the (n-1) derivatives of the system output.  Note the “order” of the system is equal to the highest exponent of s in the transfer function denominator.

##### Example 1
Express the folloing tranfer function in state variable notation
$$ \frac{Y(s)}{u(s)}=\frac{100}{(s^2+9s+25)(1+s)} - - - - \dots(8)$$
$$ Y(s)(s^2+9s+25)(1+s)=100u(s)$$
$$\therefore (s^3+10s^2+34s+25)Y(s)=100u(s) - - - - \dots(9)$$

Taking the inverse Laplace Transforms of equation (9) and remembering that multiplication by s is equivalent to differentiation with respect to t in the time domain, we have:
$$ \dddot{y}+10\ddot{y}+34\dot{y}+25y=100u - - - - \dots(10)$$

We now choose our state variables as follows recalling y is the system output.  Recall that
$$\begin{aligned} x_1=y \\ x_2=\dot{x}_1=\dot{y} \\ x_3=\dot{x}_2= \ddot{y} \end{aligned} - - - - \dots(11) $$
Also note that $$ \dot{x}_3=\dddot{y} - - - - \dots(12) $$

From equations (5), (10), (11) and (12) we may write
$$ \dot{x}_3=-10x_3-34x_2-25x_1+100u - - - - \dots(13) $$

There fore the state variable matrix equation can be derived as follows:

$$ \begin{matrix}
\begin{bmatrix}\dot{x}_1\\ \dot{x}_2\\ \dot{x}_3\\ \vdots\\ \dot{x}_{n-1}\\ \dot{x}_n \end{bmatrix}=
\begin{bmatrix}
0 & 1 & 0 & 0 & \dots & 0 \\
0 & 0 & 1 & 0 & \dots & 0 \\
0 & 0 & 0 & 1 & \dots & 0 \\
\vdots \\
0 & 0 & 0 & 0 & \dots & 1 \\
-a_0&-a_1&-a_2&-a_3&\dots&-a_{n-1}
\end{bmatrix}
\begin{bmatrix}x_1\\ x_2\\ x_3\\ \vdots\\ x_{n-1}\\ x_n \end{bmatrix}+
\begin{bmatrix}0 \\ 0 \\ 0 \\ \vdots\\ 0 \\ b_0 \end{bmatrix}u
\dots(6)
\end{matrix} $$

And the corresponding output equation is given as
$$ y=\begin{bmatrix}1 & 0 & 0 & \dots  & 0 \end{bmatrix}
\begin{bmatrix}x_1 \\ x_2 \\ x_3 \\ \vdots \\ x_{n-1} \\ x_n \end{bmatrix} - - - -\dots(7) $$

##### Example 2
Find the state-space representation in phase-variable form for the transfer function shown in Figure 1a below
![Figure 1](https://selene.hud.ac.uk/u1273400/images/seg_media/s5.PNG)
**Figure 1:** a. Transfer function b. equivalent block diagram shoing phase variables.

##### Solution
###### Step 1
Find the associated differential equation
Since 
$$ \frac{C(s)}{R(s)}=\frac{24}{s^3+9s^2+26s+24} - - - - \dots(16)  $$
cross multiplying yields
$$ (s^3+9s^2+26s+24)C(s)=24R(s) - - - - \dots(17) $$

The corresponding differential equation is found by taking the inverse Laplace transform, assuming zero initial conditions:
$$ \dddot{c}+9\ddot{c}+26\dot{c}+24c=24r - - - - \dots(18) $$

The corresponding matrix equation is given as:

At this point, we can create an equivalent block diagram of the system to help visualise the state variables.  We draw three integral blocks a shown and lebel each output as the corresponding state variables as shown.

#### Method 2: Polynomial in s in the numberator

*If a transfer function has a polynomial in s in the numerator that is of order less than the polynomial in the denominator, as shown in figure 2a, the numerator and denomenator can be handled separately.  First separate the transfer function into two cascaded transfer functions, as shown in Figure 2b; the first is the denomenator and the second is the numerator.*
![figure 2](https://selene.hud.ac.uk/u1273400/images/seg_media/c4.PNG)
**Figure 2: ** Decomposing a transfer function

*The first transfer function with just the denominator is converted to the phase-variable representation in state space as shown in the preceding method and examples.  Hence, phase variable x<sub>1</sub> is the output, and the rest of the phase variables are the internal variables of the first block, as shown in Figure 2b.  The second transfer function with just the numerator yields*
$$ Y(s) = C(s) = (b_2s^2+b_1s+b_0)X_1(s) - - - - \dots(19) $$
*where, after taking the inverse Laplace transform with zero initial conditions,*
$$ y(t)=b_2\frac{d^2x_1}{dt^2}+b_1\frac{dx_1}{dt}+b_0x_1 - - - - \dots(20) $$
*But the derivative terms are the definitions of the phase variables obtained in the first block.  Thus, writing the terms in reverse order to conform to an output equation,*
$$ y(t)=b_0x_1+b_1x_2+b_2x_3 - - - - \dots(21) $$

*Hence, the second block simply forms a specified linear combination of the state variables developed in the first block.* In summary we choose n-state (phase) variables as an "intermediate" output and the (n-1) derivatives of this intermediate output.

*From another perspective, the denominator of the transfer function yields the state equations, while the numerator yields the output equation. The next example demonstrates the process.*

##### Example 3
Express the folloing transfer function in state variable notation.
$$ \frac{Y(s)}{U(s)}=\frac{s^2+7s+2}{s^3+9s^2+26s+24} - - - -\dots(22) $$

We write equation (22) in terms of an "intermediate" output x<sub>1</sub>(s) a follows:
$$ \frac{X_1(s)}{U(s)}=\frac{1}{s^3+9s^2+26s+24} - - - -\dots(23) $$

$$ \frac{Y(s)}{X_1(s)}=s^2+7s+2 - - - -\dots(24) $$

From equation 23 we have
$$\therefore (s^3+9s^2+26s+24)X_1(s)=u(s) - - - - \dots(25)$$

Taking the inverse Laplace Transforms of equation (25) we have:
$$ \dddot{x}+9\ddot{x}+26\dot{x}+24y=u - - - - \dots(26)$$

We now choose our state variables as follows recalling y is the system output.  Recall that
$$\begin{aligned} x_1 \\ x_2 &=\dot{x}_1 \\ x_3 &=\dot{x}_2= \ddot{x}_1 \end{aligned} - - - - \dots(27) $$
Also note that $$ \dot{x}_3=\dddot{x}_1 - - - - \dots(28) $$

From equations (5), (26), (27) and (28) we may write
$$ \dot{x}_3=-24x_3-26x_2-9x_1+u - - - - \dots(29) $$

There fore the state variable matrix equation can be derived as follows:

$$ \begin{matrix}
\begin{bmatrix}\dot{x}_1\\ \dot{x}_2\\ \dot{x}_3\\ \vdots\\ \dot{x}_{n-1}\\ \dot{x}_n \end{bmatrix}=
\begin{bmatrix}
0 & 1 & 0 & 0 & \dots & 0 \\
0 & 0 & 1 & 0 & \dots & 0 \\
0 & 0 & 0 & 1 & \dots & 0 \\
\vdots \\
0 & 0 & 0 & 0 & \dots & 1 \\
-a_0&-a_1&-a_2&-a_3&\dots&-a_{n-1}
\end{bmatrix}
\begin{bmatrix}x_1\\ x_2\\ x_3\\ \vdots\\ x_{n-1}\\ x_n \end{bmatrix}+
\begin{bmatrix}0 \\ 0 \\ 0 \\ \vdots\\ 0 \\ b_0 \end{bmatrix}u
\dots(30)
\end{matrix} $$

From equation (24) we have
$$ Y(s)=(s^2+7s+2)X_1(s) - - - -\dots(31) $$
From equation (31) and (27) we have
$$ y=x_3+7x_2+2x_1 $$
and so

And the corresponding output equation is given as
$$ y=\begin{bmatrix}1 & 0 & 0 & \dots  & 0 \end{bmatrix}
\begin{bmatrix}x_1 \\ x_2 \\ x_3 \\ \vdots \\ x_{n-1} \\ x_n \end{bmatrix} - - - -\dots(7) $$

![Figure 3](https://selene.hud.ac.uk/u1273400/images/seg_media/c5.PNG)
