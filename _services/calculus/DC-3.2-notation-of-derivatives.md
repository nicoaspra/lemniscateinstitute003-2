---
title: "Notation of Derivatives"
prevcontenturl: ../DC-3.1-introduction-to-derivatives
nextcontenturl: ../DC-3.3-slope-of-a-curve
---




Notation of derivatives refers to the different ways in which a derivative can be expressed mathematically. Numerous notations are in use and have been proposed by various mathematicians throughout history, including Leibniz's notation, Lagrange's notation, Euler's notation, and Newton's notation. In our lessons, we will be primarily using Leibniz's and Lagrange's Notations. 

In Leibniz's notation, the derivative of $f(x)$ is expressed as $\textstyle{ \frac{d}{dx}f(x) }$ or $\textstyle{ \frac{dy}{dx} }$ which we are already familiar with since we've already encountered this notation from the previous lesson. In this notation, $\textstyle{ \frac{d}{dx} }$ is not treated as a fraction but as an **operator**. Just as $+$ sign denotes addition, or $\div$ sign denotes division, here $\textstyle{ \frac{d}{dx} }$ denotes **differentiation**. So for example, the derivative of $3x^2+2x-1$ can be expressed as $\textstyle{ \frac{d}{dx}(3x^2+2x-1)} $

And in Lagrange's notation, the derivative of $f(x)$ is expressed as $f'(x)$ or $y'$ where the prime symbol denotes a derivative.



{% include tcolorbox.html
    details = "
	\text{Leibniz's Notation} 		&& 	\frac{dy}{dx}=\frac{d}{dx}f(x)&=\lim_{\Delta x\to 0} \frac{\Delta y}{\Delta x}
		\label{eq:leibniz's notation}\\
	\text{Lagrange's Notation} 	&& 	y'=f'(x)&=\lim_{\Delta x\to 0} \frac{\Delta y}{\Delta x}
		\label{eq:lagrange's notation} \\
	\text{Euler's Notation} 	&& 	Dy=Df(x)&=\lim_{\Delta x\to 0} \frac{\Delta y}{\Delta x}
		\label{eq:euler's notation} \\
	\text{Newton's Notation} 	&& 	\dot{y}&=\lim_{\Delta x\to 0} \frac{\Delta y}{\Delta x}
		\label{eq:newton's notation}
    "
%}