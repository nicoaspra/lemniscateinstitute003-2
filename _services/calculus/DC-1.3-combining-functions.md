---
title: "Combining Functions"
prevcontenturl: ../DC-1.2-function-notation
nextcontenturl: ../DC-1.4-composite-functions
---


Functions expressed in equation form should behave similarly to equations and algebraic expressions. As with equations, functions can also be combined to form new functions by performing basic arithmetic operations such as addition, subtraction, multiplication, and division.

In this section, since we will be combining multiple functions, the notation of functions will be instrumental. By naming functions, we can keep track of the functions we are currently working on.


The sum, difference, product and quotient of two functions $f(x)$ and $g(x)$ are:
{% include tcolorbox.html 
    details= "
    & \text{Sum} 		& 	(f+g)(x) &= f(x)+g(x) 
		\label{eq:sum of functions}\\
	& \text{Difference} 	& 	(f-g)(x) &= f(x)-g(x) 
		\label{eq:diff of functions}\\
	& \text{Product}		& 	(f \cdot g)(x) &= f(x) \cdot g(x) 
		\label{eq:prod of functions}\\
	& \text{Quotient} 	& 	\br{ \frac{f}{g} } \! (x) &=  \frac{f(x)}{g(x)} , \quad where: \, g(x) \neq 0 
		\label{eq:quo of functions}
        "
%} 

	


For example, given two functions $\tcA{f(x)=2x+5}$ and $\tcB{g(x)=3x-4}$, determine $(f+g)(x)$

The notation $(f+g)(x)$ simply means $\tcA{f(x)}+\tcB{g(x)}$, which we can refer from Equation 1. Thus,

$$
\begin{align*}
	(f+g)(x) &= \tcA{f(x)}+\tcB{g(x)} \\
	&= \tcA{(2x+5)}+\tcB{(3x-4)} \quad \tcAal{replace $f(x)$ and $g(x)$} \\
	&= 2x+5+3x-4 \\
	&= 5x+1
\end{align*}
$$

Hence, $(f+g)(x) = 5x+1$





---

$\example{1}$
If $ f(x)=x+2 $ and $ g(x)=x-1 $, find:
**a.** $ (f+g)(x) $, 
**b.** $ (f-g)(x) $,
**c.** $ (g-f)(x) $,
**d.** $ (f \cdot g)(x) $,
**e.** $ \br{ \frac{f}{g} } (x) $,
**f.** $ \br{ \frac{g}{f} } (x) $

