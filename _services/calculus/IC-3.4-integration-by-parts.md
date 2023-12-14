---
title: "Integration by Parts"
authornum: 2
author: Engr. Nico O. Aspra, M.Eng., RMP, LPT  <br> Engr. Pee Jay N. Gealone
prevcontenturl: ../IC-3.3-trigonometric-functions
nextcontenturl: ../IC-3.5-tabular-integration-by-parts
---





Integration by parts is a method of integration that can be used to evaluate integrals of a **product of two functions** that cannot be solved using the basic formulas of integration, which we have discussed from our previous lessons.

The formula for Integration by Parts is derived from the differential of the product of two functions. Consider $\eref{eq:diff of products of two functions, by parts}$, where $u$ and $dv$ are both functions of $x$.

$$
\begin{align}
	d(uv) &= u\,dv+v\,du \label{eq:diff of products of two functions, by parts}
\end{align}
$$

Then integrate the equation,

$$
\begin{align}
	\int d(uv) &= \int\br{u\,dv+v\,du} \nonumber \\
	uv &= \int u\,dv+ \int v\,du \nonumber
\end{align}
$$

Hence, rearranging the function gives us the **formula for the Integration by Parts**, which is,

{% include tcolorbox.html
    details = "
        \int u\,dv = uv - \int v\,du
        \label{eq:integration by parts}
    "
%}

However, we need to remember that we would only resort to integration by parts if all of the methods from the previous lessons can no longer be used to evaluate the integral.



---
$\example{1}$
Evaluate the integral $\int x^2\ln x \,dx$

$\solution$ \\
In using the formula for integration by parts, we must first choose the $u$ and $dv$ from the integrand. The $u$ from the two functions when differentiated must be simpler than $u$ itself, and the $dv$ must be a function that can be easily integrated. In this example, the logarithmic function "$\ln x$'' is simpler to differentiate than to integrate. Thus, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= \ln x &  dv &= x^2\,dx &&&&&&&\\
\end{align*}
$$

But in order to use the formula, we still need $du$ and $v$. To solve for $du$, differentiate $u$; and for $v$, integrate $dv$, \\
$$
\begin{align*}
	\phantom{Let:-} d(u) &= d(\ln x) &  \int dv &= \int x^2\,dx \\
	du &= \frac{1}{x}\,dx & v &= \frac{x^3}{3}
\end{align*}
$$

Then substituting to $\eref{eq:integration by parts}$ gives us,

$$
\begin{align*}
	\int x^2\ln x \,dx &= uv-\int v\,du \\
        &= \ln x \cdot \frac{x^3}{3} - \int \frac{x^3}{3} \cdot \frac{1}{x}\,dx \\
        &= \frac{x^3}{3} \ln x - \frac13\int x^2\,dx \\
        &= \frac{x^3}{3} \ln x - \frac13 \cdot \frac{x^3}{3}+C \\
        &= \frac{x^3}{3} \ln x - \frac{x^3}{9}+C		\tagans
\end{align*}
$$


---

**LIATE** is an acronym that can be used to help in choosing the $u$ and $dv$ from the integral to be evaluated. Whichever comes first out of the list from the two functions of the integral must be the $u$.

$$
\begin{array}{cl}
    \textbf{L} & \text{Logarithmic Functions} \\
    \textbf{I} & \text{Inverse Trigonometric Functions} \\
    \textbf{A} & \text{Algebraic Functions} \\
    \textbf{T} & \text{Trigonometric Functions} \\
    \textbf{E} & \text{Exponential Functions}
\end{array}
$$

From the previous example, the integral is composed of logarithmic and algebraic functions, since logarithmic function comes first before the algebraic function based from the acronym LIATE, hence, "$\ln x$'' must be the $u$ and the algebraic function "$x^2$'' be the $dv$.


---
$\example{2}$
Evaluate the integral $\int x e^x\,dx$

$\solution$ \\
Since $x$ is an algebraic function and $e^x$ is an exponential function, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= x &  dv &= e^x\,dx &&&&&&&\\
	du &= dx & v &= e^x
\end{align*}
$$

Thus,

$$
\begin{align*}
	\int x e^x\,dx &= xe^x-\int e^x\,dx \\
	&= xe^x-e^x+C	\tagans
\end{align*}
$$




