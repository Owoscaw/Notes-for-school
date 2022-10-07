An object-oriented program consists of objects:
> Each object has its own associated data (attributes), and operations done on said data (methods)
> Objects interact with one another
> All processing is done by objects

A class is a blueprint for an object. This class defines attributes and methods that represent behaviour and characteristics of the object it represents. A constructor is used to craete objects based on the class.

Encapsulation is a fundamental principle of OOP. Attributes and methods are wrapped into a single entity. Information about an object can be hidden from the user using private attributes and methods. When attributes are private, they cannot be directly accessed by the programmer, they have to be accessed via getters and setters (methods).  This is considered good practice, as information can only be accessed on the class's terms, not the programmer's.

Notation:
class instance.class attribute
class instance.class method

Example:

```python
class Animal:

    def __init__(self, s, n):

        self.__state = s
        self.__size = n

    def feed(self):

        self.__size += 1
        if self.__size == 5:
            self.__state = "FISH"

    def getState(self):
        return self.__state

    def getSize(self):
        return self.__size

thisFish = Animal("Fish", 1)
print("{} is of size {}".format(thisFish.getState(), thisFish.getSize()))

while thisFish.getState() != "FISH":
    thisFish.feed()

  

print("It is now a big {}".format(thisFish.getState()))
````

Classes can be instatiated by assigning a variable like this:
myVariable = MyClass()

Instatiation is the point at which a variable is created from the class "blueprint".
