---
title: "Differentials"
prevcontenturl: ../DC-5.4-maxima-and-minima
nextcontenturl: ../DC-7.1-differentials
---





Derivative is the rate of change of a variable with respect to another. In [Chapter 3](../DC-3.1-introduction-to-derivatives), we have established that the derivative $dy/dx$ is not referred as a ratio but a limit of the ratio $\Delta y / \Delta x$ as $\Delta x$ approaches zero. On the other hand, the **differential** simply means an **infinitely small amount of change** which can be useful to approximate the amount of change of the function. The notation $dy$ or $dx$ alone are called **differentials**, the symbol $d$ before the variable is read "differential of.''

Given the function $y=f(x)\,dx$, its differential is denoted as,

{% include tcolorbox.html
    details="
	dy = f'(x) \, dx
    "
%}




## Differential Formulas
From all our past lessons, we have been differentiating functions using the [rules for algebraic functions](../DC-4.1-differentiation-and-its-rules-for-algebraic-functions.md), but now, let us look at the differential formulas. 
Differentials can be useful in various applications such as approximating small amount of quantities, and also in future courses such as Integral Calculus.

The following differentials are some of the most used formulas in integration. Integration techniques are applied in a differential function rather than derivative functions; hence a good mastery of differentials will give you an edge in solving problems in Integral Calculus.


However, in this lesson, we are more particular in understanding first how to evaluate functions using the following formulas.

<!-- The following formulas are useful in quantifying small amount of change compared to the formulas that we're already accustomed to which are used to evaluate slopes and rate of change, specifically problems that are in relation to other variables. In the case of differentials, however, we can consider the derivative $\dydx$ as two independent differentials $dy$ and $dx$ respectively. -->

<!-- As you may have realized, the formulas in differentials are not that different compared with what we were already used to. Instead of treating $\dydx$ as one, in this lesson it is treated as two independent differentials.  -->


{% include tcolorbox.html
    details="
	\text{Constant:} &&& d(c) = 0 \\
	\text{Variable:} &&& d(x) = dx \\
	\text{Constant Multiple:} &&& d(cu) = c\,du \\
	\text{Sum/Difference of Two Functions:} &&& d(u\pm v) = du\pm dv \\
	\text{Product of Two Functions:} &&& d(uv) = u\,dv + v\,du \\
	\text{Quotient of Two Functions:} &&& d\br{\frac{u}{v}} = \frac{v\,du - u\,dv}{v^2} \\
	\text{General Power Formula:} &&& d(u^n) = n \cdot u^{n-1} \,du
	\label{eq:differential formula the general power rule}
    "
%}


As you can see, the formulas do not differ very much compared to the formulas for differentiation. Even solving for the differential is not that far of an experience; some may even find it easier to deal with. Nonetheless, it will be best if we try some examples using these formulas.





---
$\example{1}$
Determine the differential of the function:
$y = 6x^4+5x^3-2x-1$

{% capture include_content %}

$$
\begin{align*}
	d\br{y} &= d(6x^4+5x^3-2x-1) \\
	dy & = d(6x^4)+d(5x^3)-d(2x)-d(1) \\
	   &= 24x^3\,dx+15x^2\,dx-2\,dx +0 \\
    dy &= (24x^3+15x^2-2)\,dx		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}











---
$\example{2}$ 
Determine $\frac{dx}{dy}$ of the function:
$x = \frac15 y^4 - \frac{2}{y^2}+\sqrt{y}$

{% capture include_content %}

$$
\begin{align*}
	x &= \frac15 y^4 - 2y^{-2}+y^{1/2} \\
	d\br{x} &= d\br{\frac15 y^4 - 2y^{-2}+y^{1/2}} \\
	dx &= \frac45 y^3 \,dy +4y^{-3}\,dy + \frac12 y^{-1/2}\,dy \\
	&= \br{\frac45 y^3+\frac{4}{y^3}+\frac{1}{2\sqrt{y}}}\,dy \\
	\frac{dx}{dy} &= \frac45 y^3+\frac{4}{y^3}+\frac{1}{2\sqrt{y}}	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}

<!-- % $z = \sqrt[3]{2-6x}$

% $x = t^3(t^2-5)^{-1/3}$ -->










---
$\example{3}$
Solve for the derivative of the function $x^2+y^2 = 9$ with respect to $x$ using differentials.


{% capture include_content %}
In this example, the given equation is  expressed implicitly. 
However, formulas for differentials can be used to obtain the derivative of a variable,

$$
\begin{align*}
	d\br{x^2+y^2} &= d\br{9} \\
	2x\,dx +2y\,dy &= 0 \\
	2y\,dy &= -2x\,dx
\end{align*}
$$

Then, rearranging the differentials, we obtain,

$$
\begin{align*}
	\dydx &= -\frac{\cancel{2}x}{\cancel{2}y} \\
	&= -\frac{x}{y}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{4}$
Determine the differential of the implicit function
$x^3+2x^2y+3y = 1$

{% capture include_content %}

$$
\begin{align*}
	d\br{x^3+2x^2y+3y} &= d\br{1} \\
	3x^2\,dx + 2\brk{(x^2)(dy)+(y)(2x\,dx)}+3\,dy &= 0 \\
	3x^2\,dx + 2\br{x^2\,dy+2xy\,dx}+3\,dy &= 0 \\
	3x^2\,dx + 2x^2\,dy+4xy\,dx+3\,dy &= 0 
\end{align*}
$$

Then combine all the terms that contains the same differentials,

$$
\begin{align*}
	(3x^2+4xy)\,dx + (2x^2+3)\,dy &= 0	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}

