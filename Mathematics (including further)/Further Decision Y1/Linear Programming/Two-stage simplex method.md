The simplex method described in [[The simplex algorithm]] only works if all constraints are "$\leq$" constraints. The two-stage simplex works when there are "$\geq$" constraints. Inequalities required different treatment to be used with this method. If an inequality contains "$\geq$", then a surplus variable must be subtracted. However, this does not solve the problem of using the simplex method with $x$ and $y$ as non-basic variables, so another variable can be introduced. This is the artificial variable. Example:
$$\Huge x+3y\geq10\to x+3y-s_{1}=10\to x+3y-s{_1}+a_{1}=10$$
This constraint can now be written into a simplex tableau using $x, y,$and $s$ as non-basic variables and $a$ as a basic variable. 

However, we do not stop there. Sometimes there is no feasible solution to a linear programming problem, due to the clash of $\leq$ and $\geq$ constrains, causing there to be no feasible region. A new objective funciton therefore needs to be defined. This is a function that minimises the sum of the artificial variables. Equations can be rearranged to make the artificial variable the subject, this is what I mean by "the sum of the artificial variables"

This function should be minimised using the simplex method. If the minimum value of this function is 0, then there is a basic feasible solution. If the minimum value of this function is not 0, then there is no feasible solution. 

After minimising the sum of the artificial variable, the tableau can be used to solve the original problem, but all artificial variables as well as the function that minimises the sum of the artificial variables can be removed. 

This is the general form of a function to minimise the sum of the artificial variables:
$$\Huge Maximise:\,\,I=-\left(\sum_{1}^{n}a_{n}\right)$$
Using the example above:
$$\Huge a_{1}=10-x-3y\,+s_{1}$$
$$\Huge Maximise:\,\,I=-(10-x-3y+s_{1})$$
$$\Huge I-x-3y\,+s_{1}=-10$$