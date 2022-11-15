Differentiation is defined as the rate of change for a function. In the case of linear functions, the rate of change (gradient) is constant. For higher order functions, the function will have an algebraic function that determines the gradient of the original function at any given input.

The gradient of a function can be found by dividing the difference in $y$ ($\Delta y$) by the difference in $x$ ($\Delta x$). This only works for linear functions, however can be adapted to work for higher order functions by setting the difference in $x$ as an arbitrary number, $h$, and finding the gradient in terms of this arbitrary number. This process can be written as:
$$\large Let\,\,f(x)\,\,be\,\,an\,\,arbitrary\,\,function: $$
$$\Large m=\frac{f(x+h)\,-f(x)}{(x+h)\,-x}=\frac{f(x+h)\,-f(x)}{h}$$
As $h$ becomes smaller and smaller, the accuracy of the gradient will become greater and greater. Letting it become zero produces a truly accurate gradient function for the original function, $f(x)$. The gradient function of $f(x)$ is denoted as $f'(x)$. Sometimes the gradient of a function is written as $\frac{dy}{dx}$:
$$\Large f'(x)=\lim_{h\to0}\,\frac{f(x+h)\,-f(x)}{h}$$
This process is often referred to as differentiation by first principles. It can be summarised by a rule of thumb for differentiating $y=x^{n}$:
$$\Huge y=x^{n}$$
$$\Huge \frac{dy}{dx}=nx^{n-1}$$
![[Differentiation from first principles.png|400]]

As the difference in $y$ and difference in $x$ become smaller and smaller, different symbols are used to represent their ratio:
$$\Huge \frac{\Delta y}{\Delta x}\to\frac{\delta y}{\delta x}\to\frac{dy}{dx}$$
When you differentate a function once, it is known as its first derivative. When you differentiate the first derivative, it is known as the second derivative, and so on and so forth. For example, in [[Motion along a straight line|physics]], velocity is the first derivative of displacement, and acceleration is the second derivative of displacement. 