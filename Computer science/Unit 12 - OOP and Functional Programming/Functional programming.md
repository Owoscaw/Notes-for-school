A programming paradigm is a style of programming. Different types of problems require different ways of solving them. 

Procedural programming is a "recipe" approach to problem-solving. Steps are taken one after another and are ordered. The three principles of procedural programming are sequence, selection, and iteration. 

Object-oriented programming is another type of paradigm that models parts of the problem as objects with properties and methods. Python supporst both procedural and object-oriented programming.

Declarative programming is another programming paradigm that states what needs to be done. [[Introduction to SQL|SQL]] is an example of a declarative programming language widely used.

## Functional:

Functional programming is a paradigm that describes a series of functions. Each function takes arguments and returns an output. The domain of a function is a set from which the function's input values are chosen, the co-domain is a set from which the function's output values are chosen. A function maps from a set of inputs to a set of outputs. 

For example., a function, $F$, that maps inputs $A$ to outputs $B$ can be defined as:
$$\Huge F:A\to B\,\,where\,\,f(x)=x^{2}$$
This is equivalent to the haskell code:
```haskell
squareNumber x = x*x
```


## Domain + Co-domain:

The domain is a set of inputs from which a function's values are chosen. The domain maps to a co-domain, the set of values from which outputs are chosen. A function is a mapping from a set of inputs (domain) to a set of possible outputs (co-domain).


## Function composition:

One function can be used as an argument of another:
$$\Huge f(x)=\frac{x^2}{3},\,\,\,g(x)=2x-5$$
$$\Huge g(f(x))=2f(x)-5=\frac{2x^2}{3}-5$$
Here, $g(f(x))$ is the composition of f and g. This is written in haskell as:
```haskell
f x = x*x/3
g x = 2*x-5
```

$$\Huge g(f(x))\to g.f\,\,x$$

## Types and typeclasses:

Functional languages use types and typeclasses. A typeclass is a set of types that can be defined by the user, for example:
```haskell
Typeclass Num includes Integer, Int, Float, Double
```

Functions can have an explicit type declaration, that limits the types a function can return. It is not a strongly typed language:
```haskell
sumOfTwo :: Num -> Num -> Num
sumOfTwo x y = x + y

isEqual :: Int -> Int -> Bool
isEqual x y = x == y
```
In the command line, the above code can be run:
\> :load isEqual.hs
\> isEqual 7 8
False
\> isEqual 7 7
True
\> isEqual 7.5 7
Error - 7.5 is not type Int
\> isEqual fish paste
Error - fish is not type Int
Error - paste is not type Int