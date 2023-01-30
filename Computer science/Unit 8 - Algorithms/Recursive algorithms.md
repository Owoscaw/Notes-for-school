The factorial function is a classic example of a recursive algorithm:
$$\Huge n!=\prod_{i=0}^{n}i$$
Where $0!$ is defined as $1$. For example, $5!$ can be written as:
$$\Huge 5!=5\times4\times3\times2\times1\times0!$$
$$\Huge 5!=5\times4!$$
Any factorial can be written as:
$$\Huge n!=n\times(n-1)!$$
## Recursion:

In programming, this appears when a function calls itself. A recursive algorithm has three essential characteristics: A base case, which is met and causes the stack to unwind. For input values other than the base case, the function calls itself. The base case must be reached in a finite amount of function calls.

The alternative to a recursive function is an iterative function:
```python

#recursive approach
def recursiveListSum(list):
	if len(list) == 1:
		return list[0]
	else:
		return list[0] + recursiveListSum(list[1:0])

#iterative approach
def iterativeListSum(list):
	sum = 0
	for i in list:
		sum += i
	return sum

```
The recursive approach is very CPU efficient, especially on multi-core CPUs. However a lot of information needs to be recorded on the call stack, which can be very memory inefficient.

## Call stack:

Each time a function is called, the return address, parameter, and local variables are pushed onto the call stack. When a function calls itself too many times, the call stack cannot hold any more calls  and a stack overflow is called. This happens when the recursion depth is too large or the base case is never reached.