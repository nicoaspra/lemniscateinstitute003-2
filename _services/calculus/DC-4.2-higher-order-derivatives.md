---
title: "Higher Order Derivatives"
prevcontenturl: ../DC-4.1-differentiation-and-its-rules-for-algebraic-functions
nextcontenturl: ../DC-4.3-the-chain-rule
---


Differentiation of previously differentiated functions is still possible. The process of successively differentiating a function is referred to as **Successive Differentiation**. For instance, the second derivative of a function is achieved by differentiating the first derivative, and differentiating it again yields the third derivative, provided that it is still differentiable. Thus, through Successive Differentiation, **Higher-Order Derivatives** are obtained. 

Higher-Order Derivatives can be interpreted differently in various applications; for instance, in Physics, the second derivative of an object's displacement with respect to time is referred to as acceleration. In Polynomial Curves, on the other hand, the second derivative of a function is utilized to determine the polynomial's points of inflection. 
However, before applying this concept to various fields, let us first familiarize ourselves with its notations and solve some fundamental problems.







## Notation of Higher Order Derivatives


{% include minibox.html
    details = "
    $\tcBal{Leibniz's Notation}$ 
    $$
    \begin{align}
        \frac{d^2y}{dx^2} &=\frac{d}{dx}\br{\dydx}  & \text{second derivative}      
            \nonumber\\
		\frac{d^3y}{dx^3} &=\frac{d}{dx}\br{\frac{d^{2}y}{dx^2}} & \text{third derivative}		
            \nonumber\\
		 &\cdots  
            \nonumber\\
		\frac{d^ny}{dx^n} &=\frac{d}{dx}\br{ \frac{d^{n-1}y}{dx^{n-1}} } & \phantom{asdssssssss}\text{$n^{\text{th}}$ derivative} 
            \nonumber\\
    \end{align}
    $$
    $\tcBal{Lagrange's Notation}$ 
    $$
    \begin{align}
	 	y'' &= f''(x) = \frac{d}{dx}\br{\dydx}  & \text{second derivative} 
            \nonumber\\
		y''' &= f'''(x) = \frac{d}{dx}\br{\frac{d^{2}y}{dx^2}} & \text{third derivative}		
            \nonumber\\
		&\cdots  
            \nonumber\\
		y^n &= f^n(x) = \frac{d}{dx}\br{ \frac{d^{n-1}y}{dx^{n-1}} } & \text{$n^{\text{th}}$ derivative} 
            \nonumber
    \end{align}
    $$
    "
%}





---
$\example{1}$
Find the second derivative of the function $y = x^3+3x+2$.

{% capture include_content %}
Differentiate the function,

$$
\begin{align*}
	\ddx\br{y} &= \ddx\br{x^3+3x+2} \\
	\dydx &= 3x^2+3
\end{align*}
$$

Then differentiate again,

$$
\begin{align*}
	\ddx\br{\dydx} &= \ddx\br{3x^2+3} \\
	\frac{d^2y}{dx^2} &= 6x		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}









---
$\example{2}$
Find $\frac{d^4y}{dx^4}$ of the function $y = x^5-3x^4+7x^2+5$.

{% capture include_content %}
Differentiate the function four (4) times,
$$
\begin{align*}
	\ddx\br{y} &= \ddx\br{x^5-3x^4+7x^2+5} \\
	\dydx &= 5x^4-12x^3+14x \\
	\ddx\br{\dydx} &= \ddx\br{5x^4-12x^3+14x} \\
	\frac{d^2y}{dx^2} &= 20x^3-36x^2+14 \\
	\ddx\br{\frac{d^2y}{dx^2}} &= \ddx\br{20x^3-36x^2+14} \\
	\frac{d^3y}{dx^3} &= 60x^2-72x \\
	\ddx\br{\frac{d^3y}{dx^3}} &= \ddx\br{60x^2-72x} \\
	\frac{d^4y}{dx^4} &= 120x-72		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}









