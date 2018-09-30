# Topics covered

1. Introduction to Java: Features
1. OOP: Polymorphism, Encapsulation, Inheritance, Abstraction
1. Keywords (new, static, final, etc), naming conventions
1. Constructors (noargs)
1. Methods (signature, return type, parameters)
1. Scopes of a variable (class, object, method, loop)
1. Control Statements (for, foreach, if, while, do while, switch)
1. Arrays, varargs
1. Access modifiers (private, default, protected, public)
1. String API
1. String Pool - String Pool is possible only because String is immutable in Java. Strings are instead stored in heap 
in the **String pool** and are constantly being reused in order to save space. In the instance where two String objects 
contain the same strinng, both of the objects should point to the same string in the string pool. String pool helps
 in saving a lot of space for Java Runtime although it takes more time to create the String.

1. StringBuilder vs StringBuffer
1. Exception handling (try, try with resources, catch, finally)
    2. Finally - an optional portion of a try/catch block that executes regardless.
    2. Try - Attempts to run a snippet of code that may result in an exception. If an exception does occour then it is 
handled by the catch block.
    2. Catch - The **Catch** block runs if an exception is thrown by the try block. you can have multiple catch blocks 
which will activate based on the type of exception thrown.
1. Checked Exceptions - These exceptions are checked by the compiler at run time. The sompiler knows that particular 
things could likley create exceptions thus it requires you to catch these possible execptions.
1. Unchecked Exceptions - These are a type of exception that the compiler cannot predit. This type of exception would 
only be known at runtime. 
1. errors
1. Garbage Collection, finalize()

1. Wrapper Classes - A Wrapper class is a class whose object wraps or contains a primitive data type. ex. Integer
1. Autoboxing -  automatic conversion that the Java compiler makes between the primitive types and their corresponding
object wrapper classes. For example, converting an int to an Integer.

1. Reflection API
1. Inheritance: method overloading and overriding
1. Interfaces vs Abstract classes
1. File I/O, Scanner, input/output byte/character streams
1. Serialization - Serialization is a mechanism of converting the state of an object into a byte stream. 
1. Collection API - The supperclass of several collection datastructure which are used to hold and organize objects.
1. List - A collection that can contain multiples. There are o real restrictions for this collection.
1. Set
1. Map - Similar to a dictionary where each entry is identified by a single key.
1. Iterator, Comparable vs Comparator
1. Thread, Runnable, synchronization

1. Singleton Design pattern
1. Factory Design pattern

1. Unit Testing/JUnit
1. Assert methods, annotations
1. Maven (POM, Lifecycle, repositories)