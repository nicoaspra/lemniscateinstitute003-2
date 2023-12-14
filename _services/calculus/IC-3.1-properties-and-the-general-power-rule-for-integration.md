---
title: "Properties and the General Power Rule for Integration"
authornum: 2
author: Engr. Nico O. Aspra, M.Eng., RMP, LPT  <br> Engr. Pee Jay N. Gealone
weight: 2
layout: content
prevcontenturl: ../IC-1.4-antiderivatives
nextcontenturl: ../IC-3.2-exponential-and-logarithmic-functions
---


## Introduction
In the previous lesson, we have established that integration (indefinite integral in particular) is simply the reverse of differentiation. Hence, this lesson will investigate the general power rule, which is one of the most common and valuable basic integration processes. 

The general power rule for integration can be associated as the inverse of the general power rule for differentiation.
You can also have an in-depth review of the power rule for differentiation before starting this lesson for a deeper understanding of the topic.

## Properties of Indefinite Integral
Before we start our discussion with the general power rule, let us first introduce the properties of indefinite integrals. These properties are a prerequisite before introducing the different processes of applying integration techniques in a differential function. 

For the following formulas for evaluating indefinite integrals, let $u$, $v$ and $w$ be a function of $x$; $a$ and $n$ as constants; and $C$ as the constant of integration.

{% include tcolorbox.html
    details = "
        \int du &= u+C \\
        \int a\,du &= a\int du \\
        \int (du\pm dv\pm dw) &= \int du \pm \int dv \pm \int dw
    "
%}



## The General Power Rule for Integration
If you could recall, the steps in differentiating using the power rule include **multiplying the exponent $n$ of the variable to the term** then **reducing the value of the exponent by one** ($n-1$). However, in integration, it is the reverse of that. The first step is **adding one to the exponent** ($n+1$), then dividing the whole term with the same value of the variable's new exponent ($n+1$). The equation below, shows the formula described.

{% include tcolorbox.html
    details = "
        \int u^n \,du = \frac{u^{n+1}}{n+1} + C \quad\text{where: $n\neq -1$}
    "
%}



<!-- - Assuming that you have already reviewed the concepts of differentials, we can observe that the general power formula for differentials follows two basic steps: (1) multiplying the function with the original exponent $n$, and (2) subtracting one from the original exponent $n$. Interestingly, it can be observed that we can apply anti-differentiation (integration) through \textit{reversing the steps} mentioned. Thus, for the general power rule for integration, we add one from the exponent $n$ then divide the function with the new exponent $n+1$. $\eref{eq:integration - general power rule}$ shows the formula described. -->







Let us now try some problems to illustrate the general power rule for integration.

---
$\example{1}$
Evaluate the integral: $\int x^3 \,dx$

$\solution$ \\
$$
\begin{align*}
	\int x^3 \,dx &= \frac{x^{3+1}}{3+1}+C \\
	&= \frac{x^4}{4}+C	\tagans
\end{align*}
$$




---
$\example{2}$
Evaluate the integral: $\int (2y^3-3y^2+1) \,dy$

$\solution$ \\
$$
\begin{align*}
	\int (2y^3-3y^2+1) \,dy &= \int 2y^3 \,dy - \int 3y^2 \,dy + \int 1 \,dy \\
	&= 2\int y^3 \,dy - 3\int y^2 \,dy + \int dy \\
	&= 2\cdot\frac{y^{3+1}}{3+1}-3\cdot\frac{y^{2+1}}{2+1}+\frac{y^{0+1}}{0+1}+C  \qquad\tcA{y^0=1}\\
	&= 2\cdot\frac{y^4}{4}-\cancel{3}\cdot\frac{y^3}{\cancel{3}}+\frac{y}{1}+C \\
	&= \frac{y^4}{2}-y^3+y+C	\tagans
\end{align*}
$$




---
$\example{3}$
Evaluate the integral: $\int \br{5x^{-2}+\frac{2}{x^3}-3\sqrt{x}} \,dx$

