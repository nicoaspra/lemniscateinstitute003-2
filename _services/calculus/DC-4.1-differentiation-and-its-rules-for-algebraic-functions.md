---
title: "Differentiation and its Rules for Algebraic Functions"
prevcontenturl: ../DC-3.5-average-and-instantaneous-velocity
nextcontenturl: ../DC-4.2-higher-order-derivatives
---


Differentiation is the process of solving for the derivative of a function. In the [previous chapter](../DC-3.1-introduction-to-derivatives), we have differentiated functions by the *definition of the derivative*. It is a long and tedious process, and it is easy to make mistakes. However, there are available rules that we could follow so that we can simplify the process and differentiate functions without having to apply the definition of the derivative every time. Moreover, this method will also drastically reduce the amount of time evaluating problems that involve derivatives.


{% include youtube.html 
    id="njmatKZGn0o" 
%}


## Differentiation Rules for Algebraic Functions
For the following rules of differentiation, let $c$ be as any constant, $x$ as a variable, and $u$ and $v$ be as a function of $x$.

$\rule{1}{Derivative of a Constant}$	\\
The derivative of any constant is equal to zero.
{% include tcolorbox.html
    details = "
		\ddx (c) = 0
    "
%}


$\rule{2}{Power Rule}$\\
The derivative of a power of a variable is equal to the product of the exponent and the power of a variable with the exponent diminished by 1, given that $n \neq 0$.
{% include tcolorbox.html
    details = "
		\frac{d}{dx} (x^n) = n \cdot x^{n-1}
    "
%}


	
$\rule{3}{Constant Multiple Rule}$\\
The derivative of the product of a constant and a function is equal to the product of the constant and the derivative of the function.
{% include tcolorbox.html
    details = "
		\frac{d}{dx} (cu) = c \frac{du}{dx}
    "
%}



$\rule{4}{Sum Rule}$\\
The derivative of the sum of two functions is equal to the sum of their derivatives.
{% include tcolorbox.html
    details = "
		\frac{d}{dx} (u+v) = \frac{du}{dx} + \frac{dv}{dx}
    "
%}


$\rule{5}{Product Rule}$\\
The derivative of the product of two functions is equal to the sum of the products of each function and the derivative of the other.
{% include tcolorbox.html
    details = "
		\ddx(uv) = u \frac{dv}{dx} + v \frac{du}{dx}
    "
%}


$\rule{6}{Quotient Rule}$\\
The derivative of the quotient of two functions is equal to the product of the divisor and derivative of the dividend minus the product of the dividend and the derivative of the divisor, and the difference is divided by the square of the divisor.
{% include tcolorbox.html
    details = "
		\ddx\br{\frac{u}{v}} = \frac{v\dfrac{du}{dx} - u\dfrac{dv}{dx}}{v^2}
    "
%}





---
$\example{1}$
Differentiate the function $y = \sqrt{5}$

{% capture include_content %}
Since $\sqrt{5}$ is a constant, its derivative is equal to zero.

$$
\begin{align*}
	\ddx{(y)} &= \ddx\br{ \sqrt{5} }  \quad \tcA{\ddx (c) = 0} \\
	\dydx &= 0	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}




---
$\example{2}$
Differentiate the function $y=7x^3$

{% capture include_content %}
Apply the Power Rule. Multiply the term by the exponent 3, then subtract 1 to the exponent,
$$
\begin{align*}
	\ddx{(y)} &= \ddx\br{ 7x^3 } \\
	\dydx &= 3\cdot 7x^{3-1}   \quad \tcA{\ddx (x^n) = n\cdot x^{n-1}} \\
	&= 21x^2		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}





---
$\example{3}$
Differentiate the function $y=5x^2+3x$

{% capture include_content %}
Apply the Sum Rule along with the Power Rule,
$$
\begin{align*}
	\ddx{(y)} &= \ddx\br{ 5x^2+3x } \\
	\dydx &= \ddx(5x^2)+\ddx(3x) \qquad \tcA{\frac{d}{dx} (u+v) = \frac{du}{dx} + \frac{dv}{dx}} \\
	&= (2)5x^{2-1} + (1)3x^{1-1} \\
	&= 10x^1 + 3x^0 \\
	&= 10x+3		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}



---
$\example{4}$
Differentiate the function $y = x^3+7x^{-6}-2x^5+\frac{\pi}{3}$

{% capture include_content %}
The Sum Rule also applies to subtraction. In this case, the function that is to be differentiated has four terms. Thus, the function's derivative can be obtained by differentiating each term separately.

$$
\begin{align*}
	\ddx{(y)} &= \ddx\br{ x^3+7x^{-6}-2x^5+\frac{\pi}{3} } \\
	\dydx &= \ddx(x^3)+\ddx(7x^{-6})-\ddx(2x^5)+\ddx\br{ \frac{\pi}{3} } \\%\quad \text{\tcA{$\pi$ is a constant}}\\
	&= 3x^{3-1}+(-6)7x^{-6-1}-(5)2x^{5-1}+0 \\
	&= 3x^2-42x^{-7}-10x^4 \\
	&= 3x^2-\frac{42}{x^7}-10x^4		\tagans
\end{align*}
$$


{% endcapture %}
{% include solution.html details = include_content %}



