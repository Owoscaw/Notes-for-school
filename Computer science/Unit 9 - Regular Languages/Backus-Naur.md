Backus-Naur form is a formal notation that is used to describe language syntax, it is a language that describes a language. BNF is needed because not all lanuages are regular, and therefore cannot be described by a regular expression. BNF allows for wider expression of contex-free languages. For example, the set $\{a^nb^n | n\geq 0\}$ cannot be represented by a [[Regular Expressions|regular expression]]. Each BNF statement is called a production rule. Instructions for a computer cannot be ambiguous, as the processor cannot make assumptions. A programming language requires a strict set of rules to define it. BNF can be used by compilers to represent the syntax of a programming language.

## BNF syntax:

$::=$ is defined as
$|$ or
$<>$ surrounds category items
side by side items must follow exactly
terminal symbols cannot be further broken down
non-terminal symbols can be further broken down

Example:
$<digit>\,\,::=\,\,0|1|2|3|4|5|6|7|8|9$
$<upper>\,\,::=\,\,A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z$
$<postcode>\,\,::=\,\,<upper><upper><digit><digit>$

## Context free languages:

A context-free language can be defined in BNF when a single non-terminal symbol on the left can be replaced by its definition to the right, the context of a non-terminal symbol does not affect its definition. A terminal symbol cannot be broken down into other terminal symbols, for example, a digit. A non-terminal symbol can be broken down / represented by other non-terminal symbols or terminal symbols, for example, a postcode.

Context-free languages can also be represented by a syntax diagram, a graphical representation of BNF:
An ellipse / circle represents a terminal symbol
A rectangle represents a non-terminal symbol
Arrows are used to show recursion and repetition

## Production rules:

Each BNF statement defines a production rule for a symbol. These production rules can be recursive, i.e. they contain their own symbol:
$$\Large <unsigned>\,::=\,<digit>|<digit><unsigned>$$
Recursive production rules allow for complex symbols to be represented using a relatively short definition.

## Parsing:

Parsing involves checking if an input string is valid against the set of rules defined by a BNF. When a compiler recieves input, said input is checked against it's input tree according to its rules. This begins at terminal symbols and works its way up the tree of symbols to check validity.
