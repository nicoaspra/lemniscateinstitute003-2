---
title: "The Chain Rule"
prevcontenturl: ../DC-4.2-higher-order-derivatives
nextcontenturl: ../DC-4.4-implicit-differentiation
---


Functions may not always appear as simple as the examples given from the past sections. Hence, differentiating complexly structured functions such as a [composite function](../DC-1.4-composite-functions) cannot be easily solved by the previously discussed rules. With this in mind, we will introduce the Chain Rule in this section to differentiate composite functions. Notably, this rule is essential and may be **one of the most widely used rules** in Calculus. It may seem ambiguous now, but composite functions appear more frequently than it seems.

To start our discussion, let us first describe what the Chain Rule is and how to use it. Consider the composite function $y=f(g(x))$, let $u=g(x)$ so that we could simplify the function to  $y=f(u)$. Where $f(u)$ is the outer function and $g(x)$ is the inner function, given that $f(u)$ is differentiable to $g(x)$ and $g(x)$ is differentiable to $x$. The derivative of the composite function $f(g(x))$ with respect to $x$ is equal to the *product of the derivative of the outer function and the derivative of the inner function*.

{% include tcolorbox.html
    details = "
	(f \circ g)'(x) = f'(g(x)) \cdot g'(x)
	\label{eq:chain rule lagranges notation}
    "
%}

In Leibniz’s Notation, if $u=g(x)$ so that $y=f(u)$, then
{% include tcolorbox.html
    details = "
	\frac{dy}{dx}=\frac{dy}{du} \cdot \frac{du}{dx}
	\label{eq:chain rule leibnizs notation}
    "
%}

Where $dy/du$ is the derivative of the outer function $y=f(u)$ and $du/dx$ is the derivative of the inner function $u=g(x)$. To illustrate how the chain rule works, consider the following example.

---
$\example{1}$
Differentiate the function $y = (x^2+x)^3$.

{% capture include_content %}
$$
\begin{align*}
	\text{Let: } u &= x^2+x & \\
	y &= u^3
\end{align*}
$$

Differentiate the function with respect to $u$,

$$
\begin{align*}
	\frac{d}{du}\br{y} &= \frac{d}{du}\br{u^3} \\
	\frac{dy}{du} &= 3u^{2}
\end{align*}
$$

Then differentiate $u=x^2+x$ with respect to $x$,

$$
\begin{align*}
	\ddx\br{u} &= \ddx\br{x^2+x} \\
	\frac{du}{dx} &= 2x+1 \\
\end{align*}
$$

Thus, applying the Chain Rule gives us,

$$
\begin{align*}
	\dydx &= 3u^2 \cdot (2x+1) \quad \tcA{\dydx=\frac{dy}{du}\cdot\frac{du}{dx}} \\
\end{align*}
$$

Since $u=x^2+x$,

$$
\begin{align*}
	\dydx &= 3(x^2+x)^2 (2x+1)	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}









---

## General Power Rule

The General Power Rule is a **special case of the chain rule**. 
This rule is meant to evaluate functions in the form of $y=[f(x)]^n$ or $y=u^n$, given that $u$ is a function of $x$.

The derivative of the function $y=u^n$ with respect to $x$ is equal to the product of the exponent $n$, the power of a function with the exponent diminished by one $u^{n-1}$, and the derivative of the inner function ${du}/{dx}$.

{% include tcolorbox.html
    details = "
	\frac{d}{dx}(u^n)=nu^{n-1} \frac{du}{dx}
    "
%}

And we can also prove this by using the Chain Rule ($\eref{eq:chain rule leibnizs notation}$). Consider the function $y=u^n$.


Differentiate the function with respect to $u$,

$$
\begin{align*}
	\frac{d}{du}\br{y} &= \frac{d}{du}\br{u^n} \\
	\frac{dy}{du} &= nu^{n-1} \\
\end{align*}
$$

Then differentiate $u$ with respect to $x$,

$$
\begin{align*}
	\ddx\br{u} &= \frac{du}{dx} \\
\end{align*}
$$

Thus, applying the Chain Rule,

$$
\begin{align*}
	\dydx &= \frac{dy}{du}\cdot\frac{du}{dx} \\
	&= nu^{n-1}\frac{du}{dx}
\end{align*}
$$


---
$\example{2}$
Differentiate the function $y=(7x^2+1)^5$.

{% capture include_content %}
Apply the General Power Rule,
$$
\begin{align*}
	\ddx\br{y} &= \ddx\brk{(7x^2+1)^5} \\
	\dydx &= 5(7x^2+1)^4 \cdot \ubraces{\ddx\br{7x^2+1}}{derivative of the}{inner function} \qquad \tcA{u=7x^2+1} \\
	&= 5(7x^2+1)^4 (14x) \\
	&= 70x(7x^2+1)^4		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{3}$
Differentiate the function $y=\br{5-\frac{x}{3}}^{-4}$.

{% capture include_content %}
Apply the General Power Rule,
$$
\begin{align*}
	\ddx\br{y} &= \ddx\brk{ \br{5-\frac{x}{3}}^{-4} } \\
	\dydx &= -4 \br{5-\frac{x}{3}}^{-5} \cdot \ddx\br{5-\frac{x}{3}} \qquad \tcA{u=5-\frac{x}{3}} \\
	&= -\frac{4}{\br{5-\frac{x}{3}}^{5} } \br{-\frac{1}{3}} \\
	&= \frac{4}{3 \br{5-\frac{x}{3}}^{5} }		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}

