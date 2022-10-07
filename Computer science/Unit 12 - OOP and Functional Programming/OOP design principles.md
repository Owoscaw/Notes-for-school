## Inheritance:

A superclass is a class that is used to declare a subclass. A subclass inherits methods and attributes from its superclass, while being able to have methods and attributes exclusive to it.

Within the declaration of the superclass, methods and attributes declared as "protected" are private to any code outside the class, except for children of that class (subclasses). In python, protected attributes and methods are preceded by an underscore, whereas private methods and attributes are preceded by a double underscore.

Access modifiers are used to define how attributes and methods can be accessed. A member of a class is accessible from anywhere if it is public, from the class definition and any subclasses if it is protected, and only from within the class definition if it is private.

## Polymorphism: 

Polymorphism is a method used in a class heirarchy that can change behaviour based on the class it belongs to. Many forms. This is achieved through overriding methods, previously defined in the superclass. 

## Overriding: 

Overriding a class redefines a previously defined class (from a superclass) with new code. The new, overriden method can be extended by calling the original method within the redefinintion of the method. The constructor function can also be overriden and extended by calling the parent constructor within the new definiton for the contructor. Overriding is used to achieve polymorphism.

## Association:

Composition and aggregration are both types of relationship that describes what objects belong to a parent object. Both of these relationships describe association between classes.

Composition is a relationship where if a containing object is destroyed, all child (containing) objects are destroyed with it. This is depicted by a filled diamond connected by a solid line in a class diagram.

Aggregation is a relationship where if the containing object is destroyed, containing objects persist. This is depicted by an unfilled diamond with a solid line in a class diagram.

## Methods:

An abstract method is a method defined, typically in a superclass, that only contains a signature. There is no code in this method, it is only defined to tell an interpreter/compiler that this class will be defined later by children.

A virtual method is an implementation that can be redefined by child classes, it may have a definintion in a parent class, unlike an abstract method, but may also be overidden by child classes.

A static method is relevent to all instances of a class, rather to a specific instance.

Python only supports virtual and abstract methods.

## Class diagrams:

Class diagrams are a way of showing the relationship between parent and child classes in a tree-like format. They consist of boxes representing classes, with private, protected, and public attributes / methods are denoted with -, #, and + suffixes respectively. Arrows are used to show where a class inherits from. Methods and attributes should be grouped seperately.

![[class diagram.jpg]]

