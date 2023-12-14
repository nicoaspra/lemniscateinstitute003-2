---
title: "Derivatives of Exponential and Logarithmic Functions"
prevcontenturl: ../DC-8.2-logarithmic-functions
nextcontenturl: ../DC-9.1-angles
---




In the previous lesson, we have reviewed the concepts and the handling of exponential and logarithmic functions. It is essential to develop a strong understanding of the basic rules and laws governing such functions' analysis before attempting to try to understand its derivative.



Just as algebraic functions, differentiating exponential and logarithmic functions have its own set of rules. For the following formulas, let $u$ be a function of $x$; $a$ as a constant; and $e$ is the Euler's number.


{% include tcolorbox.html
    details="
	\text{Logarithmic Funcion to Base $a$:} &&& d(\log_a u) = \frac{du}{u\,\ln a} 
		\label{eq:differential of the Logarithmic Funcion to Base a}\\
	\text{Natural Logarithmic Function:} &&& d(\ln u) = \frac{du}{u}
		\label{eq:differential of Natural Logarithmic Function}\\
	\text{Exponential Function, $e^u$:} &&& d(e^u) = e^u\,du 
		\label{eq:differential of Exponential Function e^u}\\
	\text{Exponential Function, $a^u$:} &&& d(a^u) = a^u\ln a\,du 
		\label{eq:differential of Exponential Function a^u}
    "
%}


---
$\example{1}$
Find the derivative of the function $y = \log_5 (2x+3)$

{% capture include_content %}
$$
\begin{align*}
	\text{Let:}\quad a &= 5  \hspace{100cm} \\
	u &= 2x+3 & \\
	du &= 2\,dx
\end{align*}
$$

To solve for the derivative of the function, use $\eref{eq:differential of the Logarithmic Funcion to Base a}$,

$$
\begin{align*}
	d(y) &= d\br{\log_5 (2x+3)} \\
	dy &= \frac{2\,dx}{(2x+3)\ln 5} \qquad\tcA{d(\log_a u) = \frac{du}{u\,\ln a}} \\
	\dydx &= \frac{2}{(2x+3)\ln 5}	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}




---
$\example{2}$
Find the derivative of the function $y = \log_e (5-2x)$

{% capture include_content %}
$$
\begin{align*}
	\text{Let:}\quad a &= e \hspace{100cm} \\
	u &= 5-2x & \\
	du &= -2\,dx
\end{align*}
$$

To solve for the derivative of the function, use $\eref{eq:differential of the Logarithmic Funcion to Base a}$,

$$
\begin{align*}
	d(y) &= d\br{\log_e (5-2x)} \\
	dy &= \frac{-2\,dx}{(5-2x)\ln e}
\end{align*}
$$

But form the Properties of Natural Logarithms, $\ln e = 1$. Thus,

$$
\begin{align*}
	\dydx &= -\frac{2}{(5-2x)(1)} \\
	&= -\frac{2}{5-2x}	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}








---
$\example{3}$
Find the derivative of the function $y = \ln (5-2x)$

{% capture include_content %}
$$
\begin{align*}
	\text{Let:}\quad u &= 5-2x \hspace{100cm} \\
	du &= -2\,dx
\end{align*}
$$

To solve for the derivative of the function, use $\eref{eq:differential of Natural Logarithmic Function}$,

$$
\begin{align*}
	d(y) &= d\br{\ln (5-2x)} \\
	dy &= \frac{-2\,dx}{5-2x} \\
	\dydx &= -\frac{2}{5-2x}	\tagans
\end{align*}
$$


As you may have noticed, the answer is the same as the previous example. With this, we can verify that $\log_e u$ is equal to $\ln u$.

{% endcapture %}
{% include solution.html details = include_content %}










---
$\example{4}$ 
Differentiate the function $y = \ln\sqrt{2x^2-5x+3}$ with respect to $x$.

