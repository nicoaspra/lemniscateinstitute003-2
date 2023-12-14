---
title: "Trigonometric Identities"
prevcontenturl: ../DC-9.3-evaluating-trigonometric-functions
nextcontenturl: ../DC-9.5-derivatives-of-trigonometric-functions
---


{% include minibox.html
    details = "
    $\tcBal{Pythagorean Identities}$ 
    $$
    \begin{align}
        \sin^2{\theta}+\cos^2{\theta} &=1 \\
        \tan^2{\theta}+1 &= \sec^2{\theta}
            \label{eq:pythagorean id tan} \\
        \cot^2{\theta}+1 &= \csc^2{\theta}
    \end{align}
    $$
    "
%}


{% include minibox.html
    details = "
    $\tcBal{Double-Angle Formulas}$ 
    $$
    \begin{align}
        \sin{2\theta} &= 2\sin\theta \cos\theta \\
        \cos{2\theta} &= \cos^2{\theta}-\sin^2{\theta} \\
        \tan{2\theta} &= \frac{2\tan\theta}{1-\tan^2{\theta}}
    \end{align}
    $$
    "
%}


{% include minibox.html
    details = "
    $\tcBal{Half-Angle Formulas}$ 
    $$
    \begin{align}
        \sin\frac{\theta}{2} &= \sqrt{\frac{1-\cos\theta}{2}} \\
        \cos\frac{\theta}{2} &= \sqrt{\frac{1+\cos\theta}{2}} \\
        \tan\frac{\theta}{2} &= \frac{1-\cos\theta}{\sin\theta} = \frac{\sin\theta}{1+\cos\theta}
    \end{align}
    $$
    "
%}


{% include minibox.html
    details = "
    $\tcBal{Sum and Difference Identities}$ 
    $$
    \begin{align}
        \sin{(\alpha \pm \beta)} &= \sin\alpha \cos\beta \pm \cos\alpha \sin\beta \\
        \cos{(\alpha \pm \beta)} &= \cos\alpha \cos\beta \mp \sin\alpha \sin\beta \\
        \tan{(\alpha \pm \beta)} &= \frac{\tan\alpha \pm \tan\beta}{1 \mp \tan\alpha \tan\beta}
    \end{align}
    $$
    "
%}


{% include minibox.html
    details = "
    $\tcBal{Product-Sum Identities}$ 
    $$
    \begin{align}
        \sin\alpha \sin\beta &= \frac{1}{2}\left[ \cos(\alpha-\beta)-\cos(\alpha+\beta)\right] \\
        \cos\alpha \cos\beta &= \frac{1}{2}\left[ \cos(\alpha+\beta)+\cos(\alpha-\beta)\right] \\
        \sin\alpha \cos\beta &= \frac{1}{2}\left[ \sin(\alpha+\beta)+\sin(\alpha-\beta)\right]
    \end{align}
    $$
    "
%}


{% include minibox.html
    details = "
    $\tcBal{Sum-Product Identities}$ 
    $$
    \begin{align}
       \sin\alpha + \sin\beta &=  2\sin\frac{\alpha+\beta}{2} \cos\frac{\alpha-\beta}{2} \\
        \sin\alpha - \sin\beta &=  2\sin\frac{\alpha-\beta}{2} \cos\frac{\alpha+\beta}{2} \\
        \cos\alpha + \cos\beta &=  2\cos\frac{\alpha+\beta}{2} \cos\frac{\alpha-\beta}{2} \\
        \cos\alpha - \cos\beta &= -2\sin\frac{\alpha+\beta}{2} \sin\frac{\alpha-\beta}{2}
    \end{align}
    $$
    "
%}




---
$\example{1}$
Simplify the function $y = \frac{\sin 2x}{\cot x}$.

{% capture include_content %}

$$
\begin{align*}
    y &= \frac{\sin 2x}{\cot x} \\
    &= \frac{2\sin x \cos x}{\br{\dfrac{\cos x}{\sin x}}} \\
    &= \frac{2\sin x \cancel{\cos x} \sin x}{\cancel{\cos x}} \\
    &= 2\sin^2 x	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}









---
$\example{2}$
Express the function $\tan x + \cot x$ in terms of sine and cosine.

{% capture include_content %}

$$
\begin{align*}
    \tan x + \cot x &= \frac{\sin x}{\cos x} + \frac{\cos x}{\sin x} \\
    &= \frac{(\sin x) (\sin x) + (\cos x) (\ cos x)}{\sin x \cos x} \\
    &= \frac{\sin^2 x + \cos^2 x}{\sin x \cos x} \\
    &= \frac{1}{\sin x \cos x}		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}






---
$\example{3}$
Express the angle of the function as a single term $\cos 7x \cos x$.

{% capture include_content %}
Recall that the identity: $\cos\alpha \cos\beta = \frac{1}{2}\brk{\cos(\alpha+\beta)+\cos(\alpha-\beta)}$

$$
\begin{align*}
	\cos 7x \cos x &= \frac{1}{2} \brk{ \cos(7x+x)+\cos(7x-x) }\\
		&= \frac{1}{2} \brk{ \cos(8x)+\cos(6x) } \tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}







---
$\example{4}$ 
Prove the equation $\frac{\tan{x}\csc^2{x}}{1+\tan^2{x}}=\cot{x}$.

{% capture include_content %}
In proving identites, the first thing that we want to do is to choose one side of the equation that is more complicated. Then try to break it down in terms of sine and cosine to simplify the function.

$$
\begin{align*}
	\cot{x} &= \frac{\tan{x}\csc^2{x}}{1+\tan^2{x}} \\
	&= \frac{\dfrac{\cancel{\sin x}}{\cos x} \cdot \dfrac{1}{\sin^{\cancel{2}}x}}{\sec^2{x}} \\
	&= \frac{\dfrac{1}{\cos x \sin x}}{\dfrac{1}{\cos^2 x}} \\
	% &= \frac{\frac{1}{\cos{x}\cdot\sin{x}}}{\frac{\cos{x}+\sin{x}}{\cos{x}}} \\
	&= \frac{1}{\cancel{\cos{x}}\cdot\sin{x}} \cdot \cos^{\cancel2}{x} \\
	&= \frac{\cos x}{\sin x} \\
	&= \cot x		\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}






---
$\example{5}$ 
Prove the equation $1+2\sin\beta = (\sin\beta+\cos\beta)^2$.

{% capture include_content %}
In this example, the function is already expressed in terms of sine and cosine. So, what we can do now is we can first expand the binomial.

$$
\begin{align*}
	1+2\sin\beta &= (\sin\beta+\cos\beta)^2 \\
	&= \sin^2\beta + 2\sin\beta\cos\beta + \cos^2\beta \\
	&= (\sin^2\beta + \cos^2\beta) + 2\sin\beta\cos\beta \\
	&= 1 + 2\sin\beta	\tagans
\end{align*}
$$

{% endcapture %}
{% include solution.html details = include_content %}