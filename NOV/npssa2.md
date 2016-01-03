
### Obtaining a Transfer function from a State Space model

Given the state and output equations
$$ \dot{x}=Ax + Bu - - - -\dots(1) $$
$$ y = Cx + Du - - - - \dots(2) $$

Take the Laplace transform assuming zero initial conditions
$$ sX(s)=AX(s) + BU(s) - - - -\dots(3) $$
$$ Y(s) = CX(s) + DU(s) - - - - \dots(4) $$
Solving for X and introducing an identity matrix for equation (3), we have
$$ (sI - A)X(s)=BU(s) $$
OR
$$ X(s)=(sI - A)^{-1}BU(s) - - - - \dots(5)$$

Substituting equation (5) into equation (4)
$$ Y(s) = C(sI - A)^{-1}BU(s) + DU(s)$$
$$ Y(s) = [C(sI - A)^{-1}B(s) + D]U(s) - - - - \dots(6) $$

Equation (6) is called the transfer function matrix, since it relates the output vector Y(s) to input vector, U(s).

$$ T(s)= \frac{Y(s)}{U(s)} = C(sI - A)^{-1}B(s) + D - - - - \dots(6) $$

#### Example

#### Solution

## State Variable Feedback Control

State variable feedback control (also known as state vector feedback control) occurs when all of the state variable (rather than just the final output) are feed back to the effect of the control of the system.
![Figure 1](https://selene.hud.ac.uk/u1273400/images/seg_media/c3.PNG)
**Figure 1**

Figure 1 Represents a closed loop system whereby the ith state variable sis fed back via a fixed gain h<sub>i</sub>.  The process input u(t) can be represented by
$$ u(t)=r(t)-\begin{bmatrix} h_1 & h_2 & h_3 & h_4 \end{bmatrix}
\begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix} - - - - \dots(1) $$

The matrix H is known as the feedback matrix, and is a "i x n" matrix.  Equation (1) can also be written as
$$ u = r - HX - - - - \dots(2) $$

Let us suppose that "Process 1" shon in Figure 1 can be represent by the following "open loop" state variable equations.
$$ \dot{X}=AX + Bu - - - - \dots(3) $$
and
$$ Y=CX + Du - - - - \dots(4) $$
if we Substitute  equation (2) into (3) we have
$$ \dot{X}=AX + B(r-HX)  $$
Which gives
$$ \dot{X}=AX + Br-BHX  $$
and
$$ \dot{X}=X(A-BH) + Br - - - - \dots(5) $$
By taking the laplace transform of Equation (5) we have that

$$ sX(s)=X(s)(A-BH) + Br(s)  $$
Therefore
$$ Br(s)=sX(s) - X(s)(A-BH)  - - - - \dots(6) $$

To sufficiently resolve an "n x n" matrix an identy matrix, I is introduced to the system, this becomes
$$ Br(s)=sIX(s) - X(s)(A-BH)   $$
Factorizing yields
$$ Br(s)=X(s)(sI - A + BH)   $$
Therefore
$$ X(s)=\frac{Br(s)}{sI - A + BH} - - -  - \dots(7) $$

Taking the Laplace Transform of equation (4) gives
$$ Y(s)=CX(s) + Du(s) - - - - \dots(8) $$
Given that for regular systems D=0 and substituting for X by equation (7) now gives
$$ Y(s)=\frac{CBr(s)}{sI - A + BH}  $$
Therefore
$$ \frac{Y(s)}{r(s)}=\frac{CB}{sI - A + BH} - - -  - \dots(9) $$

