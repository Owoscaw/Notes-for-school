## Euler's relation:

Euler's relation states:
$$\Huge re^{i\theta}=r\left(\cos{\theta}+i\sin{\theta}\right)$$
This is another [[Other Forms of Complex Numbers|form of a complex number]] and comes from the Maclaurin expansion of $e^x$, $\cos{x}$, and $\sin{x}$:
$$\Large \sin{x}=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\frac{x^9}{9!}+\frac{(-1)^{n+1}\,x^{2n-1}}{(2n-1)!}+...$$
$$\Large \cos{x}=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\frac{x^8}{8!}+\frac{(-1)^{n+1}\,x^{2n}}{(2n)!}+...$$
$$\Large e^x=1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\frac{x^4}{4!}+\frac{x^n}{n!}+...$$
Substituting $ix$ for $x$ in the expansion for $e^x$:
$$\Large e^{ix}=1+ix+\frac{(ix)^2}{2!}+\frac{(ix)^3}{3!}+\frac{(ix)^4}{4!}+\frac{(ix)^n}{n!}+...$$
$$\Large e^{ix}=1+ix-\frac{x^2}{2!}-i\frac{x^3}{3!}+\frac{x^4}{4!}+\frac{i^n\,x^n}{n!}+...$$
Factoring $i$ out of this expansion:
$$\Large \displaylines{e^{ix}=\left(1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\frac{x^8}{8!}+\frac{(-1)^{n+1}\,x^{2n}}{(2n)!}+...\right)\\+i\left(x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\frac{x^9}{9!}+\frac{(-1)^{n+1}\,x^{2n-1}}{(2n-1)!}+...\right)}$$
The expansions in each bracket is identical to $\cos{x}$ and $\sin{x}$ respectively:
$$\Huge e^{ix}=\cos{x}+i\sin{x}$$
Chaing the $x$ to a $\theta$ for convention:
$$\Huge e^{i\theta}=\cos{\theta}+i\sin{\theta}$$


## De Moivre's Theorem:

Abraham De Moivre theorised a formula to find complex numbers raised to the $n$th power. He stated as follows:
$$\Large (r(\cos{\theta}+i\sin{\theta}))^n=(re^{i\theta})^n=r^ne^{in\theta}=r^n(\cos{n\theta}+i\sin{n\theta})$$
$$\Huge n\in\mathbb{Z}^+$$
This result can be used to find trigonometric identities for large powers, when using formulae would be unfeasable. This can be done in two ways:
$$\Large z+z^{-1}=\cos{\theta}+i\sin{\theta}+\cos{-\theta}+i\sin{-\theta}$$
$$\Large z+z^{-1}=\cos{\theta}+\cos{\theta}+i\sin{\theta}-i\sin{\theta}$$
$$\Large z+z^{-1}=2\cos{\theta}$$
$$\Large z-z^{-1}=\cos{\theta}+i\sin{\theta}-\cos{-\theta}-i\sin{-\theta}$$
$$\Large z-z^{-1}=\cos{\theta}-\cos{\theta}+i\sin{\theta}+i\sin{\theta}$$
$$\Large z-z^{-1}=2i\sin{\theta}$$
Rasing either $z+z^{-1}$ or $z-z^{-1}$ to a power can help find powers of trigonometric identities, for example:
$$\huge \sin^{n}{\theta\,\,or\,\,\cos^{n}{\theta}}$$
Raising $\cos{\theta}+i\sin{\theta}$ to a power can help find multiples of trignometric identities, by observing real and imaginary parts of the binomial expansion, for example:
$$\Large (\cos{\theta}+i\sin{\theta})^n=\cos{n\theta}+i\sin{n\theta}=\sum^n_{r=0}{}^nC_r\cos^r{\theta}\,(i\sin\theta)^{n-r}$$
$$\Large \cos{n\theta}=\Re\left(\sum^n_{r=0}{}^nC_r\cos^r{\theta}\,(i\sin\theta)^{n-r}\right)$$
$$\Large \sin{n\theta}=\Im\left(\sum^n_{r=0}{}^nC_r\cos^r{\theta}\,(i\sin\theta)^{n-r}\right)$$