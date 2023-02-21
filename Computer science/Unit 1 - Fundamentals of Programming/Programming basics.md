
An algorithm is defined as a sequence of instructiosn that can be followed to solve a problem. Algorithms can be written in pseudocode. This consists of statements similar to english that represent the logical flow of a program. There are guidlines for pseudocode, however no strict guidlines. 

Writing a program out in pseudocode is helpful for thinking about the steps needed in order to write a program.

## Variables and assignment

An identifier is used to refer to a location in memory that is used to store a variable. Assigment is the act of assigning a value to a location in memory. This looks like this in most programming languages:
```python
variable_name = "variable value"
```
Here, the identifier, $variable\_name$ was used to store the string value "variable value".

Constants are variables that cannot have their value changed once assigned. These are useful when the value will never need to be amended, as it can prevent errors by restricting access to the memory location represented by the constant's identifier.


## Operators

Operators are used on variables to return a new variable. These are most prevelant in mathematical operations. For example, two integers could be added in the following manner:
```python
sum = 3 + 4
```
Here, the integer 3 is added to the integer 4 to return the integer 7, storing the result in the variable $sum$.

Operators can be strict between different data types, as their behaviour needs to be defined explicitley when doing so. For example, you cannot add an integer to a string without first converting it to a string:
```python
sum = 3 + " thousand bees" #gives error
sum = "3" + " thousand bees" #works
```


The modulus and div operators are two not usually used in mathematics that are frequently used in programming. Modulus, $\%$, returns the remainder from integer division, where div, $/$ returns the integer. 