Let us suppose the system has a single output of interest y(t) (which is the same as the state variable x<sub>1</sub>(t) as shown in Figure 1.  We may now state that equation (12) represent the closed loop "s" transfer function of a process characterised by the matrices A, B, and C which is controlled via a feedback matrix H.

#### Example 1
A process has an open loop transfer functio G(s) given by
$$ G(s)=\frac{Y(s)}{U(s)}=\frac{100}{(s^2+9s+25)(1+s)} - - - - \dots(10) $$

Convert this 's' transfer function to state variable notation then provide state variable feedback control via matrix H (where H=[h<sub>1</sub>, h<sub>2</sub>, h<sub>3</sub>].  Express the resultant closed loop system as an 's' transfer function.

#### Solution
##### Steps
1. Determine the State Space notation of inputs and outputs
2. State the state space notation for Feedback matrix
3. Perform the state space computation for the closed loop using matrix operations in terms of h

##### Finding the Inverse of a 3 x 3 matrix

Consider the folloing 3 x 3 matrix
$$ Q=\begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix} $$

the "adjoint" of Q is adjQ where
$$ adjQ=\begin{bmatrix} 
 \begin{vmatrix} e & f \\ h & i \end{vmatrix} & 
 -\begin{vmatrix}d & f \\ g & i \end{vmatrix} &
 \begin{vmatrix} e & f \\ h & i \end{vmatrix} \\ 
 -\begin{vmatrix} b & c \\ h & i \end{vmatrix} & 
 \begin{vmatrix}a & c \\ g & i \end{vmatrix} &
 -\begin{vmatrix} a & b \\ g & h \end{vmatrix} \\ 
 \begin{vmatrix} b & c \\ e & f \end{vmatrix} & 
 -\begin{vmatrix}a & c \\ d & f \end{vmatrix} &
 \begin{vmatrix} a & b \\ d & e \end{vmatrix} \\ 
\end{bmatrix}^T $$

Therefore
$$ adjQ=\begin{bmatrix} (ei-hf & -(di-fj) & (dh-eg) \\ -(bi-ch) & (ai-cg) & -(ah-bg) \\ (bf-ce) & -(af-cd) & (ae-bd) \end{bmatrix}^T $$
Therefore
$$ adjQ=\begin{bmatrix} (ei-hf & -(bi-ch) & (bf-ce) \\ -(di-fj) & (ai-cg) &  -(af-cd)\\ (dh-eg) & -(ah-bg) & (ae-bd) \end{bmatrix} - - - -\dots(1)$$

The determinant of Q, detQ or $\Delta Q$ is given by
$$ detQ=a\begin{vmatrix}e & f \\ h & i \end{vmatrix}-a\begin{vmatrix}e & f \\ h & i \end{vmatrix}+a\begin{vmatrix}e & f \\ h & i \end{vmatrix}$$
Therefore
$$ detQ = a(ei-fh)-b(di-fg)+c(dh-eg) - - - - \dots(2) $$
The inverse of matrix Q is given by
$$ Q^{-1}=\frac{adjQ}{detQ} - - - -\dots(3) $$

#### Example 2
For the closed loop system given example 1 above, choose, $h_1, h_2, \text{ and }h_3$ such that there are system poles at $s=-2\pm2j$ and that there is a zero steady state error to a step change in set point r(t).

#### Solution
We start by examining the criteria for zero steady state error to a (unit) step change in set point.
$$ \lim_{t \rightarrow \infty}y(t)= \lim_{s \rightarrow 0}s(\frac{1}{s})\frac{100}{s^3+(10+100h_3)s^2+(34+100h_2)s+(25+100h_1)} - - - -\dots(4)$$  where (1/s) is the step change Laplace transform. Therefore
$$ \lim_{t \rightarrow \infty}y(t)=\frac{100}{(25+100h_1)} $$
Given that  $ \lim_{t \rightarrow \infty}y(t)=1$
$$ \implies \frac{100}{(25+100h_1)}=1 $$
$$ \implies (25+100h_1)=100 $$
$$ \therefore h_1=0.75 - - - -\dots(5) $$

From equations (4) and (5), the denomenator can be written as $s^3+(10+100h_3)s^2+(34+100h_2)s+100$.  With system poles at $s=-2\pm2j$ we may write
$$s^3+(10+100h_3)s^2+(34+100h_2)s+100=(s+2+2j)(s+2-2j)(s+\alpha) - - - -\dots(6)$$
where $\alpha$ is the 3rd system pole.

From equation (6) we have
$$s^3+(10+100h_3)s^2+(34+100h_2)s+100=s^3+(4+\alpha)s^2+(8+\alpha)s+8\alpha - - - -\dots(7)$$
Equating terms in $s^0$ in equation (7) gives
$$ 8\alpha=100 \implies \alpha=12.15 - - - - \dots(8)$$
Equating terms in s in equation (7) and using $\alpha$ derived from equation (8) gives


## Controllability

An open-loop system is said to be controllable if it is possible to change its state from some initial state to some desired equilibrium state, in a finite time by manipulating the system input u(t).

Consider an nth-order open loop system defined by the state equations
$$ \dot{X}=AX + Bu - - - - \dots(1) $$
and
$$ Y=CX + Du - - - - \dots(2) $$

For this system, it is possible to write an "n x n" matrix Sc, knon as the composite matrix defined as
$$ Sc = [B AB A^2B \dots A^{n-1}B] - - - - \dots(3)

For the system to be controllable the determinant of Sc must not be equal to zero i.e. 
$$ Sc \neq 0  \implies Controllable- - - - \dots(4)$$


In many text books the condition for controllability given in equation (4) is expressed "**the necessary and sufficient condition for controllability is that the composite matrix has a rank of n**".

- The rank of matrix Sc is the order of the largest non-singular matrix contained within Sc.  
- The order of a square matrix is the number of rows or number of columns.  
- A singular matrix has a determinant equal to zero

#### Example 3
Consider the system having the state system matrix variables A and B as follows
$$ A=\begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ -25 & -34 & -10 \end{bmatrix} - - - - \dots(5) $$
and
$$ \begin{bmatrix} 0 \\ 0 \\ 100 \end{bmatrix} - - - - \dots(6) $$
Determine if this system is controllable

#### Solution
The composite matrix Sc for this 3rd order system is givem by Sc=[B AB A<sup>2</sup>B] - - - - ...(7)

#### Example 4
Suppose a 3rd order system has a composite matrix Sc as below
$$ Sc=\begin{bmatrix} 1 & 2 & 3 \\ 2 & 3 & 4 \\ 3 & 5 & 7 \end{bmatrix} - - - - \dots(5) $$
Determine if this system is controllable

#### Solution
detSc = 1 x (3 x 7 - 4 x 5) - 2 x (2 x 7 - 4 x 3) + 3 x (2 x 5 - 3 x 3) = 1 - 4 + 3 = 0.

Since detSc=0, the composite matrix is singular and therefore the system is not controllable
