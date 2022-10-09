The "big M method" is an alternative method for performing [[The simplex algorithm]] for  [[Linear programming problems]]. It replaces the stage of minimising the sum of the artificial variables stage of the [[Two-stage simplex method]], however still results in the sum of the artificial variables being zero. 

In the big M method, M represents an arbitrarily large positive number such that $x-nM$ is negative and $nM-x$ is positive, $x,n\in\mathbb{R}^{+}$. This method follows exactly the same method in terms of formulating equations as the two stage simplex method, except for defining a new objective function. Instead of defining a function to minimise the sum of the artificial variables, M times the sum of the artificial variables is taken away from the value of the objective function. Example:
$$\Large 2x+y+z\,+s_{1}=20$$
$$\Huge x-2y-z\,+s_{2}=7$$
$$\Huge x-s_{3}+a_{1}=4\to a_{1}=4-x+s_{3}$$
$$\Huge P=x-y+z\,-M(a_{1})$$
$$\Huge P-x+y-z=-M(4-x+s_{3})$$
$$\Huge P-x-Mx\,+y-z\,+Ms_{3}=-4M$$
$$\Huge P+(-1-M)x+y-z\,+(M)s_{3}=-4M$$
Now carry out the simplex algorithm as usual, treating M as a value. The sheer size of M pushes the artificial variables towards zero. The solution is reached under the same conditions as a normal simplex problem. There is no feasible solution if, at the end of the algorith, any artificial variable has a non-zero value.