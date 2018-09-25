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