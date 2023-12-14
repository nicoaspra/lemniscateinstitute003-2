---
title: "Implicit Differentiation"
prevcontenturl: ../DC-4.3-the-chain-rule
nextcontenturl: ../DC-5.1-tangents-and-normals-to-plane-curves
---




Before we can differentiate Implicit functions, we must first understand what an implicit function is, and to do this, we need to know the difference between explicit and implicit functions. An **Explicit Function** is a function where the dependent variable is **expressed explicitly** in terms of the independent variable, which means that the dependent variable (usually $y$) can be left alone in one side of the equation and be expressed in terms of the independent variable; it is denoted as $y=f(x)$. With this in mind, all the functions that we have dealt with are all explicit functions for the past sections, but not all functions can be expressed explicitly.  Having said so, an Implicit Function is a function where the dependent variable is **not expressed explicitly** as a function of the independent variable; it is denoted as $f(x,y)=0$. To illustrate the distinction between the two functions, consider the following examples:


{% include minibox.html
    details = "
	$\tcAal{Examples of Explicit Functions}$
        $$y=3x^2+5x-1$$
        $$w=\frac{3x-1}{5x^2+2}$$
        $$f(x) = \sqrt{1+\sqrt{x+1}}$$
    "
%}

{% include minibox.html
    details = "
        $\tcAal{Examples of Implicit Functions}$
        $$x^2+y^2=1$$
        $$5x^3+xy^2=3x^2y^5$$
        $$f(x,y)=x^2+4xy+y^2$$
    "
%}


The first step in solving the derivative of an Implicit Function is by differentiating all the terms of the equation individually, treating one of the variables as a function of the other (usually $y$ is a function of $x$). The chain rule will be a great use when differentiating the dependent variable $y$. After differentiating, combine all the terms that contains $dy/dx$, then isolate $dy/dx$ on one side. Then the result would now be the derivative of the function. 


---
$\example{1}$
Find $\frac{dy}{dx}$ of the equation $x^2+y^2=1$.

$\solution$\\
From the given problem, we are required to solve for $\dydx$, which means that we have to differentiate the equation with respect to $x$. Thus,

$$
\begin{align*}
	\ddx\br{x^2+y^2} &= \ddx\br{1} \\
	\ddx\br{x^2} + \ddx\br{y^2} &= 0 \\
\end{align*}
$$

Then apply the [Chain Rule](../DC-4.3-the-chain-rule) to $\ddx\br{y^2}$,

$$
\begin{align*}
	2x + 2y \cdot \dydx &= 0  \qquad \tcA{\ddx(y^2)= \frac{d}{\tcB{dy}}(y^2) \cdot \frac{\tcB{dy}}{dx}} \\
	2y \cdot \dydx &= -2x \\
	\dydx &= -\frac{\cancel{2}x}{\cancel{2}y} \\
	&= -\frac{x}{y}		\tagans
\end{align*}
$$

You may be wondering at this point how the rules are similar to those for differentiating algebraic functions, except for the term containing the variable $y$. Differentiating implicit functions is not that different from differentiating explicit functions; the rules discussed in previous lessons remain valid.

In this example, we have used the [Chain Rule](../DC-4.3-the-chain-rule) to solve for the term that contains $y$. However, if this continues to confound you, let us try another approach. 

Consider the following result of differentiating an explicit function such as $y=5x^2$,

$$
\begin{align*}
    \ddx\br{y} &= \ddx\br{5x^2} \\
    \dydx &= 10x
\end{align*}
$$


Differentiating $y$ with respect to $x$ results in $\dydx$. Differentiating $x$ with respect to $x$, on the other hand, produces 1. Keeping this in mind, the method for differentiating implicit functions is identical to the method for differentiating explicit functions, the only difference is how the function is expressed.





---
$\example{2}$
Find $y'$ of the implicit function $x^2+2xy+y^2=0$.

{% capture include_content %}
Differentiate the equation with respect to $x$,

$$
\begin{align*}
	\ddx\br{x^2+2xy+y^2} &= \ddx\br{0} \\
	\ddx\br{x^2} + \ddx\br{2xy} \ddx\br{y^2} &= 0 \\
\end{align*}
$$

Then apply the [Product Rule](../DC-4.1-differentiation-and-its-rules-for-algebraic-functions) to $\ddx\br{2xy}$,

$$
\begin{align*}
	2x + 2\brk{ x \cdot \ddx(y) + y \cdot \ddx(x) } + 2y \cdot \dydx &= 0 
		\quad \tcA{\ddx{uv}=u\frac{dv}{dx}+v\frac{du}{dx}} \\
	2x+2\brk{x\dydx+y(1)}+ 2y \dydx &= 0 \\
	2x+2\br{xy'+y}+ 2y \, y' &= 0 \\
	2x+2xy'+2y+2y \, y' &= 0 \\
\end{align*}
$$

Combining all the terms that contains $y'$ gives us,

$$
\begin{align*}
	(2x+2y) y' &= -2x-2y \\
	y' &= \frac{-\cancel{(2x+2y)}}{\cancel{2x+2y}} \\
	&= -1			\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}