---
$\example{3}$
Evaluate the integral $\int \ln(\sin x)\cos x\,dx$

$\solution$ \\
Since $\ln(\sin x)$ is a logarithmic function and $\cos x$ is a trigonometric function, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= \ln(\sin x) &  dv &= \cos x\,dx &&&&&&&\\
	du &= \frac{\cos x}{\sin x}\,dx & v &= \sin x
\end{align*}
$$

Thus,

$$
\begin{align*}
	\int \ln(\sin x)\cos x\,dx &= \ln(\sin x)\cdot\sin x - \int \cancel{\sin x} \cdot \frac{\cos x}{\cancel{\sin x}}\,dx \\
	&= \ln(\sin x)\cdot\sin x - \int \cos x\,dx \\
	&= \ln(\sin x)\cdot\sin x - \sin x + C		\tagans
\end{align*}
$$



---
$\example{4}$
Evaluate the integral $\int x^3\sqrt{x^2+2}\,dx$

$\solution$ \\
In this case, both functions are algebraic hence the acronym cannot be used to determine the $u$ and $dv$ of the integral. But by inspection, $x\sqrt{x^2+2}\,dx$ can be integrated by using the power formula so let this be the $dv$ and $x^2$, which will be the remaining factor of the integrand be the $u$.

$$\int x^3\sqrt{x^2+2}\,dx = \int x^2\cdot x\sqrt{x^2+2}\,dx$$

$$
\begin{align*}
	\text{Let:}\qquad u &= x^2 &  dv &= x\sqrt{x^2+2}\,dx &&&&&&&\\
	du &= 2x\,dx & v &= \int x\sqrt{x^2+2}\,dx \\
	&&&= \int x\br{x^2+2}^{1/2} \,dx \\
	&&&= \frac12 \int x\br{x^2+2}^{1/2} (2x\,dx) \\
	&&&= \frac{1}{2}\cdot\frac{3}{2}(x^2+2)^{3/2} \\
	&&v&= \frac{1}{3}(x^2+2)^{3/2} \\
\end{align*}
$$

Thus, 

$$
\begin{align*}
	\int x^3\sqrt{x^2+2}\,dx &= x^2 \cdot \frac{1}{3}(x^2+2)^{3/2} - \int \frac{1}{3}(x^2+2)^{3/2} \cdot 2x\,dx \\
	&= \frac13 x^2(x^2+2)^{3/2}-\frac13\int(x^2+2)^{3/2}(2x\,dx) \\
	&= \frac13 x^2(x^2+2)^{3/2}-\frac13\cdot\frac{(x^2+2)^{5/2}}{5/2}+C \\
	&= \frac13 x^2(x^2+2)^{3/2}-\frac{2}{15}(x^2+2)^{5/2}+C		\tagans
\end{align*}
$$



---
$\example{5}$
Evaluate the integral $\int x^2 \sin x \,dx$

$\solution$ \\
Since $x^2$ is an algebraic function and $\sin x$ is a trigonometric function, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= x^2 &  dv &= \sin\,dx &&&&&&&\\
	du &= 2x\,dx & v &= -\cos{x}
\end{align*}
$$

$$
\begin{align*}
	\int x^2 \sin x\,dx &= -x^2\cos{x}-\int(-\cos{x}\cdot 2x\,dx) \\
	&= -x^2\cos{x} + 2\int x\cos{x} \,dx
\end{align*}
$$

We still cannot integrate $\int x\cos{x}\,dx$ using the basic integration formulas, thus we can again use integration by parts for the second time, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= x &  dv &= \cos\,dx &&&&&&&\\
	du &= dx & v &= \sin{x}
\end{align*}
$$

$$
\begin{align*}
	\int x^2 \sin x\,dx &= -x^2\cos{x} + 2\brk{ x\sin{x} - \int \sin{x}\,dx } \\
	&= -x^2\cos{x} + 2\brk{ x\sin{x} - (-\cos{x}) } + C \\
	&= -x^2\cos{x} + 2x\sin{x} +2\cos{x}+ C		\tagans
\end{align*}
$$



---
$\example{6}$
Evaluate the integral $\int x^3 (\ln x)^2 \,dx$