<!-- \note{This can still be simplified} -->




---
$\example{4}$
Differentiate the function $y = \frac{1}{(5x^2+1)^2}+(x^2+2)^{1/3}$.


{% capture include_content %}
Simplify the expression,

$$
\begin{align*}
	y &= (5x^2+1)^{-2}+(x^2+2)^{1/3} \\
\end{align*}
$$

Then differentiate the function by applying the Sum Rule along with the General Power Rule,

$$
\begin{align*}
	\ddx\br{y} &= \ddx\brk{(5x^2+1)^{-2}+(x^2+2)^{1/3}} \\
	\dydx &= \ubrace{ -2(5x^2+1)^{-3} \cdot \ddx\br{5x^2+1} }{derivative of $(5x^2+1)^{-2}$} + 
		\ubrace{ \frac{1}{3}(x^2+2)^{\frac{1}{3}-1} \cdot \ddx\br{x^2+2} }{derivative of $(x^2+2)^{1/3}$} \\
	&= -2(5x^2+1)^{-3} (10x) + \frac{1}{3}(x^2+2)^{-2/3} (2x) \\
	&= -\frac{20x}{(5x^2+1)^{3}} + \frac{2x}{3(x^2+2)^{2/3}}
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{5}$
Differentiate the function $x = \sqrt{5t^4-t^2+2t+7}$.

{% capture include_content %}
Express the radical as a power of a rational exponent,

$$
\begin{align*}
	x &= \br{5t^4-t^2+2t+7}^{1/2} \\
\end{align*}
$$

Then differentiate the function,

$$
\begin{align*}
	\ddt\br{x} &= \ddt\brk{\br{5t^4-t^2+2t+7}^{1/2}} \\
	\frac{dx}{dt} &= \frac{1}{2}\br{5t^4-t^2+2t+7}^{\frac{1}{2}-1} 
		\cdot \ddt\br{5t^4-t^2+2t+7} \\
	&= \frac{1}{2}\br{5t^4-t^2+2t+7}^{-1/2} \br{20x^3-2t+2} \\
	&= \frac{\cancel{2} (10x^3-t+1)}{\cancel{2} (5t^4-t^2+2t+7)^{1/2}} \\
	&= \frac{10x^3-t+1}{\sqrt{5t^4-t^2+2t+7}}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{6}$
Find the slope at point $(1,9)$ of the curve $y = (2x-1)^3(x+2)^2$

{% capture include_content %}
Apply the Product Rule along with the General Power Rule,
$$
\begin{align*}
	\ddx\br{y} &= \ddx\brk{(2x-1)^3(x+2)^2} \\
	\dydx &= \ubrace{(2x-1)^3 \cdot\ddx\brk{(x+2)^2}}{$u\cdot\frac{dv}{dx}$} + \ubrace{(x+2)^2 \cdot\ddx\brk{(2x-1)^3}}{$v\cdot\frac{du}{dx}$} 
		\quad \tcA{\ddx{uv}=u\frac{dv}{dx}+v\frac{du}{dx}} \\
	&= (2x-1)^3 [2(x+2)(1)] + (x+2)^2 [3(2x-1)^2(2)] \\
	&= 2(2x-1)^3 (x+2) + 6(x+2)^2 (2x-1)^2 \\
\end{align*}
$$

At point $(1,9)$,

$$
\begin{align*}
	&= 2[2(1)-1]^3 [(1)+2] + 6[(1)+2]^2 [2(1)-1]^2 \\
	&= 60		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}





---
$\example{7}$
Differentiate the function $\textstyle{ y = \sqrt{1+\sqrt{x+1}} }$

{% capture include_content %}
There are situations when we must use the chain rule multiple times to determine the derivative. This particular example is one of its instances. To start, let us first express the radical as a power of a rational exponent.

$$
\begin{align*}
	y &= \br{1+(x+1)^{1/2} }^{1/2} \\
\end{align*}
$$

Differentiate the function by applying the chain rule more than once,

$$
\begin{align*}
	\ddx\br{y} &= \ddx\brk{ \br{1+(x+1)^{1/2} }^{1/2} } \\
	\dydx &= \frac{1}{2} \brk{1+(x+1)^{1/2} }^{1/2-1} \cdot\ddx\brk{1+(x+1)^{1/2} } \\
	&= \frac{1}{2} \brk{1+(x+1)^{1/2} }^{-1/2} \brk{0+\frac{1}{2}(x+1)^{1/2-1} \cdot \ddx\br{x+1} } \\
	&= \frac{1}{2} \brk{1+(x+1)^{1/2} }^{-1/2} \brk{\frac{1}{2}(x+1)^{-1/2} (1) } \\
	&= \frac{1}{4} \brk{1+(x+1)^{1/2} }^{-1/2} (x+1)^{-1/2} \\
	&= \frac{1}{4} \bbbrk{ \brk{ 1+(x+1)^{1/2} } (x+1) }^{-1/2} \\
	&= \frac{1}{4\brk{ (1+\sqrt{x+1})(x+1) }^{1/2}} \\
	&= \frac{1}{4\sqrt{ (1+\sqrt{x+1})(x+1) } }		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}