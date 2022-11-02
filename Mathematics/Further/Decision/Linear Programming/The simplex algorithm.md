A linear programming problem must first be formulated into constraints and an objective function first. The simplex algorithm is a method of solving linear programming problems for more than 2 decision variables, as graphical methods cannot be used for this (effectivly). 

Inequalities have to be transformed into equations using slack variables (they represent the amount of slack between an actual quantity and the maximum possible value of that quantity). For example:
$$\Huge10x-72y+36z\leq 625$$
$$\Huge 10x-72y+36z+s_{1}=625$$

When more and more variables are added to a solution, the problem becomes impossible to visualise. However, a polyhedron is still formed with a finite amount of verticies. The simplex method starts at one vertex, and moves between verticies in sequence in search for the one that maximises the objective function. Each iteration increases only one variable at a time. If a problem involves minimising a function, then it can be written as:
$$\Huge P=-C$$
Where $C$ is the function to minimise. Maximising $P$ will therefore minimise $C$. The variables that maximise $P$ will also minimise $C$. The objective function needs to be in the form $P-ax-by-cz=value$. Where $a,b,$ and $c$ are the amounts of each decision variable and $x,y$ and $z$ are the decision variables.

The simplex method allows for:
\> The determination if a particular vertex on the edge of the feasible region is optimal
\> The decision to move to an adjacent vertex to increase the value of the objective function

A linear programming problem can be formulated into a simplex tableau that contains all the information about constraints and the objective function. To do this, draw a table that is ($2\,+$ the amount of slack variables) tall and($2\,+$ the amount of decision and slack variables) wide. 

In the first column, head it with "Basic variables" then write the names of all the slack variables with the name of the objective function on the bottom row. For the first row, write all variables (starting with decision variables) and a colum headed "Value" at the end. Now for each row, write down the amount of each variable in the constraint that contains the slack variable at the start of the row with it's associated value. A typical simplex tableau may look like this:
![[Simplex tableau 1.png|300]]
$$\Huge 5x+7y\leq70\to5x+7y+r=70$$
$$\Huge 10x+3y\leq60\to10x+3y+s=60$$
$$\Huge P=3x+2y\to P-3x-2y=0$$
The table is read that the basic variable, $r$, has the value 70 and that the basic variable, $s$, has the value 60. This causes the objective function ,$P$, to have a value of 0. This is a basic feasible solution, as all constraints are satisfied, but it is not an optimal solution.

START ITERATION

Now analyse the objective function's row. The most negative cell is the pivot column. Divide the value in each row by the value in the cell of that row's pivot column to get the $\theta$ value of each row. The row with the least positive (still positive) $\theta$ value is the pivot row. Where the pivot row and the pivot column cross is the pivot value.

Now divide all values in theb pivot row by the pivot value, replacing the front of the row with the head of the pivot column. The other values in the pivot column must be reduced to zero. Do to this, add or subtract multiples of the pivot row from every value in the row. This marks the completion of the first iteration.

END ITERATION

Iterate until there are no negative cells in the objective function's row. Note that the pivot row can never be the objective function row and the pivot column can never be the value column. When there are no longer any negative cells in the objective function's row, an optimal solution has been reached. If a problem requires integer solutions, test every combination of points for rounding up and down. Whichever integer solution maximises the objective function.

The following are the iterations for the example tableau:

ITERATION 1 START
![[Simplex tableau 2.png|300]]
![[Simplex tableau 3.png|300]]
![[Simplex tableau 4.png|300]]
ITERATION 1 END
ITERATION 2 START
![[Simplex tableau 5.png|300]]
![[Simplex tableau 6.png|300]]
![[Simplex tableau 7.png|300]]
ITERATION 2 END

Solution:
$$\Huge P=26$$
$$\Huge x=\frac{42}{11}$$
$$\Huge y=\frac{80}{11}$$
Given that the question requires integer solution:
![[Simplex integer solution.png|500]]
This changes our solution to:
$$\Huge P=23$$
$$\Huge x=3$$
$$\Huge y=7$$