---
$\example{3}$
Differentiate the implicit function $x\sqrt{y}=2x+1$ with respect to $x$.

{% capture include_content %}

$$
\begin{align*}
	x(y)^{1/2} &= 2x+1 \\
\end{align*}
$$

Differentiate the equation with respect to $x$,

$$
\begin{align*}
	\ddx\brk{ x(y)^{1/2} } &= \ddx\br{2x+1} \\
	x\cdot\ddx\br{y^{1/2}} + y^{1/2} \cdot\ddx\br{x} &= 2 
		\qquad \qquad \tcA{\ddx{uv}=u\frac{dv}{dx}+v\frac{du}{dx}} \\
	x\br{\frac12}y^{-1/2} \dydx + y^{1/2} (1) &= 2 \\
	\frac{x}{2y^{1/2}} \dydx &= 2 - y^{1/2}\\
	\dydx &= \frac{2y^{1/2}}{x} \br{2 - y^{1/2}} \\
	&= \frac{2\sqrt{y}}{x} \br{2 - \sqrt{y}} 		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}










---
$\example{4}$
Differentiate the function $5x^3=(2xy+1)^2$ with respect to $x$.

{% capture include_content %}
Differentiate the equation with respect to $x$,

$$
\begin{align*}
	\ddx\br{5x^3} &= \ddx\brk{(2xy+1)^2} \\
	15x^2 &= 2(2xy+1) \cdot \ddx\br{2xy+1} \\
	15x^2 &= 2(2xy+1) \cdot 2(xy'+y) \\
	4(2xy+1)(xy'+y) &= 15x^2 \\
	xy' &= \frac{15x^2}{4(2xy+1)} - y \\
	y' &= \frac{15x^2}{4x(2xy+1)} - \frac{y}{x} \\
	&= \frac{15x^2 - 4y(2xy+1)}{4x(2xy+1)}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{5}$
Use implicit differentiation to find the derivative of the function $\textstyle{ y=\sqrt{1+\sqrt{x+1}} }$.

{% capture include_content %}
From the previous lesson, we have already differentiated the same problem using the [Chain Rule](../DC-4.3-the-chain-rule). However, we can further simplify our solution through Implicit Differentiation. In this case, what makes the problem a bit challenging to solve are the radicals. Therefore, to alleviate the situation, let us first eliminate the radicals by squaring the equation.

$$
\begin{align*}
	y^2 &= \br{ \sqrt{1+\sqrt{x+1}} }^2 \\
	y^2 &= 1+\sqrt{x+1} \\
	(y^2-1)^2 &= \br{ \sqrt{x+1} }^2 \\
	(y^2-1)^2 &= x+1 \\
\end{align*}
$$

Then differentiate the equation with respect to $x$,

$$
\begin{align*}
	\ddx\brk{(y^2-1)^2} &= \ddx\br{x+1} \\
	2(y^2-1) \cdot \ddx\br{y^2-1} &= 1 \\
	2(y^2-1)(2y\,y') &= 1 \\
	4y\,y' (y^2-1) &= 1 \\
	y' &= \frac{1}{4y(y^2-1)}		\tagans
\end{align*}
$$

As you may have noticed, the final answer does not match the answer from our [previous lesson](../DC-4.3-the-chain-rule). It is because we have differentiated it implicitly. Thus, having a final answer of an implicit function. If, however, you want to express the final answer explicitly as a function of $x$, we can replace the value of $y$ with $\sqrt{1+\sqrt{x+1}}$.

$$
\begin{align*}
    y' &= \frac{1}{4y(y^2-1)} \\
       &= \frac{1}{4\sqrt{1+\sqrt{x+1}}\brk{\br{\sqrt{1+\sqrt{x+1}}}^2-1}} \\
       &= \frac{1}{4\sqrt{1+\sqrt{x+1}}\brk{\cancel{1}+\sqrt{x+1}-\cancel{1}}} \\
       &= \frac{1}{4\sqrt{\br{1+\sqrt{x+1}}(x+1)}}      \tagans
\end{align*}
$$


As a result, the final answer can be expressed in any of the two ways. It will ultimately come down to personal preference or to what is required.

$$y' = \frac{1}{4y(y^2-1)} = \frac{1}{4\sqrt{\br{1+\sqrt{x+1}}(x+1)}}$$

{% endcapture %}
{% include solution.html details = include_content %}



