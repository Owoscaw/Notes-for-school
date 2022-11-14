
A finite state machine is an abstract representation of how something changed from one state to another in response to a condition or event. A finite state machine can either be in a single state, or transitioning between states at any given time.

In a finite state machine (FSM), said machine can only be in a single state at a time (or transitioning). An FSM is defined by a list of its states and conditions for each transition between states.

An example of an FSM is a turnstile. It can be in one of two states, locked or unlocked. Inserting a ticket unlocks the turnstile, allowing a single customer to pass. Then the arms are locked again until another ticket is inserted.

![[FSM.png]]

Finite state automation is an FSM that has no output. It has a start state and a set of end or accept states. If the automation reaches a final state, it is said to have accepted the input. Starting from an initial state, the automaton processes a sequence of symbols and follows it to the target state.

A finite state system will accept a string if there is a path from the start state to the end or accept state labelled by the symbols c1…cn. The language recognised by the FSM consists of all the strings accepted by it. A string is only accepted if all transitions are valid and there are no redundancies.

State transition tables are an alternate representation of an FSM. It shoes the next state for any input.

These are similar to [[Graphs]], and can be modelled by them.


