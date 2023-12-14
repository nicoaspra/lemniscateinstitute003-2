---
title: "Infinite Limits"
prevcontenturl: ../DC-2.4-one-sided-limits
nextcontenturl: ../DC-2.6-limits-of-functions-with-absolute-value
---

 If you recall our lecture on [Limits at Infinity](../DC-2.3-limits-at-infinity), we used a pizza to depict its size after being sliced into an infinite number of pieces. Here, it is absolutely the opposite. The question that we are now attempting to answer is "how many slices can there be if each slice has a size approaching to nothing (zero)." 
As you may anticipate, the answer would be "infinity."


**Infinite Limits** are those with a limit that approaches infinity in either direction. The limit that approaches infinity "$\infty$" means that as $x$ approaches $a$, the function gets larger and larger where it increases without bound ($\eref{eq:infinite limits 1}$). On the other hand, the limit is approaching negative infinity "$-\infty$" as $x$ approaches $a$ if the function decreases without bound ($\eref{eq:infinite limits 2}$).
 

{% include tcolorbox.html
    details = "
        \lim_{x\to a}f(x)=\infty 
		    \label{eq:infinite limits 1} \\
	    \lim_{x\to a}f(x)=-\infty
		    \label{eq:infinite limits 2}
    "
%}




If we illustrate this concept graphically, the graph of a function with Infinite limits contains **Vertical Asymptotes**; for example, in Figure 1, the function has an asymptote at $x=a$. The curve approaches the line $x=a$ without touching it. Vertical asymptotes occur where the function becomes **undefined**, given that *the limit approaches positive or negative infinity*. 

In relation to [Limits at Infinity](../DC-2.3-limits-at-infinity), the graph has **Horizontal Asymptotes** when *the function approaches infinity*.

{% include images.html 
    url= "DC/DC-2.5.1.png" 
    size= "600px"
    caption = "Figure 1: Vertical asymptotes at $x=a$ of infinite limits"
%}










---
$\example{1}$
Evaluate $\lim_{x\to 0} \frac{1}{x}$

{% capture include_content %}
By substituting $x$ in the function with 0, we would get $\frac{1}{0}$ which is undefined. However, let us try to substitute a value for $x$ that approaches zero from either side and try to see what value the function is approaching.

{% include images.html 
    url= "DC/DC-2.5.2.png" 
    size= "400px"
%}


As you can see, the value is getting larger and larger as $x$ approaches zero. Thus, the function is not approaching a certain value but to infinity. In this case, 
the **right hand-limit** is approaching to positive infinity,

$$\lim_{x\to 0^+} \frac{1}{x} = \infty$$

And the **left-hand limit** is approaching negative infinity.

$$\lim_{x\to 0^-} \frac{1}{x} = -\infty$$

Since the left and right hand limits do not approach the same value, the limit as $x$ approaches $0$ **does not exist**.

$$
\begin{align*}
	\lim_{x\to 0^-} &\neq \lim_{x\to 0^+} \\  
	\lim_{x\to 0} \frac{1}{x} &= \mathrm{DNE}	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}






---
$\example{2}$
Evaluate $\lim_{x\to 0} \frac{5}{x^2}$

{% capture include_content %}
Substitute values to $x$ approaching 0 from both sides.

{% include images.html 
    url= "DC/DC-2.5.3.png" 
    size= "400px"
%}

The left and right hand limits **both approaches to infinity** as $x$ approaches 0. Hence,

$$
\begin{align*}
%	\lim_{x\to 0^-} &= \lim_{x\to 0^+} \\  
	\lim_{x\to 0} &= \infty		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}






---
$\example{3}$
Evaluate $\lim_{x\to 2^+} \frac{7}{x-2}$

{% capture include_content %}
In this example, we are only asked to determine the **right-hand limit** of the function. So, substitute values to $x$ approaching 2 from the right.

{% include images.html 
    url= "DC/DC-2.5.4.png" 
    size= "400px"
%}

Since the function is getting larger and larger as $x$ approaches 2 from the right,

$$
\begin{align*}
	\lim_{x\to 2^+} \frac{7}{x-2} &= \infty	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{4}$
Evaluate $\lim_{x\to -3^-} \br{ 5-\frac{1}{x+3} }$

{% capture include_content %}
In this example, we are only asked to determine the **left-hand limit** of the function. So, substitute values to $x$ approaching $-3$ from the left.

{% include images.html 
    url= "DC/DC-2.5.5.png" 
    size= "400px"
%}

Since the function is getting larger and larger as $x$ approaches $-3$ from the left,

$$
\begin{align*}
	\lim_{x\to -3^-} \br{ 5-\frac{1}{x+3} } &= \infty	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}

