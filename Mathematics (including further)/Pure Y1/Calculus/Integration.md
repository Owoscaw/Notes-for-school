Integration is the reverse process of [[Differentiation]], it is used to find the area under a function between two bounds. When an integral is bound by two numbers, it is called a definite integral. When it is not bounded, it is called an indefinite integral.

The process of integration involves taking the sum of rectangles that are fitted with a width $\delta x$ and a height $f(\delta x)$. It can be written as a sum:
$$\Large \int f(x)\,dx=\lim_{n\to\infty}\,\sum_{i=1}^{n}f(x_{i})\delta x$$
Let's look closer at the LHS of the equation:
$$\Huge \int f(x)\,dx$$
The large curly "s" represents the integral, $f(x)$ is the function that we are integrating, and $dx$ indicates that we are integrating with respect to the variable $x$. Now looking at the RHS of the equation:
$$\Huge \lim_{n\to\infty}\,\sum_{i=1}^{n}f(x_{i})\delta x$$
We are taking the limit as $n$ tends to infinity of the sum from  $i=1$ to $i=n$ of the output of the function $f(x)$ multiplied by an increasingly small change in $x$, $\delta x$. This produces the sum of rectangles, width $\delta x$ and height $f(\delta x)$. This is an approximation of the area under the function $f(x)$ until $n$ reaches infinity, at which point the sum becomes an accurate representation of the area under the curve. The actual algebraic method of integration is as follows:
$$\Large \int x^{n}\,dx=\frac{x^{n+1}}{n+1}+c$$
Where $c$ is a constant. Note that the following is true for any number of terms for the intergrand (function being integrated):
$$\Large \int (ax^{n}+bx^{m})dx=\int ax^{n}\,dx\,\,+\int bx^{m}\,dx$$
The following is a useful visualisation of the process when taking an integral:
![[Integration visualisation part 1.png|500]]
![[Integration visualisation part 2.png|500]]

Once the integral has been found, the values of $a$ and $b$ are substituted into the resulting function and the value produced from $a$ is taken away from the value produced from $b$:
$$\Large \int_{a}^{b} x^{n}\,dx=\left[\frac{x^{n+1}}{n+1}+c\right]^{b}_{a}=\left(\frac{b^{n+1}}{n+1}+c\right)-\left(\frac{a^{n+1}}{n+1}+c\right)$$
This cancels out the constant and leaves the value for the area under the function $f(x)=x^{n}$ from $x=a$ to $x=b$. Note that when the area dips below the $x$-axis, it must be multiplied by -1 or a negative area will be returned. Area can also be found by integrating along the $y$-axis. The function needs to be found and used in terms of $x$ in order to do this, and values for $a$ and $b$ should bind the function along the $y$-axis.