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
1. Finally - an optional portion of a try/catch block that executes regardless.
1. Try - Attempts to run a snippet of code that may result in an exception. If an exception does occour then it is 
handled by the catch block.
1. Catch - The **Catch** block runs if an exception is thrown by the try block. you can have multiple catch blocks 
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
1. Inheritance - The ability for children to **Inherit** the preexisting fields and methods of the parent class.
1. Polymorphism - The ability for children to change the functionality of inherited methods.
1. Method overloading - This can be done either to a method within the child or to an inherited method. Overloading is 
where you have multiple methods of the same name but have diffrent arguments.
1. Overriding - **Overriding** is the more blatant use of polymorhpism where a child re-implements or augments the 
functionality of a parent method.

1. Interfaces - Identified by the keyword: implement. **Interface** can only include abstract methods.
1. Abstract classes - Identified by the keyword: extends. **Abstract** classes can include both concrete and absract 
methods with the only requirement beig that is contains at least one abstract method. Both **Abstract** and **Interfaces** 
are used for providing abstraction to your programming. A rule of thumb when deciding which to use, if class A doesn't 
share any common code eith class B then use an interface.

1. File I/O, Scanner, input/output byte/character streams
1. Serialization - Serialization is a mechanism of converting the state of an object into a byte stream. 
1. Collection API - The supperclass of several collection datastructure which are used to hold and organize objects.
1. List - A collection that can contain multiples. There are o real restrictions for this collection.
1. Set -  collection of non duplicate elements meaning there will never exist a situation where element1.equals(element2)
1. Map - Similar to a dictionary where each entry is identified by a single key.
1. Iterator, Comparable vs Comparator

1. Thread - **Thread** is a class in java which allows for the creation and managing of threads. Threads allow for a 
programmer to create applications that will run on multiple cores concurretly.
1. Runnable -  is an interface that is to be implemented by a class whose instances are intended to be executed by a thread.
By defining a Run method, you tell **Thread** where the entry point for this thread is.
1. Synchronization -  is the capability to control the access of multiple threads to any shared resource. This is important
 because without **syncronization** you could create a deadlock if two threads try to access the same resource ast the same time.

1. Singleton Design pattern
1. Factory Design pattern

1. Unit Testing/JUnit
1. Assert methods, annotations
1. Maven (POM, Lifecycle, repositories)