
### Cross Correlation
*Consider a system with two sensors from which the outputs are x(t) and y(t).  Suppost that y(t) is a delayed version of x(t).  Suppose also that y(t) contains some random changes when compared to x(t).  If it is required to estimate the mean time delay between y(t) and x(t) then the statistical signal processing technique known as cross correlation can be used*.

*The use of cross correlation can be illustrated by considerating a multiphase flow meter used to measure gas velocity in the bubbly flow regime.  As the random pattern of bubbles (in water) passes the front sensor, variation in the mixture electrical resistances give rise to the output signal x(t).  As the bubbles move upwards, turbulence within the flow causes the bubble pattern to change and so the signal y(t) from the rear sensor is similar to, but not entirely identical, to a delayed version of x(t)*  The block diagram below illustrates the example setup.  Thus in the diagram below $ v_2=(\frac{R_x}{R_1})v_1 $.

![Circutry for meauring fluid resistance (separate circuits required for front and rear positions)](https://selene.hud.ac.uk/u1273400/images/seg_media/xcp.PNG)

*By cross-correlating signals x(t) and y(t), a function $ R_{xy}(\tau) $ with a well defined peak is obtained.  The time delay $ \tau_p $ corresponding to the peak of the cross correlation function represents the mean time delay betwen y(t) and x(t).  Thus  $ \tau_p $  represents the mean transit time for a given pattern of bubbles between the front and rear sensors.  If the separation of the front and rear sensors is L, then the mean gas bubble velocity is v<sub>b</sub> is given by
$$ V_b=\frac{L}{\tau_p}  - - - - (1)$$
and flow rate will be Q=VA*.

*The mathematical definition of cross correlation function $ R_{xy}(\tau) $ for two signals is x(t) and y(t) is *
$$ R_{xy}(\tau) = \frac{1}{T}\int_{t=0}^{t=T}{x(t)y(t+\tau)dt} - - - - (2) $$

*For sampled signals, where N samples of x(t) are taken with a sampling interval $\delta t$ and N samples of y(t) are taken with a sampling interval $\delta t$ (Note the nth sample of x(t) is asumed to be taken at precisely the same time as the nth sample of y(t)) equation (2) can be rewritten as*:

$$ R_{xy}(\tau) = R_{xy}(n\delta{t}) = \frac{1}{N}\sum_{i=1}^{i=N-n}{x_i y_{i+n}} - - - - (3) $$

#### Example 1
*In a wallpaper factory, the  speed of the wallpaper as it moves betwen rollers is measured with the aid of two optic sensors.  The separation of the optic sensors is 10cm.  Twenty samples of the signal x(t) from the front of the sensor and the signal y(t) from the rear sensor are taken using a sampling interval of 10ms.  These samples are shown below.  Determine the speed of the wall paper betwen the  rollers: x=-4 -17 1 3 -11 12 12 0 3 2 -2 7 -6 22 -1 1 11 -1 ;  y = 7 -7 -1 -9 -4 -6 -13 5 6 -5 15 18 -6 3 1 -10 9 -11 29 -5
(ans= 2ms<sup>-1</sup>)*

*A computationally very efficient method for calculating cross correlation functions arises from the fact that*
$$ R_{xy}=IDFT\{X_k*Y_k\} - - - - .(4) $$

*where $Y_k$ is the DFT of sampled signal y(t), $x_k^*$ is the complete conjugate of sampled x(t) and IDFT represents "inverse discrete fourier transform".  To implement equation (4) in MATLAB, the 'xcorr' function is used.  The matlab 'xcorr' function requires that x(t) and y(t) are both sampled N times over a time period T.  The two time series $x_r$ and  $y_r$ (r=0,N-1).  The sampling interval between consecutive points in  $x_r$ (and in  $y_r$) is  $\delta{t}$ where  $\delta{t}=\frac{T}{N}$.  Note that because use is made of DFTs N must be of the form  $N=2^n$; where n is an integer. In the following matlab code  $x_r$ and  $y_r$ has $\frac{1}{512}=0.00195 seconds$ as the sampling interval.  Note that the time interval between points in  $R_xy$ is the same as the original sampling interval  $\delta t$ (where  $\delta t=T/N$

```matlab
hold off
T=1;
N=512;
t=linspace(0,T,N);
x=5*randn(size(t));
for j=1:20
    y(j)=0;
end

# first plot
plot(t,x,'green');
hold on
plot(t,y,'red');
axis([0.1,0.2,-20,20]);
title('x is green y [delayed signal] is red')
a=input('Hit enter to continue');
hold off

# second plot
plot(t,x,'green');
hold on
plot(t,y,'red');
axis([0.1,0.5,-20,20]);
title('x is green y [delayed signal] is red')
a=input('Hit enter to continue');
hold off

# cross correlation plot
c=xcorr(x,y);
t=linspace(-T,T,2*N-1);
plot(t,c)
xlabel('t (seconds)')
ylabel('cross correlation function')

```



```python

```
