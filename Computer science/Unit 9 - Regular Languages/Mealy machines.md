
Mealy machines are an extension of [[Finite state machines]], they are abstract representations of states and their transitions. A finite state machine acceps a string, given that there is a path from the start state to an accept state via the path string, $c_{1}, c_{2}, ...,c_{n}$ .The language recognised by an FSM consists of all strings that it can accept. Example:

A mealy machine is a type of FSM. It generates an output based on each state transition. The output is determined by the current state and the current input. For each state transition, there is an associated output. Notation in a mealy machine is given as input/output for each transition, the first parameter specifing the input that will cause the transition, the second parameter specifing the output with the associated transition. 

Mealy machines can be used to respond to substrings in a larget input, for example an input of "001" could be flagged by output with a 1, when 001 is enterred as part of a larger string.

A state transition table can be used to define a mealy machine, instead of an FSM diagram. It shows all states and possible inputs and output for every combination of state and input. It also shows what state will be the next state when the given imput happens.