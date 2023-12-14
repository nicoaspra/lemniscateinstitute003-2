---
title: "Properties of Limits"
prevcontenturl: ../DC-2.1-introduction-to-limits
nextcontenturl: ../DC-2.3-limits-at-infinity
---


In this lesson, we will now be solving for limits. However, in order for us to simplify the solutions, we must first look at the different basic properties of limits. Below are some of the commonly used properties.




$\thrm{Property 1:}$
The limit of any **constant** is equal to the constant.

{% include tcolorbox.html
    details = "
		\lim_{x \to a} {c} = c
    "
%}

$\thrm{Property 2:}$
The limit of the **product of a constant and a function** is equal to the product of the constant and the limit of the function.

{% include tcolorbox.html
    details = "
		\lim_{x \to a} {c \,f(x)}= c \lim_{x \to a} f(x)
    "
%}
	
		
$\thrm{Property 3:}$
The limit of the **sum or difference** of two or more functions is equal to the sum or difference of their limits.

{% include tcolorbox.html
    details = "
		\lim_{x \to a} \left[ f(x) + g(x) \right] = \lim_{x \to a} f(x) + \lim_{x \to a}g(x)
    "
%}
		
$\thrm{Property 4:}$
The limit of the **product of two or more functions** is equal to the product of their limits.

{% include tcolorbox.html
    details = "
		\lim_{x \to a} \left[ f(x) \cdot g(x) \right] = \lim_{x \to a}{f(x)} \cdot \lim_{x \to a}{g(x)} 
    "
%}

$\thrm{Property 5:}$
The limit of the **quotient of two or more functions** is equal to the quotient of their limits, provided the limit of the devisor is not zero.

{% include tcolorbox.html
    details = "
		\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{\lim_{x \to a} f(x) }{ \lim_{x \to a} g(x) }  , \hspace{10pt} where: \,   \lim_{x \to a} g(x) \neq 0
    "
%}

$\thrm{Property 6:}$
The limit of a **power of a function** is equal to the power of the limit.

{% include tcolorbox.html
    details = "
		\lim_{x \to a} \left[ f(x) \right] ^n =\left[ \lim_{x \to a} f(x) \right]^n
    "
%}

$\thrm{Property 7:}$
The limit of the **root of a function** is equal to the root of their limits.

{% include tcolorbox.html
    details = "
		\lim_{x \to a}{ \sqrt[n]{f(x)} } = \sqrt[n]{ \lim_{x \to a} {f(x)} }
    "
%}
		
$\thrm{Property 8:}$
The limit of $\frac{ \sin \theta }{\theta}$ as $\theta$ approaches zero is equal to 1, given that the angle $\theta$ is in radians.

{% include tcolorbox.html
    details = "
		\lim_{\theta \to 0}{\frac{ \sin \theta }{\theta}} =1 , \hspace{10pt} where: \theta \; \text{is in radians}
    "
%}





---
$\example{1}$
Evaluate: $ \lim_{x \to 2} \br{x^2+2x+3} $

{% capture include_content %}
$$
\begin{align*}
		\lim_{x \to 2} \br{x^2+2x+3} &=  \lim_{x \to 2} {x^2} +  \lim_{x \to 2} {2x} +  \lim_{x \to 2} {3} \\
		&=  \br{ \,\lim_{x \to 2} {x}}^2 +  2 \br{ \,\lim_{x \to 2} {x} } + 3 \\
		&= (2)^2+2(2)+3 \\
		&= 11		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}






---
$\example{2}$
Evaluate: $ \lim_{t \to 3} \br{t^5+10-2t^2-5t^3} $

{% capture include_content %}
$$
\begin{align*}
	\lim_{t \to 3} \br{t^5+10-2t^2-5t^3} &=  \lim_{t \to 3} {t^5} +  \lim_{t \to 3} {10} - \lim_{t \to 3} {2t^2} - \lim_{t \to 3} {5t^3} \\
		&=  \br{ \,\lim_{t \to 3} {t}}^5 + 10 - 2 \br{ \,\lim_{t \to 3} {t} }^2 - 5 \br{ \,\lim_{t\to 3} {t} }^3 \\
		&= (3)^5+10+2(3)^2+5(3)^3 \\
		&= 100		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{3}$