$\solution$ \\
$$
\begin{align*}
	\int \br{5x^{-2}+\frac{2}{x^3}-3\sqrt{x}} \,dx &= \int \br{5x^{-2}+2x^{-3}-3x^{1/2}} \,dx \\
	&= \frac{5x^{-2+1}}{-2+1}+\frac{2x^{-3+1}}{-3+1}-\frac{3x^{\frac12+1}}{\frac12+1}+C \\
	&= \frac{5x^{-1}}{-1}+\frac{\cancel{2}x^{-2}}{-\cancel{2}}+\frac{\cancel{3}x^{3/2}}{\cancel{3}/2}+C \\
	&= -\frac{5}{x}-\frac{1}{x^2}+2x^{3/2}+C 		\tagans
\end{align*}
$$



---
$\example{4}$
Evaluate the integral: $\int \frac{3\sqrt{x}+2x^3}{x} \,dx$

$\solution$ \\
If the case where the integrand is a fraction, where the numerator can be divided by the denominator,

$$
\begin{align*}
	\int \frac{3\sqrt{x}+2x^3}{x} \,dx &= \int \frac{3x^{1/2}+2x^3}{x} \,dx \\
	&= \int \br{\frac{3x^{1/2}}{x}+\frac{2x^3}{x}} \,dx \\
	&= \int \br{3x^{-1/2}+2x^2} \,dx \\
	&= \frac{3x^{1/2}}{1/2}+\frac{2x^3}{3}+C \\
	&= 6\sqrt{x}+\frac23x^3+C 		\tagans
\end{align*}
$$



---
$\example{5}$
Evaluate the integral: $\int (5x-2)^3 \,dx$

$\solution$ \\
If we have encountered this type of problem while differentiating, we would probably use the chain rule. But in integration, we must first make sure that the integrand follows the format of the formulas of integration, which in this case is the ``General Power Rule for Integration''. To simplify the integral, let $5x-2$ be represented by a variable,

Let: $u = 5x-2 $

Then,

$$\int (5x-2)^3 \,dx = \int u^3 dx$$

However, in performing integration, the integrand must contain a uniform variable. In this case, we need to express all the variables in terms of $u$. Thus, even $dx$ must be replaced, to do that, we can first solve for the differential of $u$. Hence,

$$
\begin{align*}
    d(u) &= d(5x-2) & \\
	du &= 5\,dx \\
	dx &= \frac15 du
\end{align*} 
$$

Thus,

$$
\begin{align*}  
    \int (5x-2)^3 \,dx &= \int u^3 \br{\frac15 du} \\
	&= \frac15 \int u^3\,du \\
	&= \frac15\br{\frac{u^4}{4}}+C \\
	&= \frac{u^4}{20}+C
\end{align*}
$$

But $u=5x-2$,

$$
\begin{align*} 
	\int (5x-2)^3 \,dx &= \frac{(5x-2)^4}{20}+C	\tagans
\end{align*}
$$



---
$\example{6}$
Evaluate the integral: $\int x\sqrt{2x^2-7} \,dx$

$\solution$ \\
In this example, to simplify the integral, we can replace the function inside the square root by a variable $u$. Furthermore, to simplify the process, we can immediately solve for its differential before replacing the previous variable to the integrand.

Let:

$$
\begin{align*}
	\quad u &= 2x^2-7 & \\
	du &= 4x \,dx  \\
	x\,dx &= \frac14 du
\end{align*}
$$

$$
\begin{align*}
	\int x\sqrt{2x^2-7} \,dx &= \int x(2x^2-7)^{1/2}\,dx \\
	&= \int (2x^2-7)^{1/2} \br{x\,dx} \\
	&= \int u^{1/2} \br{\frac14 du} \\
	&= \frac14\br{\frac{u^{3/2}}{3/2}}+C \\
	&= \frac{2u^{3/2}}{12}+C \\
	&= \frac{u^{3/2}}{6}+C \\
\end{align*}
$$

Since $u=2x^2-7$,

$$
\begin{align*}
	\int x\sqrt{2x^2-7} \,dx &= \frac{(2x^2-7)^{3/2}}{6}+C	\tagans
\end{align*}
$$


