
A problem is computable if there is an algorithm that can solve every instance of it in a finite number of steps. A problem is computational is any problem that can be solved by a computer. Not all computational problems are computable.

Limits of computation are imposed by algorithm complexity and hardware power.

A problem is intractable if it has a [[Big O notation|time complexity]] of anything worse than polynomial, $O(2^n)$, $O(n!)$, e.c.t. A problem is tractable if it has a polynomial or less time complexity, $O(n^k)$.

![[problems.png|500]]

## TSP:

The [[Travelling salesman problem|travelling salesman problem]] is a classic example of an incomputable problem. It is an optimisation problem that has applications in shipping, transport, e.c.t. 

Brute forcing this problem results in a time complexity of $O(n!)$, as each permutation of each possible arc combination needs to be explored. It is an intractable problem.

## Heuristic methods:

Not all intractable problems are equally hard. Approximations can be found by finding a solution that may not be perfect, however is adequate for practical purposes. This is done frequently when finding [[Travelling salesman problem|solutions to the tsp]]. 

Often, as technology develops, non-computable problems can be considered computable through heurstic methods.

## The halting problem:

This is the problem of determining, for any given input, whether a program will finish running in a finite amount of time. Alan Turing proved, in 1936, that the halting problem cannot be solved for any input and any program. He also proved that for a set of inputs to a program, the halting problem can be solved. It cannot be solved for every input on any machine.

`