{% capture include_content %}
$$
\begin{align*}
	\text{Let:}\quad u &= \sqrt{2x^2-5x+3} \hspace{100cm} \\
	du &= d\br{\sqrt{2x^2-5x+3}} \\
	&= d\br{(2x^2-5x+3)^{1/2}} \\
	&= \frac12(2x^2-5x+3)^{-1/2}\cdot d(2x^2-5x+3) \\
	&= \frac{1}{2\sqrt{2x^2-5x+3}} \cdot (4x-5) \,dx \\
	&= \frac{4x-5}{2\sqrt{2x^2-5x+3}} \,dx \\
\end{align*}
$$


To solve for the derivative of the function, use $\eref{eq:differential of Natural Logarithmic Function},$

$$
\begin{align*}
	d(y) &= d\br{\ln\sqrt{2x^2-5x+3}} \\
	dy &= \frac{\frac{4x-5}{2\sqrt{2x^2-5x+3}} \,dx}{\sqrt{2x^2-5x+3}} \\
	dy &= \frac{4x-5}{2\sqrt{2x^2-5x+3} \cdot \sqrt{2x^2-5x+3}} \,dx \\
	\dydx &= \frac{4x-5}{2\br{\sqrt{2x^2-5x+3}}^2} \\
	&= \frac{4x-5}{2\br{2x^2-5x+3}} 	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{5}$ 
Determine the differential of the function $y = 5e^{3x}$.

{% capture include_content %}
To solve for the differential of the function, use $\eref{eq:differential of Exponential Function e^u}$,

$$
\begin{align*}
	d(y) &= d\br{5e^{3x}} \\
	dy &= 5e^{3x} \cdot d(3x) \\
	&= 5e^{3x} \cdot 3\,dx \\
	&= 15e^{3x} \,dx	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{6}$ 
Find the derivative of the function with respect to $t$: $x = e^{3t}e^{2t^2}$.

{% capture include_content %}
To solve for the derivative of the function, use $\eref{eq:differential of Exponential Function e^u}$,

$$
\begin{align*}
	d(x) &= d\br{e^{3t}e^{2t^2}} \\
	dx &= d\br{e^{3t+2t^2}} \qquad\tcA{a^m+a^n = a^{m+n}} \\
	&= e^{3t+2t^2} \cdot d(3t+2t^2) \\
	&= e^{3t+2t^2} \cdot (3+4t)\,dt \\
	\frac{dx}{dt} &= (3+4t)e^{3t+2t^2}	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}









---
$\example{7}$ 
Determine the differential of the function $w = 125\br{5^{3v}}$.

{% capture include_content %}
To solve for the differential of the function, use $\eref{eq:differential of Exponential Function a^u}$,

$$
\begin{align*}
	d(w) &= d\br{125\br{5^{3v}}} \\
	dw &= d\br{5^3\cdot 5^{3v}} \\
	&= d\br{5^{3+3v}} \\
	&= 5^{3+3v} \ln 5 \cdot d\br{3+3v} \\
	&= 5^{3+3v} \ln 5 \cdot 3 \,dv \\
	&= 3\ln 5\cdot 5^{3+3v} \,dv 		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}








<!-- ---
$\example{}$
$\ln{y} = 8x+3$ -->



---
$\example{8}$ 
Find the derivative of $y$ with respect to $x$ of the function
$e^{\frac12 y} = x^2-1$.

{% capture include_content %}
In this example, the given equation is expressed as an [implicit function](../DC-4.4-implicit-differentiation). Hence, to determine its derivative, we can differentiate the given equation explicitly.
 <!-- with respect to $x$. -->
$$
\begin{align*}
	d\br{e^{\frac12 y}} &= d\br{x^2-1} \\
	e^{\frac12 y} \cdot d\br{\frac12 y} &= 2x\,dx \\
	e^{y/2} \cdot \frac12 \,dy &= 2x\,dx \\
	\dydx &= \frac{4x}{e^{y/2}}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}