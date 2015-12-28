

## SEQUENCES AND SERIES

### Objectives
1. Manipulate arithmetic and geometric series
2. Manipulate series of powers of natural numbers
3. Determine the limiting values of arithmetic and geometric series
4. Determine the limiting values of simple indeterminate forms
5. Apply various convergence tests to infinite series
6. Distinguish between absolute and conditional convergence

### Arithmetic Series
For an arithmetic series a+(a+d)+(a+2d)+(a+3d)+...
$$ \begin{aligned}
 u_n=a+(n-1)d  & & S_n=\frac{n}{2}[2a+(n-1)d]
 \end{aligned}   $$

### Geometric Series
For a geometric series $ a+ar+ar^2+ar^3+\dots $
$$ \begin{aligned}
u_n=ar^{n-1}  &  &  S_n=\frac{a(1-r^n)}{1-r}
 \end{aligned} $$

### Powers of natural numbers

$$ 
\begin{aligned}
\sum_{r=1}^n{r } & =\frac{n(n+1)}{2}\\   
\sum_{r=1}^n{r^2} & =\frac{n(n+1)(2n+1)}{6} \\   
\sum_{r=1}^n{r^3}  & =\big\{\frac{n(n+1)}{2}\big\}^2
\end{aligned} 
$$


### Test for Convergence
Given an infinite series  $ S_n=u_1+u_2+u_3+\dots+u_n+\dots $
[comment]: <> (If lim┬(n→∞)⁡〖u_n 〗=0 the series may be convergent)
[comment]: <> (If lim┬(n→∞)⁡〖u_n 〗≠0 the series may be convergent)
- If $\lim_{n\rightarrow\infty}{S_n=0}$ the series may be convergent
- If $\lim_{n\rightarrow\infty}{S_n=}$  not a definite value, series is divergent.

#### COMPARISON TEST
If series is comparable with
$$ \frac{1}{1^p}+\frac{1}{2^p} +\frac{1}{3^p} +\frac{1}{4^p} +⋯+\frac{1}{n^p} = \sum_{n=1}^\infty{\frac{1}{n^p}} $$ for p>1 then the series converges else if p≤1 the series diverges

#### D’ALEMBERT’S RATIO TEST
[comment]: <> (If lim┬(n→∞)⁡|u_(n+1)/u_n |<1 the series converges)
[comment]: <> (If lim┬(n→∞)⁡|u_(n+1)/u_n |>1 the series diverges)
[comment]: <> (If lim┬(n→∞)⁡|u_(n+1)/u_n |=1 the test cannot be applied)
- If $\lim_{n\rightarrow\infty}{\frac{u_{n+1}}{u_n}}<1, $ series converges
- If $\lim_{n\rightarrow\infty}{\frac{u_{n+1}}{u_n}}>1, $ series diverges
- If $\lim_{n\rightarrow\infty}{\frac{u_{n+1}}{u_n}}=1, $  inconclusive

#### Generally
- If $ \sum{|u_n|} $ converges, $ \sum{u_n} $
- If $ \sum{|u_n|} $ diverges, but $ \sum{u_n} $ converges, then  $ \sum{u_n} $ is conditionally convergent

#### Example 1
Find the range of values of x for which the series is convergent or divergent $$ 1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\frac{1}{5}+\frac{1}{6}+\dots $$


#### Solution
Because the series does not tend to a definite value it diverges

Proof:
because 
$$ \left\{\frac{1}{3}+\frac{1}{4}\right\}>\left\{\frac{1}{4}+\frac{1}{4}\right\}=\frac{1}{2} $$

and
$$ \left\{\frac{1}{5}+\frac{1}{6}+\frac{1}{7}+\frac{1}{8}\right\}>\left\{\frac{1}{8}+\frac{1}{8}+\frac{1}{8}+\frac{1}{2}\right\}=\frac{1}{2} $$

So if 
$$ S_n>1+\frac{1}{2}+\frac{1}{2}+\frac{1}{2}+\frac{1}{2}+\frac{1}{2}+\dots $$
$ \therefore $ $ S_\infty=\infty $

#### Example 
Deterimine if the folowing series is convergent or divergent $$ 1+\frac{1}{3}+\frac{1}{9}+\frac{1}{27}+\dots $$


