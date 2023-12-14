---
title: "Logarithmic Functions"
prevcontenturl: ../DC-8.1-exponential-functions
nextcontenturl: ../DC-8.3-derivatives-of-exponential-and-logarithmic-functions
---




Logarithms are the inverse of exponentials. This can be useful in solving for the exponent of an equation in the form $x=b^y$ or vice versa since the exponential function $x=b^y$ can be written in the form of a logarithmic function $y=\log_{b}x$.

{% include tcolorbox.html
    details = "
	    y=\log_{b}x \quad\text{is equivalent to}\quad x=b^y
    "
%}

Where $b$ is any number given that $b>0$ and $b \neq 1$. And $y=\log_{b}x$ is usually read as "log base $b$ of $x$"

If you recall the methods in solving for the inverse of a function, let us attempt to solve the inverse of the exponential function $f(x)=b^x$,

$$
\begin{align*}
	f(x) &= b^x \\
	y &= b^x 	&&		\tcA{\text{replace $f(x)$ with $y$}} \\
	x &= b^y 	&&		\tcA{\text{switch $x$ and $y$}} \\
	y &= \log_b{x} 	&&	\tcA{\text{solve for $y$}} \\
	f^{-1}(x) &= \log_b{x}
\end{align*}
$$


Hence, this proves that Exponential and Logarithmic Functions are indeed inverses of each other.






---
$\example{1}$
Solve for $x$ if $\log_{10} x =2$

{% capture include_content %}
Express the logarithmic function as an exponential function,

$$
\begin{align*}
	\log_{10} x &= 2 \\
	x &= 10^2 	\quad \tcA{\log_b x = y \;\tcB{\Rightarrow}\; x=b^y} \\
	&= 100		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---

## Common Logarithm (Briggsian Logarithm)

Common Logarithm is a type logarithm whose base is 10 and is the inverse of the exponential function $10^x$. It is abbreviated as "log" which means the same as "$\log_{10}$". The function $x= 10^y$ can be expressed in the logarithmic form $y=\log_{10}x$ which can also be written as $y=\log{x}$.


{% include tcolorbox.html
    details = "
        \log{x} = \log_{10}x
    "
%}





## Natural Logarithm (Napierian Logarithm)
	
Natural logarithm is a type logarithm whose base is $e$ (Euler's number) and is the inverse of the exponential function $e^x$. It is abbreviated as "ln" which means the same as "$\log_{e}$". The function $x=e^y$ can be expressed in the logarithmic form $y=\log_{e}x$ which can also be written as $y=\ln{x}$.


{% include tcolorbox.html
    details = "
	    \ln{x} = \log_{e}x
    "
%}

### Properties of Common and Natural Logarithm

{% include minibox.html
    details = "
    $\tcBal{Properties of Common Logarithms}$ 
    $$
    \begin{align}
        \log⁡(xy) &= \log ⁡x + \log ⁡y \\
		\log⁡\br{\frac{x}{y} } &= \log ⁡x - \log ⁡y \\
		\log⁡ x^n &= n \log ⁡x \\
		\log_y⁡x &= \frac{\log⁡ x}{\log⁡ y} \\
		\log_x⁡ x &= 1 \\
		\log⁡ 1 &= 0 \\
		y^{\log_{y⁡}x} &= x \\
		\log⁡ 0 &= -\infty
    \end{align}
    $$
    "
%}


{% include minibox.html
    details = "
    $\tcBal{Properties of Natural Logarithms}$ 
    $$
    \begin{align}
        \ln⁡(xy) &= \ln ⁡x + \ln ⁡y \\
		\ln\br{ ⁡\frac{x}{y} } &= \ln ⁡x - \ln ⁡y \\
		\ln⁡ x^n &= n \ln ⁡x \\
		\log_y⁡x &= \frac{\ln⁡ x}{\ln⁡ y} \\
		\ln e &= 1 \\
		\ln⁡ 1 &= 0 \\
		e^{\ln x} &= x \\
		\ln 0 &= -\infty
    \end{align}
    $$
    "
%}













---
$\example{2}$
Solve for $x$: $\log_4(x+3) = 2$	

{% capture include_content %}
Express the logarithmic function in an exponential form,

$$
\begin{align*}
	\log_4(x+3) &= 2 \\
	x+3 &= 4^2 	\quad\quad \tcA{\log_b x = y \;\tcB{\Rightarrow}\; x=b^y} \\
	x &= 16-3 \\
	&= 13	\tagans
\end{align*}
$$	

{% endcapture %}
{% include solution.html details = include_content %}






---
$\example{3}$
Solve for $x$: $\log_{5}(x+3)+\log_{5}5 = 2$

{% capture include_content %}
Combine the terms that contains logarithms,

$$
\begin{align*}
    \log_{5}(x+3)+\log_{5}5 &= 2 \\
    \log_{5}[5(x+3)] &= 2	\quad \tcA{\log(xy)=\log{x} + \log{y}} \\
    5(x+3) &= 5^2 \\
    5x + 15 &= 25 \\
    x &= 2	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}








