# Java - Tuesday
## Variables
A value is stored and identified in memory by a variable. Variables have a name that makes it possible to access the value, and a type that defines what sort of value it stores.
>int variableName = 5;

>String txtVar = "Hello World";

## Primitive data types
Java handles two kinds of datatypes: primitives and references. Primitives are variables that store simple values. There are eight in Java.
-Integer types: **byte**, **short**, **int**, and **long** (42)  
-Floating-point types: **float**, and **double** (3.1415)  
-Logical types: **boolean** (true)  
-Character type: **char** ('x')

## Reference types
Reference types store the memory address location of more complex data types. They are most commonly used to point to the location of objects in memory, and are checked by the garbage collector regularly. If an object has no reference, it will eventually be removed from memory.

## Naming variables
- Case sensitivity
- Can only use letters, numbers, and *$* or *_* characters
- Cannot begin with a number
- Cannot be a reserved Java keyword

## Scopes of a variable
A variable's reference will only exist within the context of its declared scope, which is based on the location of its declaration.

**Static** or class scoped variables are visible to all instances of a related class.
**Instance** or object scoped variables are visible to only that object instance.
**Local** or method scoped variables are visible only within a method.
**Block** or loop scoped variables are visible only within a block statement.

Be aware of shadowing, when two variables in different scopes share names.

## Methods
Methods accept a list of arguments known as *parameters* and return some value. They are used to implement repeatable, consistent actions on variable input, much like math functions.
>public int myMethod(int a, int b);

>public int myMethod(int a);

## Constructors
Classes not only define object fields and methods, but how it should be instantiated through special methods called constructors. Contructors must have no return type and share the same name as its class. Java will automatically give you a *noargs* contructor. However, if you define any constructor, you will lose the automatically given constructor.

While a constructor may be *private*, used for singletons, it may not be *final*, *static*, or *abstract*.

## Access modifiers
**private** - accessible only within the context of that class
**default** - accessible within the context of a package, has no associated keyword so is set when no modifier is used
**protected** - accessible to the package, but also to derived child classes outside of the package
**public** - accessible anywhere

Classes should only be public or default. There are no cascading access levels, and unspecified fields will be default. Subclasses can only change inherited fields to be less restrictive.