Evaluate: $ \lim_{x \to 1} \br{ \frac{3x^2-2}{x^3+2x^2-x+5} } $

{% capture include_content %}
$$
\begin{align*}
	\lim_{x \to 1} \br{ \frac{3x^2-2}{x^3+2x^2-x+5} }
		&=  \frac{ \lim_{x \to 1} \br{3x^2-2} }{ \lim_{x \to 1} \br{x^3+2x^2-x+5}  } \\
		&= \frac{3(1)^2-2}{(1)^3+2(1)^2-(1)+5} \\
		&= \frac{1}{7}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{4}$
Evaluate: $ \lim_{y \to 8} { \left[ \frac{5(2-y)^2}{y^2-4} \right] } $

{% capture include_content %}
By Theorem 05,
$$
\begin{align*}
	\lim_{y \to 8} { \left[ \frac{5(2-y)^2}{y^2-4} \right] }
		&=  \frac{ \lim_{y \to 8} { \left[ 5(2-y)^2 \right] } }{ \lim_{y \to 8} \br{y^2-4}  } \\
		&= \frac{5(2-8)^2}{(8)^2-4} \\
		&= 3		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{5}$
Evaluate: $ \lim_{x \to 1} \br{ \frac{x^2-1}{x^2+3x-4} } $

{% capture include_content %}
Factor both the numerator and the denominator,

$$
\begin{align*}
	\lim_{x \to 1} \br{ \frac{x^2-1}{x^2+3x-4} } 
		&=  \lim_{x \to 1} { \left[ \frac{ \cancel{(x-1)}(x+1)}{ \cancel{(x-1)}(x+4)} \right] }  \\
		&= \lim_{x \to 1} \br{ \frac{x+1}{x+4} }  \\
		&= \frac{1+1}{1+4} \\
		&= \frac{2}{5}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{6}$
Evaluate: $ \lim_{y \to 2}{ \sqrt{ \frac{y^3-y^2-y-2}{2y^3-5y^2+5y-6} } } $

{% capture include_content %}
Factor both the numerator and the denominator,

$$
\begin{align*}
	\lim_{y \to 2}{ \sqrt{ \frac{y^3-y^2-y-2}{2y^3-5y^2+5y-6} } }
		&=  \lim_{y \to 2}{ \sqrt{ \frac{ \cancel{(y-2)}(y^2+y+1)}{ \cancel{(y-2)}(2y^2-y+3)} } }  \\
		&=  \sqrt{ \frac{(2)^2+2+1}{2(2)^2-2+3} } \\
		&= \sqrt{ \frac{7}{9} } \\
		&= \frac{ \sqrt{7} }{3}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}






---
$\example{7}$
Evaluate: $ \lim_{\phi \to 0}{\frac{ \sin 5\phi }{5\phi }} $

{% capture include_content %}
$\text{Let:} \, \theta = 5\phi $ \\
$\text{If:} \, \phi = 0, \; \text{then,} \, \theta=0$

Thus,

$$
\begin{align*}
        \lim_{\phi \to 0}{\frac{ \sin 5\phi }{5\phi }} &= \lim_{\theta \to 0}{\frac{ \sin \theta}{\theta }} \\
        &=1 \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}





---
$\example{8}$
Evaluate: $ \lim_{x \to 0}{\frac{ \tan x}{x}} $

{% capture include_content %}
$$
\begin{align*}
    \lim_{x \to 0}{\frac{ \tan x}{x}} &= \lim_{x \to 0}{\frac{ \sin x}{x \cos x}} \\
    &= \lim_{x \to 0}{\frac{ \sin x}{x} \cdot \frac{1}{\cos x}} \\
    &= \lim_{x \to 0}{\frac{ \sin x}{x} \cdot \lim_{x \to 0}\frac{1}{\cos x}} \\
    &= (1)(1) \\
    &=1 \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}