---
$\example{5}$
Differentiate the function $w = \frac{1}{t^2}-\frac{1}{t^5}$

{% capture include_content %}
$$
\begin{align*}
	\frac{d}{dt}(w) &= \frac{d}{dt}\br{ \frac{1}{t^2}-\frac{1}{t^5} } \\
	\frac{dw}{dt} &= \frac{d}{dt}(t^{-2})-\frac{d}{dt}(t^{-5})	\qquad \tcA{\frac{1}{x^n}=x^{-n}} \\
	&= (-2)t^{-2-1}-(-5)t^{-5-1} \\
	&= -2t^{-3}+5t^{-6} \\
	&= -\frac{2}{t^3}+\frac{5}{t^6}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}





---
$\example{6}$
Differentiate the function $x = 2\sqrt[3]{y}-\frac{5}{y^{1/2}}$

{% capture include_content %}
Express the radical as a power with a rational exponent,
$$
\begin{align*}
	\frac{d}{dy}(x) &= \frac{d}{dy}\br{ 2\sqrt[3]{y}-\frac{5}{y^{1/2}} } \\
	\frac{dx}{dy} &= \frac{d}{dy}(2y^{1/3})-\frac{d}{dy}(5y^{-1/2})	\qquad \tcA{\sqrt[n]{x}=x^{1/n} } \\
	&= \br{\frac{1}{3}} 2y^{\frac{1}{3}-1} - \br{-\frac{1}{2}} 5y^{-\frac{1}{2}-1} \\
	&=  \frac{2}{3} y^{\frac{1}{3}-\frac{3}{3} } + \frac{5}{2} y^{-\frac{1}{2}-\frac{2}{2}} \\
	&=  \frac{2}{3} y^{-\frac{2}{3} } + \frac{5}{2} y^{-\frac{3}{2}} \\
	&=  \frac{2}{3y^\frac{2}{3}} + \frac{5}{2y^\frac{3}{2}} 	
		\quad \text{or} \quad
		\frac{2}{3\sqrt[3]{y^2}} + \frac{5}{2\sqrt{y^3}} \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}



---
$\example{7}$
Determine the slope of the function $y=(x^2+1)(3x-2)$ at $(1,2)$

{% capture include_content %}
Apply the Product Rule,
$$
\begin{align*}
	\ddx{(y)} &= \ddx\brk{ (x^2+1)(3x-2) } \\
	% \dydx &= \ubrace{(x^2+1)}{$\tcA{u}$} \cdot\ddx(3x-2)+(3x-2) \cdot\ddx(x^2+1) 	\; \tcA{\ddx(uv) = u \frac{dv}{dx} + v \frac{du}{dx}} \\
	\dydx &= \ubrace{(x^2+1)}{$\tcA{u}$} \cdot \ubrace{\ddx(3x-2)}{$\tcA{dv/dx}$} + \ubrace{(3x-2)}{$\tcA{v}$} \cdot \ubrace{\ddx(x^2+1)}{$\tcA{du/dx}$} 	\\ %\; \tcA{\ddx(uv) = u \frac{dv}{dx} + v \frac{du}{dx}} \\
	&= (x^2+1)(3)+(3x-2)(2x) \\
	&= 3x^2+3+6x^2-4x \\
	&= 9x^2-4x+3
\end{align*}
$$

At point $(1,2)$,

$$
\begin{align*}
	\dydx &= 9(1)^2-4(1)+3 \\
	&= 8		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}




---
$\example{8}$
Differentiate the function $z = \frac{w^3+2w}{3w-2}$

{% capture include_content %}
Apply the Quotient Rule,
$$
\begin{align*}
	\frac{d}{dw}(z) &= \frac{d}{dw}\br{ \frac{w^3+2w}{3w-2} } \\
	\frac{dz}{dw} &= \frac{(3w-2) \cdot\dfrac{d}{dw}(w^3+2w)-(w^3+2w) \cdot\dfrac{d}{dw}(3w-2)}{(3w-2)^2}	\\ %\quad \tcA{\ddx\br{\frac{u}{v}} = \frac{v\dfrac{du}{dx} - u\dfrac{dv}{dx}}{v^2}} \\
	&= \frac{(3w-2)(3w^2+2)-(w^3+2w)(3)}{(3w-2)^2} \\
	&= \frac{(9w^3+6w-6w^2-4)-(3w^3+6w)}{(3w-2)^2} \\
	&= \frac{6w^3-6w^2-4}{(3w-2)^2}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}






---
$\example{9}$
Differentiate the function $y = \frac{(2x+1)(x+2)}{x+1}$

{% capture include_content %}
Expand the numerator,

$$
\begin{align*}
	y &= \frac{2x^2+4x+x+2}{x+1} \\
	&= \frac{2x^2+5x+2}{x+1} \\
\end{align*}
$$

Then apply the Derivative Quotient Rule,

$$
\begin{align*}
	\ddx(y) &= \ddx\br{ \frac{2x^2+5x+2}{x+1} } \\
	\dydx &= \frac{(x+1)(4x+5)-(2x^2+5x+2)(1)}{(x+1)^2} \\
	&= \frac{(4x^2+5x+4x+5)-(2x^2+5x+2)}{(x+1)^2} \\
	&= \frac{2x^2+4x+3}{(x+1)^2}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}
