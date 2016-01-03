
## STATE VARIABLE ANALYSIS
### Dynamic Models of Mechanical Systems

### Translational motion
$$ F=ma - - - - \dots(1)$$
where
- F = the vector sum of all forces applied to each body in a system, Newtons (N) or pounds (lb)
- a = The vector acceleration of each body with respect to an internal reference frame (i.e. that is neither accelerating nor rotating with respect to the stars) often called inertial acceleration m/sec<sup>2</sup> or ft/sec<sup>2</sup>
- m = mass of the body, kg or slug.

#### Example 1: Cruise Control Model
1. Write the equations of motion for the speed and forward motion of the car shown in figure 1 assuming that the engine imparts a force u as shown.  Take the Laplace transform of the resulting differential equation and find the transfer function between the input u and output v.
2. Use MATLAB to find the response of the velocity of the car for the case in which the input jumps from being u=0 at time t=0 to a constant u=500N thereafter.  Assume that the car mass m is 1000 kg and viscous drag coefficient, b=50 N-sec/m

![Figure 1](https://selene.hud.ac.uk/u1273400/images/seg_media/d1.PNG)
**Figure 1** Use of free-body diagram in applying Newton's Law

#### Solution
1. Equations of motion:  F

### State Space Analysis Objectives
1. Development of state-variable equations from block diagrams
2. Solve for dynamic response using hand and computer analysis
3. Control Design Via State Space modelling
4. Integral control in state space
5. Advnaced methods \*

#### Design Steps
1. Select closed loop pole locations and develop the control law for the closed-loop system that corresponds to satisfactory dynamic response
2. Design an estimator
3. Combine the control law and estimator
4. Introduce the reference input

### System Description in State-Space
The motion of any finite dynamic system can be expressed as a set of first order ODEs. This is often referred to as the state-variable representation.  For example, the use of Newton's law and the free-body diagram typically lead to a 2nd order ODE - that is having a second derivitive.

### Development of state-variable equations

Let us now suppose that there are r system outputs which are of interest to us.  These outputs are y1, y2, .. yr
	The outputs can be defined in terms of the n state variables and the m inputs by the r simultaneous equations .
	These r simultaneous equations are written in the (compact matrix form below
	Y = C x + D u 	(2)
	Matrix C is the system output matrix (containing constants) and r x n ( r rows and n columns)
	Matrix D is the direct feed through matrix and is r x m (r rows and m columns). Matrix D contains constants.
	Equation (2) is the MATRIX OUTPUT EQUATION
	For any system, the outputs contained in Y can be evaluated for given inputs (u1(t)..um(t)) PROVIDED THAT A, B, C, and D are all known (and fully defined).
	A package such as matlab uses the input to the matrices A, B, C, D and for the system thus defined, determine the system outputs y1, y2, .. yr for given system inputs u1(t)..um(t).
	Example
 
	Mass = M
	Spring stiffness= K
	Damping constant f
	The system is a 2nd order, that is to say, a second order differential equation relates the displacement to the applied force P(t) as follows:
	P(t)=M (d^2 x_1)/(dt^2 )+f (dx_1)/dt+kx_1 .	(3)
	There is a single input P(t) to the system.
	Since the system is 2nd order, we require 2 stable state variables as described above.  The best choices for these state variables are x1 (displacement of mass) and x2 (velocity of mass) – because we can write two first order differential equations in terms of these variables as shown below (if we had chosen acceleration of mass as a stable variable, we would not have been able to write an expression for dx3/dt).
	We know that velocity is the derivative of displacement with respect to time therefore
	x_2=(dx_1)/dt .	(4)
	From equation (4)
	(dx_2)/dt=(d^2 x_1)/(dt^2 ) .	(5)
	Substituting (4) and (5) into (3) gives
	P(t)=M (dx_2)/dt+fx_2+kx_1 .
	And so
	(dx_2)/dt=(-f)/M x_2-k/M x_1+(P(t))/M.	(6)
	And  (dx_1)/dt=x_2. From (4)
	Equations (4) and (6) are our two required 1st order differential equations in terms of the (one) input and the two state variables.
	Equations (6) and (4) can be written in matrix notation to provide the system matrix A and the input matrix B as follows
	■([■((dx_2)/dt@(dx_1)/dt)]@x ̇ )=■([■(0&1@-k/M&(-f)/M)]@■(@A))■([■(x_1@x_2 )]@■(@x))+■([■(0@1/M)]@■(@B))■([P(t)]@■(@@u))	(7)
	Let us now suppose that the only output in which we are interested is the displacement x1 of the mass.  Accordingly, we can write down the following matrix output equation with the following output  matrix C and direct feed through matrix D
	■(y_1=@@Y=)■([■(1&0)]@@C)■([■(x_1@x_2 )]@x)+■([0]&[P(t)]@&@D&u)	(8)
	Note that if we had only been interested in the velocity x2 as the system output, our matrix would have been
	■(y_1=@@Y=)■([■(0&1)]@@C)■([■(x_1@x_2 )]@x)+■([0]&[P(t)]@&@D&u)	(9)
	If we let M=1kg, k=1000kgs-2 and f=12.65kgs-1 our matrices A, B, C and D are defined as follows (from equations (7) and (8))
	A= [■(0&1@-1000&-12.65)] 	(10)
	B= [■(0@1)] 	(11)
	C= [■(1&0)] 	(12) displacement is the required output
	D = [0]	(13)

	Let us now supposw we wish to subject the system shown in fig 1 and defined by equations (10) – (13) to a step input such that the value of P(t) changes from 0 to 150N at t=0. We wish to tsee the resultant variation in displacement x1 with time.
MATLAB COMMANDS
>>g=ss(A,B,C,D); %A,B,C,D are matrices defined above
>>step(150*g);
>>h=tf(g); % to obtain the transfer function.
	If we had wanted to investigate how the velocity of the mass changed with time as a result of the step change in the applied force then equations (7) and (9) would change as follows
	A= [■(0&1@-1000&-12.65)] 	(10)
	B= [■(0@1)] 	(11)
	C= [■(0&1)] 	(12) velocity is the required output
	D = [0]	(13)

	It should be apparent that, in order to find the variation of velocity x2 with time as a result of the step change in P(t) from 0 to 150N at t=0, it is only necessary to change a single line of the code.

EXPRESSING TRANSFER FUNCTION IN STATE VARIABLE NOTATION
	It is sometimes required to express the transfer function of a system in state variable notation.  This may be necessary if, for example, we wish to control a system with a known transfer function using ‘state variable feedback control’ 
	The method used to convert a transfer function to state variable notation depends on whether or not there is a polynomial in s in the numerator, as illustrated by the following examples.
METHOD 1:  NO POLYNOMIAL IN s IN THE NUMERATOR
	For this case, for an nth order system, we choose the state variables x1 and xn as the system output and the (n-1) derivatives of the system output.
	Note the “order” of the system is equal to the highest exponent of s in the transfer function of the 
	.X ̇=Ax+Bu.	(1)
	(Matrix state equation
	Y = C x + D u 	(2)
 OBTAINING ‘s’ TRANSFER FUNCTIONS FROM THE MATRIX EQUATION AND THE MATRIX OUTPUT EQUATION (obtaining ‘s’ transfer function from state  variable equations)
	When using state variable feedback control methods (in future lectures) it is sometimes necessary to convert state variable equations to transfer functions.  The procedure for doing this is outlined below
	.X ̇=Ax+Bu.	(1)
	(Matrix state equation
	Y = C x + D u 	(2)
	 (matrix output equation)
	If all of the state variables are equal to zero at t=0 (e.g. the state variables may be perturbation variables) then by taking Laplace Transform of equation (1) we have
	sX(s) = Ax(s) + Bu(s) 	(3)
	Taking Laplace Transform of equation (2) gives
	Y(s) = Cx(s) + Du(s) 	(4)
	From equation (3) we have
	sX(s) – Ax(s) = Bu(s) 	(5)
	For an nth order system, matrix A is “n x n” and so in order to evaluate the l.h.s. of equation (5) we must introduce an “n x n” unit matrix denoted I. Equation (5) can then be expressed as:
	(sI – A)x(s) = Bu(s) 	(6)
	Multiplication of both sides of equation (6) by (sI-A)-1 (where the exponent -1 denotes “inverse matrix”) gives
	(sI-A)-1 (sI – A)x(s) = (sI-A)-1 Bu(s) or
	x(s) = (sI-A)-1 Bu(s) 	(7)
	substituting equation (7) into equation (4) gives 
	Y(s) = C(sI-A)-1 Bu(s)  + Du(s) 	(8)
	Equation (8) may be written as
	G(s)=(Y(s))/(U(s))=C(sI-A)^(-1) Bu(s)+Du(s) 	(9)
	Matrix G(s) is shown as the “matrix transfer function”.  It relates the Laplace transforms of the systems outputs (contained within Y(s)) to the Laplace transforms of the systems inputs (contained in u(s))
	We know that the number of outputs “r” in Y corresponds to the number of state variables of interest that we wish to consider as outputs.
	Consequently, G(s) contains “r” elements, each element corresponding to a transfer function relating the Laplace transform of a specific output (state variable) to the Laplace Transform of the system inputs.
	Note C is “r x n”, (sI-A)-1 is “n x n” and b is “n x 1” for a single input.  Therefore C(sI-A)-1B is “r x 1” for a single input.
Example
	Let us consider the example of the “spring-mass-damper” system.
	The matrix state equation can be written as:
	■([■((dx_2)/dt@(dx_1)/dt)]@x ̇ )=■([■(0&1@-k/M&(-f)/M)]@■(@A))■([■(x_1@x_2 )]@■(@x))+■([■(0@1/M)]@■(@B))■([P(t)]@■(@@u))	(10)
	We will use a slightly different output equation because we are now considering both x1 (displacement) and x2 (velocity) as outputs of interest
	■([■(y_1@y_2 )]=@Y=)■([■(1&0@0&1)]@C)■([■(x_1@x_2 )]@x)+■([■(0@0)]@D)■([P(t)]@@u)	(11)
	With reference to equation (6), equation (10) can be written in the form (sI-A)x(s)=Bu(s) as follows
	{s[■(1&0@0&1)]-[■(0&1@-k/M&(-f)/M)]}x(s)=[■(0@1/M)][P(s)]
	or
	{[■(s&0@0&s)]-[■(0&1@-k/M&(-f)/M)]}x(s)=[■(0@1/M)][P(s)]
	Therefore 
	{[■(s&-1@k/M&s+f/M)]}x(s)=[■(0@1/M)][P(s)]	(12)
	Thus  sI-A= [■(s&-1@k/M&s+f/M)] 	(13)
	Note for a 2x2 matrix Q of the form Q= [■(q_1&q_2@q_3&q_4 )] 
	Then  Q^(-1)=  1/(q_1 q_4-q_2 q_3 ) [■(q_4&〖-q〗_2@〖-q〗_3&q_1 )]
	And where the quantity q1q4-q2q3 is the determinant of the matrix, which is denoted by Δ
	From equation (13)
	Thus  (sI-A)^(-1)=  1/∆ [■(s+f⁄M&1@(-k)⁄M&s)] 	(14)
	Where Δ=s(s+f/M)+k/M	(15)
	With reference to equation (9) and using equations (14) and (11)
	.  〖C(sI-A)〗^(-1)= [■(1&0@0&1)].1/∆ [■(s+f⁄M&1@(-k)⁄M&s)] 
	Therefore
	.  〖C(sI-A)〗^(-1)= [■(1&0@0&1)].1/∆ [■(s+f⁄M&1@(-k)⁄M&s)] 	(16)
	With reference to equation (9) and using equations (16) and (10)
	.  〖C(sI-A)〗^(-1) B=  1/∆ [■(s+f⁄M&1@(-k)⁄M&s)][■(0@1/M)]  
	Therefore 
	.  〖C(sI-A)〗^(-1) B=  1/∆ [■(1/M@s/M)] 	(17)
	With reference to equation (9), using equation (17) and using the fact that D=[■(0@0)] in equation (11) we have:
	G(s)=(Y(s))/(U(s))=C(sI-A)^(-1) Bu(s)+Du(s)=  1/∆ [■(1/M@s/M)] 	(18)
	and since, from equation (15) Δ=s(s+f/M)+k/M
	we have:
	G(s)=(Y(s))/(U(s))=  1/(s^2+s f/M+k/M) [■(1/M@s/M)] 	(18)
	Therefore 
	G(s)= [■(1/(s^2+s f/M+k/M)@s/(s^2+s f/M+k/M))] 	(19)
	In this example the input u(s) is simply the applied force P(s).  The top element in G(s) is therefore the transfer function relating the Laplace Transform of output y1(s) to P(s).  From equation (11) we know that y1(s) is equivalent to the Laplace Transform of the state variable x1 (displacement)
	Therefore 
	(x_1 (s))/(P(s))=  1/(〖Ms〗^2+sf+k) 	(20)
	Similarly, the lower element in G(s) is the transfer function relating the Laplace Transform of state variable x2 (velocity) to P(s).
	Therefore
	(x_1 (s))/(P(s))=  s/(〖Ms〗^2+sf+k) 	(20)