$\solution$ \\
Since $(\ln x)^2$ is a logarithmic function and $x^3$ is an algebraic function, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= (\ln x)^2 &  dv &= x^3\,dx &&&&&&&\\
	du &= 2\ln{x}\cdot\frac{dx}{x} & v &= \frac{x^4}{4} \\
	&= \frac{2\ln{x}}{x}\,dx
\end{align*}
$$

$$
\begin{align*}
	\int x^3 (\ln x)^2 \,dx &= \frac{x^4}{4}(\ln x)^2 - \int \frac{x^4}{4}\cdot\frac{2\ln{x}}{x}\,dx \\
	&= \frac{x^4}{4}(\ln x)^2 - \frac12\int x^3\ln{x}\,dx \\
\end{align*}
$$

In this case, $\int x^3\ln{x}\,dx$ still needs integration by parts. Hence, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= \ln x &  dv &= x^3\,dx &&&&&&&\\
	du &= \frac{dx}{x} & v &= \frac{x^4}{4}
\end{align*}
$$

$$
\begin{align*}
	\int x^3 (\ln x)^2 \,dx &= \frac{x^4}{4}(\ln x)^2 - \frac12\brk{ \frac{x^4}{4}\ln{x} - \int \frac{x^4}{4}\cdot\frac{dx}{x} } \\
	&= \frac{x^4}{4}(\ln x)^2 - \frac12\brk{ \frac{x^4}{4}\ln{x} - \frac14\int x^3\,dx } \\
	&= \frac{x^4}{4}(\ln x)^2 - \frac12\brk{ \frac{x^4}{4}\ln{x} - \frac14\cdot\frac{x^4}{4} } + C \\
	&= \frac{x^4}{4}(\ln x)^2 - \frac{x^4}{8}\ln{x} + \frac{x^4}{32} + C		\tagans
\end{align*}
$$

---
$\example{7}$
Evaluate the integral $\int e^x\sin x\,dx$

$\solution$ \\
Since $\sin{x}$ is a trigonometric function and $e^x$ is an exponential function, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= \sin{x} &  dv &= e^x\,dx &&&&&&&\\
	du &= \cos{x}\,dx & v &= e^x
\end{align*}
$$

$$\int e^x\sin x\,dx = e^x\sin{x}-\int e^x\cos{x}\,dx$$

$\int e^x\cos{x}\,dx$ still needs integration by parts. Hence, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= \cos{x} &  dv &= e^x\,dx &&&&&&&\\
	du &= -\sin{x}\,dx & v &= e^x
\end{align*}
$$

$$
\begin{align*}
	\int e^x\sin x\,dx &= e^x\sin{x}-\brk{ e^x\cos{x}-\int e^x(-\sin{x}\,dx) } \\
	&= e^x\sin{x}-e^x\cos{x}-\int e^x\sin{x}\,dx 
\end{align*}
$$

In this case, the original integral appears again. If this happens, we no longer need to perform another integration by parts, rather we can transpose the integral that have appeared to the other side, which can then be combined to the original integral. Hence, simplifying the function would be a much more straightforward solution.

$$
\begin{align*}
\int e^x\sin x\,dx+\int e^x\sin x\,dx &= e^x\sin{x}-e^x\cos{x}+C \\
	2\int e^x\sin x\,dx &= e^x\sin{x}-e^x\cos{x}+C \\
	\int e^x\sin x\,dx &= \frac12\br{e^x\sin{x}-e^x\cos{x}}+C		\tagans
\end{align*}
$$



---
$\example{8}$
Evaluate the integral $\int 3^x x\,dx$

$\solution$ \\
Since $x$ is a algebraic function and $3^x$ is an exponential function, \\
$$
\begin{align*}
	\text{Let:}\qquad u &= x &  dv &= 3^x\,dx &&&&&&&\\
	du &= dx & v &= \frac{3^x}{\ln{3}}
\end{align*}
$$

$$
\begin{align*}
	\int 3^x x\,dx &= x\cdot\frac{3^x}{\ln{3}} - \int \frac{3^x}{\ln{3}}\,dx \\
	&= \frac{3^x x}{\ln 3}-\frac{1}{\ln3}\int 3^x\,dx \\
	&= \frac{3^x x}{\ln 3}-\frac{1}{\ln3}\cdot\frac{3^x}{\ln{3}}+C \\
	&= \frac{3^x x}{\ln 3}-\frac{3^x}{\ln^2{3}}+C		\tagans
\end{align*}
$$