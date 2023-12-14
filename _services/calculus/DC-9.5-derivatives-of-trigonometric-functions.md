---
title: "Derivatives of Trigonometric Functions"
prevcontenturl: ../DC-9.4-trigonometric-identities
nextcontenturl: ../DC-9.5-derivatives-of-trigonometric-functions
---




In our previous lesson, we have reviewed some of the fundamental concepts in trigonometric functions.
Since before we can differentiate such functions, we must first be proficient in transforming functions from one form to another. Below are some of the different formulas for differentiating trigonometric functions. For the following formulas, let $u$ be a function of $x$.

{% include tcolorbox.html
    details = "
	\ddu\br{\sin u} &= \cos u
		\label{eq:derivative of sin}\\
	\ddu\br{\cos u} &= -\sin u
		\label{eq:derivative of cos}\\
	\ddu\br{\tan u} &= \sec^2 u
		\label{eq:derivative of tan}\\
	\ddu\br{\cot u} &= -\csc^2 u
		\label{eq:derivative of cot}\\
	\ddu\br{\sec u} &= \tan u \sec u
		\label{eq:derivative of sec}\\
	\ddu\br{\csc u} &= -\cot u \csc u
		\label{eq:derivative of csc}
        "
%}





## Differential Formulas for Trigonometric Functions
As you may have realized, there is only a small difference between the formulas for differentiation and its differentials. 
{% include tcolorbox.html
    details = "
        d\br{\sin u} &= \cos u\,du 
            \label{eq:differential of sin}\\
        d\br{\cos u} &= -\sin u\,du
            \label{eq:differential of cos}\\
        d\br{\tan u} &= \sec^2 u\,du 
            \label{eq:differential of tan}\\
        d\br{\cot u} &= -\csc^2 u\,du 
            \label{eq:differential of cot}\\
        d\br{\sec u} &= \tan u \sec u\,du 
            \label{eq:differential of sec}\\
        d\br{\csc u} &= -\cot u \csc u\,du
            \label{eq:differential of csc}
    "
%}


---
$\example{1}$
Find the differential of the function $y = \sin 5x$

{% capture include_content %}
To solve for the derivative of the function, use $\eref{eq:derivative of sin}$,

$$
\begin{align*}
	\ddx\br{y} &= \ddx\br{\sin 5x} \\
	\dydx &= \cos{5x}\cdot \ddx\br{5x} \\
	&= \cos{5x}\cdot 5 \\
	&= 5\cos{5x}	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{2}$
Determine the second derivative of the function
$y = \cos(3-2x)$

{% capture include_content %}
<!-- We can utilize differential formulas to differentiate functions and still get the same result as differentiating them.  -->
In this example, use $\eref{eq:derivative of cos}$,

$$
\begin{align*}
	\ddx\br{y} &= \ddx\br{\cos(3-2x)} \\
	\dydx &= -\sin(3-2x)\cdot \ddx\br{3-2x} \\
	&= -\sin(3-2x) (-2) \\
	&= 2\sin(3-2x) \\
	&= 2\sin(3-2x)
\end{align*}
$$

Then differentiate again,

$$
\begin{align*}
	\ddx\br{\dydx} &= d\brk{2\sin(3-2x)} \\
	\frac{d^2y}{dx^2} &= 2\cos(3-2x) \cdot \ddx(3-2x) \\
	&= 2\cos(3-2x) \cdot (-2) \\
	&= -4\cos(3-2x) \\
	\frac{d^2y}{dx^2} &= -4\cos(3-2x)		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}








---
$\example{3}$
Differentiate the function with respect to $\theta$: $x = \sec{2\theta}+\tan{3\theta}$

{% capture include_content %}
To solve for the derivative of the function, use $\tcAal{Equations \ref{eq:differential of sec} and \ref{eq:differential of tan}}$,

$$
\begin{align*}
	d\br{x} &= d\br{\sec{2\theta}+\tan{3\theta}} \\
	dx &= \tan{2\theta}\sec{2\theta}\cdot d(2\theta) + \sec^2{3\theta}\cdot d(3\theta) \\
	&= \tan{2\theta}\sec{2\theta}\cdot 2\,d\theta + \sec^2{3\theta}\cdot 3\,d\theta \\
	&= \br{2\tan{2\theta}\sec{2\theta} + 3\sec^2{3\theta}}\,d\theta \\
	\frac{dx}{d\theta}&= 2\tan{2\theta}\sec{2\theta} + 3\sec^2{3\theta}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}








---
$\example{4}$
Find the derivative of $x$ with respect to $y$ of the function
$y = \tan x-x$

{% capture include_content %}
To solve for the derivative of the function, use $\eref{eq:differential of tan}$,

$$
\begin{align*}
	d(y) &= d(\tan x-x) \\
	dy &= \sec^2x\,dx-dx \\
	&= (\sec^2x-1)\,dx \\
\end{align*}
$$

From the [Pythagorean Identities](../DC-9.4-trigonometric-identities),

$$
\begin{align*}
	\tan^2{x}+1 &= \sec^2{x} \\
	\sec^2{x}-1 &= \tan^2{x}