---
$\example{4}$
Solve for $x$: $\ln x = \ln\frac{1}{2}+\ln 2-\ln 3$

{% capture include_content %}
Combine the terms for each side of the equation that contains logarithms.

$$
\begin{align*}
	\ln x &= \ln\frac{1}{2}+\ln 2-\ln 3 \\
	&= \ln\br{\frac{\frac12 \cdot 2}{3}} \qquad\tcA{\ln\br{\frac{x}{y}} = \ln x - \ln y} \\
	\ln x &= \ln\frac{1}{3}	
\end{align*}
$$

Raise both sides to a power with base $e$,

$$
\begin{align*}
	e^{\ln{x}}	&= e^{\ln\frac13}	\qquad\qquad\quad\tcA{e^{\ln x} = x} \\
	x &= \frac{1}{3} \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{5}$
Solve for $x$: $\ln{x} = 2\ln{3}-\ln{e}$

{% capture include_content %}

$$
\begin{align*}
	\ln{x} &- 2\ln{3} - \ln{e} \\
	&= \ln{3^2}-\ln{e}		\quad\tcA{\ln{x^n} = n\ln x} \\
	&= \ln\frac{3^2}{e} \\
	e^{\ln x} &= e^{\ln\frac{9}{e}} \\
	x &= \frac{9}{e} \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}










---
$\example{6}$
Solve for $x$: $\ln(x+6)+\ln(2-x) = \ln 15$

{% capture include_content %}

$$
\begin{align*}
	\ln(x+6)+\ln(2-x) &= \ln 15 \\
	\ln[(x+6)(2-x)] &= \ln{15} \\
	\ln(-x^2-4x+12) &= \ln{15} \\
	e^{\ln(-x^2-4x+12)} &= e^{\ln{15}} \\
	-x^2-4x+12 &= 15 \\
	x^2+4x+3 &= 0
\end{align*}
$$

Then factor the equation,

$$
\begin{align*}
	(x+3)(x+1) &= 0
\end{align*}
$$

Thus,

$$
\begin{align*}
	x+3 &= 0    &   x+1 &= 0 \\
	x &= -3 &   x &= -1     \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}









---
$\example{7}$
Solve for $x$: $2^x = 3$

{% capture include_content %}
Express the exponential function in a logarithmic form,

$$
\begin{align*}
	2^x &= 3 \\
	x &= \log_{2}3  \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{8}$
Solve for $x$: $3^{5x} = 4^{2x+1}$

{% capture include_content %}
Get the natural logarithm of both sides of the equation,

$$
\begin{align*}
	3^{5x} &= 4^{2x+1} \\
	\ln(3^{5x}) &= \ln(4^{2x+1}) \\
	5x \ln{3} &= (2x+1)\ln{4} \\
	5x \ln{3} &= 2x \ln{4} + \ln{4} \\
	x( 5 \ln{3} - 2 \ln{4} ) &= \ln{4} \\
	x &= \frac{\ln{4}}{5 \ln{3} - 2 \ln{4}} \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}








---
$\example{9}$
Solve for $x$: $e^x-6e^{-x} = -1$

{% capture include_content %}
To remove the negative exponent, multiply both sides of the equation by $e^x$,

$$
\begin{align*}
	e^x-6e^{-x} &= -1 \\
	e^x (e^x-6e^{-x}) &= e^x(-1) \\
	e^{2x}-6 &= -e^x \\
	e^{2x}+e^x-6 &= 0
\end{align*}
$$

The factor the equation,

$$
\begin{align*}
	(e^x+3)(e^x-2) &= 0
\end{align*}
$$

Thus,

$$
\begin{align*}
	x+3 &= 0    &   x-2 &= 0 \\
	x &= -3 &   x &= 2      \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}