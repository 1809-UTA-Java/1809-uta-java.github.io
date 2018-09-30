<<<<<<< HEAD
library
framework
junit
unit testing
@@@@@Add enums to thursday
@Test is calling the Test methd from junit and is incorporating your method into it? this is managed by he junit runner
junit eliminates the need for a main method

maven
mvn 
maven is a build tool
is it also a package manager?

maven is a fork of ant which aimed to simplify usage. it is currently maintained by apache
maven can build a blank java project for you
>mvn srchetype:generate -DgroupId=com.revature -D archetypArtifacteId=maven-archetype-quickstart -DinteractiveMode=false

maveb typically detects when you make a change and will rebuild your project. in the case that it does not use 
>mvn clean package

maven is ide agnostic thus you can import maven projects into any ide. this means that people on the same team can you diffrent tools
pom.xml is the main config for maven. it is what controls the updates

mvnrepository.com   wwill generate xml dependencies for your maven config
eclpise

group id = package name
artifact id: project name


design patterns
singleton - only one instance can be made and used
factory - give it a small amount of info and it does all the work for you. factory is good because if you were to modify an objects constructor, suddenly everywhere you instanciate an object there would be an error now. instead we can just change the factory and how it creates things without ruining any constructors

threading

producer consumer problem. threading pet problem will need to know for monday

syncronization and deadlocks


generics
=======
# Maven 
Build automation and dependency management tool. Once installed, use with the `mvn` command. Allows for a project to be IDE agnostic.

## Example commands
Create a new Maven project with the quickstart archetype. Change groupId and artifactId arguments as needed:
>mvn archetype:generate -DgroupId=com.revature -DartifactId=my-first-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

Package project into a jar
>mvn package

Remove target folder and compiled build
>mvn clean

Run JUnit tests
>mvn test

# Threads
A *thread* is a unit of program execution that runs independently from other threads. Java programs can consist of multiple threads of execution that behave as if they were running on independent CPUs.

- `java.lang.Thread` is the Thread class representing a thread, which you can extend and then override its run() method. Afterwards, you call start().
- `java.lang.Runnable` is a functional interface (meaning only one method) which you can implement and then override run(). Afterwards, you can pass the object to a Thread instance and run start().
- The `synchronized` keyword is a modifier that can be used to write blocks of code, methods, or other resources to protect it in a multithreaded environment.
- `wait()` and `notify()` or `notifyAll()` methods of `java.lang.Object` can be used to suspend or wake up threads.

>>>>>>> 6a8f8ef8da54ceef77a4ddb2a972547097ae0882