#### Solution
For a G.P.,  $ S_n=\frac{a-r^n}{1-r} $, so in this case since a=1 and $r=\frac{1}{3} $, we have
$$ 
\begin{aligned}
S_n=\frac{1\left(1-\frac{1}{3^n}\right)}{1-\frac{1}{3}}  
=\frac{1-\frac{1}{3^n}}{\frac{2}{3}}=\frac{3}{2}\left(1-\frac{1}{3^n}\right) \\ 
\therefore\text{ as n}\rightarrow\infty, \frac{1}{3^n}\rightarrow 0\text{ } \therefore \lim_{n\rightarrow\infty}S_n=\frac{3}{2}
\end{aligned}
$$ 
Therefore the series converges because S<sub>n</sub> tends to a definite value

#### Example 
Test if the series $$ 1+\frac{1}{2^2}+\frac{1}{3^3}+\frac{1}{4^4}+\dots+\frac{1}{n^n}+\dots $$ is convergent or divergent


#### Solution
Compare with an appropriate series that is known to converge such as
$$ 1+\frac{1}{2^2}+\frac{1}{2^3}+\frac{1}{2^4}+\dots+\frac{1}{2^n}+\dots $$
Since $ \frac{1}{3^3}<\frac{1}{2^3};\frac{1}{4^4}<\frac{1}{2^4} $ and so on for all other further analogous terms then therefore the series also converges

#### Example 
Test if the following series is convergent or divergent $$ 1+\frac{3}{2}+\frac{5}{2^2}+\frac{7}{2^3}+\dots $$


#### Solution
If we look for a pattern of the numerator/denomenator we see that the nth term numerator is $ 2n-1  $ and the nth term denomenator is $ 2^{n-1} $.  Therefore the nth and n+1 term is respectively given by
$$ \begin{aligned}
u_n & =\frac{2n-1}{2^{n-1}} \\ 
u_{n+1} & = \frac{2(n+1)-1}{2^{(n+1)-1}} =\frac{2n+1}{2^n} 
\end{aligned} $$
$$
\therefore \frac{u_{n+1}}{u_n}=\frac{2n+1}{2^n}.\frac{2^{n-1}}{2n-1}=\frac{1}{2}.\frac{2n+1}{2n-1}
$$

We now have to find the limiting value of this ratio as $ n \rightarrow \infty $. Since the top and bottom values have the independent variable we therefore divide through by the independent variable and substitute infinity.

$$
\therefore \lim_{n\rightarrow\infty}\frac{u_{n+1}}{u_n}= \lim_{n\rightarrow\infty}\frac{1}{2}.\frac{2n+1}{2n-1}=
\lim_{n\rightarrow\infty}\frac{1}{2}.\frac{2+\frac{1}{n}}{2-\frac{1}{n}}=\frac{1}{2}.\frac{2+0}{2-0}=\frac{1}{2}
$$

Because $ \lim_{n\rightarrow\infty}\frac{u_{n+1}}{u_n}<1  $ we know that the series is convergent

#### Example 
Find the range of values of x for which the series is convergent or divergent $$ 1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\frac{x^4}{4!}+\dots $$


#### Solution


### MACLAURIN’S SERIES

To establish the series, we represent the process of the previous example, but work with a general function, f(x), instead of sin x.  The first derivative of f(x) will be denoted by general f’(x); the second by f’’(x) and the third by f’’’(x); and so on. So let
f(x)=a+bx+cx^2+dx^3+ex^4+fx^5+..
Put x=0.  Then f(0)=a+0+0+0+0+..
i.e. a =  value of the function with x put equal to 0; a=f(0)
Differentiate
f^'(x) =b+c.2x+d.3x^2+e.4x^3+f.5x^4+..
Put x=0. Therefore f’(x)=b+0+0+0+0+.. therefore b=f’(0)
Differentiate
f(x)=c.2.1+d.3.2x+e.4.3x^2+f.5.4x^3+..
Put x=0.  Therefore f’’(0)=c.2! + 0 + 0 + …  Therefore c=f’’(0)/2!  Similarly d = f’’’(0)/3! And e=f’’’’(0)/4!
Therefore the Maclaurin’s series is given as
f(x)=f(0)+xf^' (0)+x^2/2! f^'' (0)+x^3/3! f^''' (0)+x^4/4! f^iv (0)+..



```R

```