---
$\example{3}$
Find $f'''(x)$ of the function $f(x)=\frac{5}{a\sqrt{x}}-\frac{1}{x^3}$, where $a$ is a constant.

{% capture include_content %}
Express the radical as a power with a rational exponent,

$$
\begin{align*}
	f(x) &= \frac{5}{a\sqrt{x}}-\frac{1}{x^3} \\
	&= \frac{5}{a}x^{-\frac{1}{2}} - x^{-3} 
\end{align*}
$$

Differentiate the function three (3) times,

$$
\begin{align*}
	f'(x) &= \ddx\br{\frac{5}{a}x^{-\frac{1}{2}} - x^{-3}} \\
	&= \br{-\frac{1}{2}} \frac{5}{a} x^{-\frac{1}{2}-1}-(-3)x^{-3-1} \\
	&= -\frac{5}{2a}x^{-\frac{3}{2}}+3x^{-4} \\
	f''(x) &= \ddx\br{-\frac{5}{2a}x^{-\frac{3}{2}}+3x^{-4}} \\
	&= \frac{15}{4a}x^{-\frac{5}{2}}-12x^{-5} \\
	f'''(x) &= \ddx\br{\frac{15}{4a}x^{-\frac{5}{2}}-12x^{-5}} \\
	&= -\frac{75}{8a}x^{-\frac{7}{2}} + 60x^{-6} \\
	&= \frac{60}{x^6} - \frac{75}{8ax^{\frac{7}{2}}}	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}









---
$\example{4}$
Determine on what $n^{th}$ derivative of $y=5x^3-x^2+7$ will have a value of zero. ($y^n = 0$)


{% capture include_content %}
Differentiate the function until its value becomes zero.

$$
\begin{align*}
	\ddx\br{y} &= \ddx\br{5x^3-x^2+7} \\
	y' &= 15x^2-2x \\
	\ddx\br{y'} &= \ddx\br{15x^2-2x} \\
	y'' &= 10x-2 \\
	\ddx\br{y''} &= \ddx\br{10x-2} \\
	y''' &= 10 \\
	\ddx\br{y'''} &= \ddx\br{10} \\
	y^{(4)} &= 0
\end{align*}
$$

Therefore, the value will become zero at the 4$\nth$ derivative.

{% endcapture %}
{% include solution.html details = include_content %}














---

## Acceleration
Acceleration is an important concept when it comes to motion. To better understand how acceleration works, let's have an example. 

If you are travelling at a rate of 50 m/s, then after a second your rate increases to 60 m/s, and 70 m/s after the next second. This indicates that you are increasing your pace as time passes or that you are "accelerating.'' According to our example, you are accelerating at a rate of 10 m/s per second, which is expressed as 10 m/s/s or 10 $\mathrm{m/s^2}$. With this, we can now define acceleration mathematically. It is the change in velocity with respect to time. Thus, acceleration can be denoted as,

<!-- Say you are traveling at a rate of 50 m/s, then after a second, your rate becomes 60 m/s, and 70 m/s after the next second. The increase in velocity means you are speeding up as the time passes by, or we could say, "you are accelerating.'' From our example, you are accelerating 10 m/s for every second or 10 m/s/s or 10 $\mathrm{m/s^2}$. With this, we can now define what acceleration is, its the rate of change in velocity with respect to time, -->

$$a=\frac{dv}{dt}$$

However, since velocity is the rate of change of displacement with respect to time ${ v=\frac{ds}{dt} }$, we can also represent acceleration as the second derivative of displacement with respect to time,

$$a=\frac{d}{dt}v=\frac{d}{dt} \br{ \frac{ds}{dt} } =\frac{d^2s}{dt^2}$$

{% include tcolorbox.html
    details = "
        a = \frac{dv}{dt} = \frac{d^2s}{dt^2}
    "
%}




---
$\example{5}$
An astronaut on the moon throws a rock vertically upward with a velocity of 5 m/s and catches it at the same position where it was thrown. 
<!-- How long did it take to be caught? ($g_{moon} = 1.62 \un{m/s^2}$) -->
The displacement of the rock is defined by the equation $s = 5t-0.18t^2 \un{m}$.
Determine the rock's
(a) velocity after 7 s, and
(b) its acceleration in $\mathrm{m/s^2}$.



{% capture include_content %}
$\For{a}$ \\
Differentiate the function with respect to time $t$,

$$
\begin{align*}
	\frac{d}{dt}\br{s} &= \frac{d}{dt}\br{5t-0.18t^2} \\
	\frac{ds}{dt} &= 5-0.36t
\end{align*}
$$

At $t=7\un{s}$,

$$
\begin{align*}
	v &= 5-0.36(7) \\
	&= 2.48 \un{m/s}	\tagans
\end{align*}
$$

$\For{b}$\\
Then differentiating again gives us the acceleration of the rock.
$$
\begin{align*}
	\frac{d}{dt}\br{\frac{ds}{dt}} &= \frac{d}{dt}\br{5-0.36t} \\
	\frac{d^2s}{dt^2} &= -0.36 \\
	a &= -0.36 \un{m/s^2}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}