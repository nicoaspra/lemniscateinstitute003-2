---
title: "Antiderivatives"
authornum: 2
author: Engr. Nico O. Aspra, M.Eng., RMP, LPT  <br> Engr. Pee Jay N. Gealone
weight: 2
layout: content
prevcontenturl: ../IC-1.3-definite-and-indefinite-integrals
nextcontenturl: ../IC-3.1-properties-and-the-general-power-rule-for-integration
---



The **Antiderivative** of a function is a result of *reversing the process of differentiation*. And **Antidifferentiation**, also known as **Integration**, is the process of solving for the antiderivative of a function. Consider the equation, 

$$F'(x) = f(x)$$

In Differential Calculus, the tick symbol is the Lagrange's notation which denotes differentiation. With this in mind, the derivative of the function $F(x)$ is $f(x)$. Hence, in reverse, the Antiderivative of the function $f(x)$ is $F(x)$.

The relationship of the function represented with integration is denoted as,
{% include tcolorbox.html
	details = "
        \int f(x) \,dx = F(x)+C
        "
%}

Where $\textstyle{\int}$ is called the **integral symbol**, $dx$ indicates that the function $f(x)$ is to be integrated with respect to the variable $x$, and the function $f(x)$ that is to be integrated is called the **integrand**.

For example, solve for the derivative of the following functions, \\
**a.** $y = x^2+1$ \\
**b.** $y = x^2-3$ \\
**c.** $y = x^2+\pi$ \\
**d.** $y = x^2+c$, where $c$ is any constant


$\solution$ \\
$\For{a}$ \\
Differentiate the function,

$$
\begin{align*}
	\ddx\br{y} &= \ddx\br{x^2+1} \\
	\dydx &= 2x	\tagans
\end{align*}
$$


$\For{b}$ \\
Differentiate the function,

$$
\begin{align*}
	\ddx\br{y} &= \ddx\br{x^2-3} \\
	\dydx &= 2x	\tagans
\end{align*}
$$


$\For{c}$ \\
Differentiate the function,

$$
\begin{align*}
	\ddx\br{y} &= \ddx\br{x^2+\pi} \\
	\dydx &= 2x	\tagans
\end{align*}
$$


$\For{d}$ \\
Differentiate the function,
$$
\begin{align*}
	\ddx\br{y} &= \ddx\br{x^2+c} \\
	\dydx &= 2x	\tagans
\end{align*}
$$


By differentiating any of the given functions, all of it would result to $2x$, since the derivative of any constant is just equal to zero and 1, $-3$, $\pi$, and $c$ are all constants. With this in mind, by reversing the method, we can no longer determine the exact value of the constant that was lost during differentiation, so in order to represent that constant, we will use an arbitrary constant $C$. Hence, the antiderivative of $2x$ is $x^2+C$, which can be denoted as, 
$$\int 2x \,dx = x^2+C$$









---
$\example{1}$
Verify the equation by differentiating the antiderivative: $\int 20 \,dx = 20x+C$

$\solution$ \\
Differentiating the antiderivative,

$$
\begin{align*}
	\ddx\br{20x+C} &= 20
\end{align*}
$$

Hence, the equation is $\tcAal{correct}$.




---
$\example{2}$
Verify the equation by differentiating the antiderivative: \\
$\int\br{3x^2+10x^4-\frac{8}{x^3}} \,dx = x^3+2x^5-\frac{4}{x^2}+C$

$\solution$\\
Differentiating the antiderivative,

$$
\begin{align*}
	\ddx\br{x^3+2x^5-\frac{4}{x^2}+C} &= \ddx\br{x^3+2x^5-4x^{-2}+C} \\
	&= 3x^2+(5)2x^4-(-2)4x^{-3} \\
	&= 3x^2+10x^4+8x^{-3} \\
	&= 3x^2+10x^4+\frac{8}{x^3} \\
\end{align*}
$$

Hence, the equation is $\tcAal{incorrect}$.




---
$\example{3}$
Verify the equation by differentiating the antiderivative: \\
$\int\br{y^{3/2}+2\sqrt{y}} \,dy = \frac25y^{5/2}+\frac23y^{3/2}+C$

$\solution$ \\
Differentiating the antiderivative,

$$
\begin{align*}
	\ddy\br{\frac25y^{5/2}+\frac23y^{3/2}+C} &= \br{\frac52}\frac25y^{\frac52-\frac22}+\br{\frac32}\frac23y^{\frac32-\frac22} \\
	&= y^{3/2}+y^{1/2} \\
	&= y^{3/2}+\sqrt{y} \\
\end{align*}
$$

Hence, the equation is $\tcAal{incorrect}$.




---
$\example{4}$
Verify the equation by differentiating the antiderivative: \\
$\displaystyle{\int\br{\frac{15t^2-6t+2}{2\sqrt{5t^3-3t^2+2t+1}}} \,dt = \sqrt{5t^3-3t^2+2t+1}+C}$

$\solution$ \\
Differentiating the antiderivative using the [Chain Rule](../DC-4.3-the-chain-rule),

$$
\begin{align*}
	\ddt\br{\sqrt{5t^3-3t^2+2t+1}+C} &= \ddt\br{(5t^3-3t^2+2t+1)^{1/2}+C} \\
    &= \frac12\br{5t^3-3t^2+2t+1}^{-1/2}  \cdot \ddt\br{5t^3-3t^2+2t+1} \\
	&= \frac{1}{2\br{5t^3-3t^2+2t+1}^{1/2}} \cdot \br{15t^2-6t+2} \\
	&= \frac{15t^2-6t+2}{2\sqrt{5t^3-3t^2+2t+1}}
\end{align*}
$$

Hence, the equation is $\tcAal{correct}$.