{% include solution.html details = "
$\For{a}$ \\
Use Equation 1,

$$
\begin{align*}
	(f+g)(x) &=  f(x)+g(x) \\
	&= (x+2)+(x-1) \\
	&= x+2+x-1 \\
	&= 2x+1		\tagans
\end{align*} 
$$

$\For{b}$ \\
Use Equation 2,

$$
\begin{align*}
	(f-g)(x) &=  f(x)-g(x) \\
	&= (x+2)-(x-1) \\
	&= x+2-x+1 \\
	&= 3		\tagans
\end{align*} 
$$

$\For{c}$ \\
Use Equation 2,

$$
\begin{align*}
	(g-f)(x) &=  g(x)-f(x) \\
	&= (x-1)-(x+2) \\
	&= x-1-x-2 \\
	&= -3	\tagans
\end{align*} 
$$

$\For{d}$ \\
Use Equation 3,

$$
\begin{align*}
	(f \cdot g)(x) &=  f(x) \cdot g(x) \\
	&= (x+2) (x-1) \\
\end{align*} 
$$

Multiply the two binomials using the ``FOIL Method''

$$
\begin{align*}
	&= x^2-x+2x-2 \\
	&= x^2+x-2	\tagans
\end{align*} 
$$

$\For{e}$ \\
Use Equation 4,

$$
\begin{align*}
	\br{ \frac{f}{g} } \! (x) &=  \frac{f(x)}{g(x)} \\
	&= \frac{x+2}{x-1}	\tagans
\end{align*}  
$$

$\For{f}$ \\
Use Equation 4,

$$
\begin{align*}
	\br{ \frac{g}{f} } \! (x) &=  \frac{g(x)}{f(x)} \\
	&= \frac{x-1}{x+2}	\tagans
\end{align*} 
$$
	
"%}
	



---
$\example{2}$ \\
If $ f(x)=x^2+2x $ and $ g(x)=x+1 $, find:
**a.** $ (f+g)(3) $, 	
**b.** $ (f-g)(5) $,	
**c.** $ (g-f)(-2) $,	
**d.** $ (f \cdot g)\br{ \frac{1}{3} } $, 
**e.** $ \br{ \frac{f}{g} } (4) $, 	
**f.** $ \br{ \frac{g}{f} } \br{ -\frac{1}{2} } $	
	
	
{% include solution.html details = "
$\For{a}$ \\
Use Equation 1,

$$
\begin{align*}
	(f+g)(x) &= f(x)+g(x)\\
	&= (x^2+2x)+(x+1)
\end{align*}
$$

Replace $x$ with 3,

$$
\begin{align*}
	(f+g)(3) &= \left[ (3)^2+2(3) \right]+[(3)+1] \\
	&= 9+6+3+1\\
	&= 19	\tagans
\end{align*}
$$

$\For{b}$ \\
Replace $x$ with 5,

$$
\begin{align*}
	(f-g)(5) &=  f(5)-g(5) \\
	&= \left[ (5)^2+2(5) \right]-[(5)+1] \\
	&= 25+10-5-1\\
	&= 29	\tagans
\end{align*}
$$

$\For{c}$ \\
Replace $x$ with $-2$,

$$
\begin{align*}
	(g-f)(-2) &=  g(-2)-f(-2) \\
	&= [(-2)+1] - \left[ (-2)^2+2(-2) \right] \\
	&= -2+1-(4-4)\\
	&= -1	\tagans
\end{align*}
$$


$\For{d}$ \\
Replace $x$ with $\frac13$,

$$
\begin{align*}
	(f \cdot g)\br{ \frac{1}{3} } &=  f\br{ \frac{1}{3} } \cdot g\br{ \frac{1}{3} } \\
	&= \left[ \br{ \frac{1}{3} }^2+2\br{ \frac{1}{3} } \right]  \left[ \br{ \frac{1}{3} }+1 \right] \\
	&= \br{ \frac{1}{9}+\frac{2}{3} } \br{ \frac{1}{3}+\frac{3}{3} }\\
	&= \br{ \frac{1}{9}+\frac{6}{9} } \br{ \frac{1}{3}+\frac{3}{3} }\\
	&= \br{ \frac{7}{9} } \br{ \frac{4}{3} }\\
 	&= \frac{28}{27}	\tagans
\end{align*}
$$

$\For{c}$ \\
Replace $x$ with $4$,

$$
\begin{align*}
	\br{ \frac{f}{g} } (4) &=  \frac{f(4)}{g(4)} \\
	&= \frac{(4)^2+2(4)}{(4)+1} \\
	&= \frac{24}{5}
\end{align*}
$$


$\For{c}$ \\
Replace $x$ with $-\frac12$,

$$
\begin{align*}
	\br{ \frac{g}{f} } \! \br{ -\frac{1}{2} } &=  \frac{g\br{ -\frac{1}{2} }}{f\br{ -\frac{1}{2} }} \\
	&= \frac{ \br{ -\frac{1}{2} }+1}{ \br{ -\frac{1}{2} }^2+2\br{ -\frac{1}{2} } } \\
	&= \frac{\frac{1}{2}}{\frac{1}{4}-1} \\
	&= \frac{\frac{1}{2}}{-\frac{3}{4}} \\
	&= \br{ \frac{1}{2} } \br{ -\frac{4}{3} } \\
	&= -\frac{2}{3}		\tagans
\end{align*}
$$

"%}