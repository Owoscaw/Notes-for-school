Infix is the notation used in mathematics:
$$\Huge a*(b\,+c)/d$$
Prefix (polish notation) was invented in 1924 by polish mathematician Jan Lukasiewicz:
$$\Huge /*a+b\,c\,d$$
Postfix (reverse polish notation) was invented in 1950 as a way to do mathematics without brackets, and can easily be implemented using a stack:
$$\Huge a\,b\,c+*d/$$
Reverse polish notation removes the need for brackets, as all ambiguity from brackets is removed. There exists an order of operations for RPN:
> Unary minus, ~
> Exponentiation, ^
> Multiplication / Division, * / /
> Addition / Subtraction, + / -

## Infix to RPN (postfix):

One method of translation between infix and RPN expressions is numbering. This algorithm numbers operands and operations. Starting from the left, each operand is numbered. When the end of the expression is reached, operators are numbered from right to left. If an operator is reached and there are enough operands availible, the operator is numbered, and the next operand is moved on to. Once all operators and operands have been numbered, they can be written out in numerical order to find the RPN translation of an infix expression. Example:
$$\Huge 4/2\,+\,8*4\,-\,(5+2)$$
$$\Huge 1\,3\,2\,\,\,7\,\,\,4\,6\,5\,\,\,(11)\,\,\,8\,(10)\,9$$
$$\Huge 42/84*+52+-$$

Another method of translation is bracketing. This is where brackets are added to every expression to make the order of precedence explicit, then each operator in each pair of brackets is moved to the end. Example:
$$\Huge 4/2\,+\,8*4\,-\,(5+2)$$
$$\Huge (((4/2)+(8*4))-(5+2))$$
$$\Huge (((42/)+(84*))-(52+))$$
$$\Huge (((42/)(84*)+)(52+)-)$$
$$\Huge 42/84*+52+-$$

Another method of translation is by using a binary tree. This works by building a [[Trees|binary tree]] from the infix expression then traversing it using a post-order traversal algorithm. Operands of lowest precedence are decomposed into two child nodes of the lowest precendece operand. Once the binary tree is constructed, traversing using post-order traversal will translate the infix expression to RPN.


## RPN to infix:

One method of converting RPN expression into infix expressions is through scanning. This works by scanning left to right, picking out pairs of operands and single operators. Using brackets between operands makes this clear.

Another method of converting RPN to infix is by bracketing. This is very similar to converting infix to RPN. Place brackets around operators and the previous two operands, then move the 2nd operand to the right of the operator, rinse and repeat.

## RPN with stack:

RPN expressions are easily evaluated using a stack. If a token is an operand, it is pushed onto the stack. If it is an operator, the required amount of operands are popped from the stack, the operation is peformed and then pushed onto the stack