\end{align*}
$$

Substituting this to the soultion,

$$
\begin{align*}
	dy &= \tan^2{x}\,dx \\
\end{align*}
$$

Hence,

$$
\begin{align*}
	\frac{dx}{dy} &= \frac{1}{\tan^2x} \\
	&= \cot^2x		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}









---
$\example{5}$
Differentiate the function with respect to $t$. $w = t^5\csc 4t$

{% capture include_content %}
In this example, before we can use a differential formula for trigonometric function, we first need to apply the Product Rule.

$$
\begin{align*}
	d(w) &= d(t^5 \cdot \csc{4t}) \\
	dw &= t^5 \cdot d(\csc{4t}) + \csc{4t} \cdot d(t^5) \\
	&= t^5\brk{-\cot{4t}\csc{4t}\,(4\,dt)}+\csc{4t}\,(5t^4\,dt) \\
	&= \brk{-4t^5\cot{4t}\csc{4t}+5t^4\csc{4t}}\,dt \\
	\frac{dw}{dt} &= 5t^4\csc{4t}-4t^5\cot{4t}\csc{4t}	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{6}$
Find the differential of the function $v = \sec^2\br{\frac{x}{6}}$

{% capture include_content %}
In this example, we can recall that $\sec^2\br{\frac{x}{6}}$ can also be expressed as $\brk{\sec\br{\frac{x}{6}}}^2$. With this in mind, we can use the power rule to differentiate the function.

$$
\begin{align*}
	d(v) &= d\brk{\brk{\sec\br{\frac{x}{6}}}^2} \\
	&= 2\sec\br{\frac{x}{6}} \cdot d\brk{\sec\br{\frac{x}{6}}} \\
	&= 2\sec\br{\frac{x}{6}} \cdot \brk{\tan\br{\frac{x}{6}}\sec\br{\frac{x}{6}} \cdot d\br{\frac{x}{6}}} \\
	&= 2\sec\br{\frac{x}{6}} \cdot \brk{\tan\br{\frac{x}{6}}\sec\br{\frac{x}{6}} \cdot \frac{1}{6}\, dx} \\
	&= \frac{1}{3} \tan\br{\frac{x}{6}}\sec^2\br{\frac{x}{6}} \,dx
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}








---
$\example{7}$
Let $a$ be hold constant. Determine the third derivative of the function $y = \cos ax$

{% capture include_content %}

In this example, $a$ is treated as a constant. Thus,

$$
\begin{align*}
	d(y) &= d(\cos ax) \\
	dy &= -\sin ax \cdot d(ax) \\
	&= -\sin ax \cdot a\,dx \\
	&= -a\sin ax\,dx \\
\end{align*}
$$

Then differentiate again,

$$
\begin{align*}
	d(dy) &= d(-a\sin ax\,dx) \\
	d^2y &= -a\cos ax\,dx \cdot(a\,dx) \\
	&= -a^2\cos ax\,dx^2
\end{align*}
$$

And differentiating for the last time,

$$
\begin{align*}
	d(d^2y) &= d(-a^2\cos ax\,dx^2) \\
	d^3y &= -(-a^2\sin ax\,dx^2) \cdot(a\,dx) \\
	&= a^3\sin ax\,dx^3 \\
	\frac{d^3y}{dx^3} &= a^3\sin ax		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{8}$
Determine the $y'$ of the function $s = \sec(\sin t)$

{% capture include_content %}
To evaluate this example, use the chain rule.

$$
\begin{align*}
	d(s) &= d(\sec(\sin t)) \\
	ds &= \tan(\sin t)\sec(\sin t) \cdot d(\sin t) \\
	&= \tan(\sin t)\sec(\sin t)\cos t \,dt \\
	\frac{ds}{dt} &= \tan(\sin t)\sec(\sin t)\cos t		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}








---
$\example{9}$
Let $A$, $B$, and $k$ be constants. From the function $y = A\cos kx+B\sin kx$, show that $\frac{d^2y}{dx^2} = -k^2x$.

{% capture include_content %}
Differentiate the function twice.

$$
\begin{align*}
	d(y) &= d(A\cos kx+B\sin kx) \\
	dy &= A(-\sin kx) (k\,dx) + B\cos kx (k\,dx) \\
	&= \br{-Ak\sin kx + Bk\cos kx}\,dx \\
	d(dy) &= d\brk{\br{-Ak\sin kx + Bk\cos kx}\,dx} \\
	d^2y &= \brk{-Ak\cos kx (k\,dx) + Bk(-\cos kx)(k\,dx) } \,dx \\
	&= \br{-Ak^2\cos kx - Bk^2\cos kx } \,dx^2 \\
	\frac{d^2y}{dx^2}&= -Ak^2\cos kx - Bk^2\cos kx \\
	&= -k^2\br{Ak^2\cos kx + B\cos kx} \\
\end{align*}
$$

Since $y = A\cos kx+B\sin kx$,

$$
\begin{align*}
	\frac{d^2y}{dx^2}&= -k^2y		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}