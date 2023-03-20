Big data is generally classed as data that is too large to store on a single conventional server, and is generally unstructured. It is collected on such a large scale that it is not easily analysed. Big data analysis is used to seek out patterns, the most prevelant example would be suggestions for online shopping.

There are three major characteristics of big data:
> Volume - big data is too big to be handled by a single server
> Velocity - the rate at which the data set is added to
> Variety - data can be audio, text, image, structured, unstructured e.c.t.

In order to process big data, it needs to be distributed across multiple servers. [[Functional programming]] is useful for processing big data because of these characteristics:
> Immutable data structures - things cannot be inadvertantly altered in a function
> Statelessness - the program's behaviour does not depend on the order in which functions are called
> Higher-Order functions - functions can be inputted as arguments to another function

# Higher Order functions

Map is a higher order function that applies a function to each element of a list, then returns a new list, comprised of the outputs from each input to the function passed to it.

Fold is a higher order function that operates by applying a function recursively over a list and returning a single value.

These functions are very efficient when parallelised. Many processors can work simultaniously on parts of a data set without affecting other parts.


# Fact based model:

In the fact based model for big data, a single piece of information is recorded. A graph schema can be used to model relationships between singular pieces of information, based on facts. 
