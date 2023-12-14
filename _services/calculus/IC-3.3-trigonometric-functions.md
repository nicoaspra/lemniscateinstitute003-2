---
title: "Trigonometric Functions"
authornum: 2
author: Engr. Nico O. Aspra, M.Eng., RMP, LPT  <br> Engr. Pee Jay N. Gealone
prevcontenturl: ../IC-3.2-exponential-and-logarithmic-functions
nextcontenturl: ../IC-3.4-integration-by-parts
---





In this section, we will learn how to integrate simple trigonometric functions. However, before starting with this lesson, it is imperative to review some of the [basic concepts in trigonometric functions](#related-articles). 

Similar to our previous lessons, integrating trigonometric functions is merely the opposite of differentiating them. With this in mind, it is best also to review the methods in differentiating these functions. To begin, let us introduce the fundamental integration formulas for trigonometric functions. 




## Integration Formulas
The following are the integration formulas that can be used in integrating basic trigonometric functions.
These formulas are derived from the basic differential formulas that were used in [Differential Calculus](../../differential-calculus).
It will be to your advantage if you are very familiar with these formulas.




{% include tcolorbox.html
    details = "
	&\int \sin u \,du = - \cos u +C \\
	&\int \cos u \,du =  \sin u +C 
		\label{eq:trig int cos} \\
	&\int \tan u \,du =  \ln (\sec u) +C \\
		& \phantom{\int \tan u \,du}= - \ln (\cos u) + C \\
	&\int \cot u \,du =  \ln (\sin u) +C  \\
	&\int \sec u \,du =  \ln (\sec u + \tan u) +C  \\
	&\int \csc u \,du =  - \ln (\csc u + \cot u) +C \\
		& \phantom{\int \csc u \,du}= \ln (\csc u - \cot u) +C \\
	&\int \sec^2 u \,du =  \tan u +C \\
	&\int \csc^2 u \,du =  - \cot u +C \\
	&\int \sec u \tan u \,du =  \sec u +C \\
	&\int \csc u \cot u \,du =  - \csc u +C
    "
%}



In evaluating trigonometric functions, we may encounter a variety of distinct forms, each of which demands a different approach. To have a deeper understanding of this notion, it is necessary to gain experience from solving problems. 


---
$\example{1}$
Evaluate the integral $\int\cos 6x \,dx$.

$\solution$ \\
$$
\begin{align*}
	\text{Let:}\quad u &= 6x & \\
		du &= 6 dx \\
		\frac{1}{6}du &= dx	
\end{align*}	
$$

$$
\begin{align*}
	\int\cos 6x \,dx &= \int\cos u \br{\frac{1}{6}du} \\
		&= \frac{1}{6} \int\cos u (\,du)
\end{align*}
$$

Then to evaluate, use $\eref{eq:trig int cos}$,

$$
\begin{align*}
		&= \frac{1}{6} \sin u + C
\end{align*}
$$

Since $u=6x$,

$$
\begin{align*}
	\int\cos 6x \,dx &= \frac{1}{6} \sin 6x + C	\tagans
\end{align*}
$$


---
$\example{2}$
Evaluate the integral $\int\sin 4x \sec 2x\,dx$.

$\solution$ \\
In integral calculus, before we can integrate, the angles of every trigonometric function in one term must all be the same. In this example, the angles are $4x$ and $2x$. Hence, the preliminary step that we must do before we can integrate is to simplify the function.

$$
\begin{align*}
	\sin 4x \sec 2x &= \sin 2(2x) \sec 2x 
\end{align*}
$$

To simplify $\sin 2(2x)$, we can use the Double-Angle Formula, $\sin{2\theta} = 2\sin\theta \cos\theta$.

$$
\begin{align*}
	&= (2 \sin 2x \cancel{\cos 2x}) \bigg(\frac{1}{\cancel{\cos 2x}} \bigg) \\
	&= 2 \sin 2x
\end{align*}
$$

\\
$$
\begin{align*}
	\text{Let:}\qquad u &= 2x & \\
		du &= 2 \,dx \\
		\frac{1}{2}du &= dx	
\end{align*}		
$$

$$
\begin{align*}
	\int\sin 4x \sec 2x\,dx &= \int (2 \sin 2x ) \,dx \\
	&= 2 \int\sin u \br{\frac{1}{2}du} \\
	&= \int\sin u (\,du) \\
	&= - \cos u + C \\
	&= - \cos 2x + C	\tagans
\end{align*}
$$

---
$\example{3}$ 
Evaluate the integral $\int 5\sec\br{\frac{x}{2}}\tan\br{\frac{x}{2}} \,dx$

$\solution$ \\
$$
\begin{align*}
	\text{Let:}\qquad u &= \frac{x}{2} & \\
		du &= \frac12 \,dx \\
		2\,du &= dx	
\end{align*}	
$$

$$
\begin{align*}
	\int 5\sec\br{\frac{x}{2}}\tan\br{\frac{x}{2}} \,dx &= 5\int \sec u \tan u \cdot 2\,du \\
	&= 10\int \sec u \tan u \cdot \,du \\
	&= 10\sec u + C \\
	&= 10\sec\br{\frac{x}{2}}+C		\tagans
\end{align*}
$$



---
$\example{4}$ 
Evaluate the integral $\int x\csc^2x^2\,dx$

$\solution$ \\
$$
\begin{align*}
	\text{Let:}\qquad u &= x^2 & \\
		du &= 2x \,dx \\
		\frac12 du &= dx
\end{align*}	
$$

$$
\begin{align*}
	\int x\csc^2x^2\,dx &= \int \csc^2u \cdot \frac12\,du \\
	&= \frac12 \int \csc^2u\,du \\
	&= -\frac12 \cot u +C \\
	&= -\frac12 \cot x^2 + C		\tagans
\end{align*}
$$



---
$\example{5}$ 
Evaluate the integral $\int \frac{\cot(\ln x)}{x}\,dx$

$\solution$ \\
$$
\begin{align*}
	\text{Let:}\qquad u &= \ln x & \\
		du &= \frac1x \,dx
\end{align*}	
$$


$$
\begin{align*}
	\int \frac{\cot(\ln x)}{x}\,dx &= \int \cot(\ln x) \cdot \frac{1}{x}\,dx \\
	&= \int \cot u\,du \\
	&= \ln(\sin u)+C \\
	&= \ln\brk{\sin (\ln x)}+C		\tagans
\end{align*}
$$




---
$\example{6}$ 
Evaluate the integral $\int \tan^2 4x\,dx$

$\solution$ \\
In this example, there is no direct formula to solve the integral. However, we can use one of the Pythagorean Identities to simplify first the integral.

$$
\begin{align*}
	\int \tan^2 4x &= \int (\sec^2 4x-1)\, dx \\
	&= \int \sec^2 4x\,dx - \int\,dx 
\end{align*}
$$

For $\int \sec^2 4x\,dx$, let $u=4x$, and $\frac14\,du=dx$.

$$
\begin{align*}
	&= \frac14 \int \sec^2 u\,du - \int\,dx \\
	&= \frac14 \tan u-x+C \\
	&= \frac14 \tan 4x-x+C	\tagans
\end{align*}
$$


---
$\example{7}$ 
Evaluate the integral $\int \frac{e^{3x}\csc e^{3x}}{\tan e^{3x}} \,dx$,

$\solution$ \\
Before integrating, simplify first the function.

$$\int \frac{e^{3x}\csc e^{3x}}{\tan e^{3x}} \,dx = \int e^{3x}\csc e^{3x}\cot e^{3x} \,dx$$

$$
\begin{align*}
	\text{Let:}\qquad u &= e^{3x} & \\
		du &= 3e^{3x} \,dx \\
		\frac13\,du &= e^{3x} \,dx
\end{align*}
$$

$$
\begin{align*}
	\int \frac{e^{3x}\csc e^{3x}}{\tan e^{3x}} \,dx &= \int \csc e^{3x}\cot e^{3x} \cdot e^{3x}\,dx \\
	&= \frac13 \int \csc u\cot u \,du \\
	&= -\frac13 \csc u+C \\
	&= -\frac13 \csc e^{3x}+C		\tagans
\end{align*}
$$



---
$\example{8}$ 
Evaluate the integral $\int \frac{\sin^3x}{1+\cos x}\,dx$

$\solution$ \\
From the trigonopmetric identities, there is no identity for cubic functions. But, what we can do, is to first break down $\sin^3x$ to $\sin x$ and $\sin^2 x$. Hence,

$$
\begin{align*}
	\int \frac{\sin^3x}{1+\cos x}\,dx &= \int \frac{\sin x \cdot \sin^2 x}{1+\cos x}\,dx \\
	&= \int \frac{\sin x (1-\cos^2x)}{1+\cos x}\,dx \\
	&= \int \frac{\sin x (1-\cos x)\cancel{(1+\cos x)}}{\cancel{(1+\cos x)}}\,dx \\
	&= \int (\sin x- \cos x \sin x) \,dx \\
	&= \int \sin x \,dx - \int \cos x \sin x \,dx \\
	&= \int \sin x \,dx + \int \cos x (-\sin x) \,dx
\end{align*}
$$

For $\int \cos x (-\sin x) \,dx,$ let $u=\cos x$, and $du=-\sin x\,dx$

$$
\begin{align*}
	&= \int \sin x \,dx + \int u\,du \\
	&= -\cos x + \frac{u^2}{2} + C \\
	&= -\cos x + \frac{\cos^2x}{2} + C \\
	&= \frac12 \cos^2x-\cos x + C		\tagans
\end{align*}
$$





---
## Related Articles
- [Angles](../calculus/DC-9.1-angles)
- [Basic Trigonometric Functions](../DC-9.2-basic-trigonometric-identities)
- [Evaluating Trigonometric Functions](../DC-9.3-evaluating-trigonometric-functions)
- [Trigonometric Identities](../DC-9.4-trigonometric-identities)
- [Derivatives of Trigonometric Function](../DC-9.5-derivatives-of-trigonometric-functions)