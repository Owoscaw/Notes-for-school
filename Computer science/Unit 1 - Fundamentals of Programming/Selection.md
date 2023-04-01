
The flow of a program is controlled using if and else statements, evaluated by a boolean condition. A boolean condition can evaluate to true or false:
```python
if(condition):
	print("condition is true")
else:
	print("condition is false")
```
If the condition is true, control is passed to the first block. Else, control is given to the second block.

Some programming languages have a case statement. This is the logical equivalent of repeating if and else:
```python
number = 100
match number:
	case 400:
		print("number is 400")
	case 300:
		print("number is 300")
	case 200:
		print("number is 200")
	case 100:
		print("number is 100")
```

## Boolean operators

There are 6 boolean operators used to evaluate a boolean condition:
\> greater than, $\gt$
\> less than, $\lt$
\> greater than or equal to, $\geq$
\> less than or equal to, $\leq$
\> equal to, $=$
\> not equal to, $\neq$ 
The syntax of these can vary from language to language, however most will feature some version of these 6.

## Compound boolean expressions

Boolean expression can be chained together with boolean operators. There are 3 main boolean operators used in programming:
\> AND
\> OR
\> NOT
```python
if(condition1 and condition2):
	print("condition 1 and condition 2 are true")
elif(condition1 or condition2):
	print("either condition 1 or 2 are true")
elif(!(condition1 or condition2)):
	print("condition 1 and condition 2 are false")
```
NB: elif is a combination of else and if

