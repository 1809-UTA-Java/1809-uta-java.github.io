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


producer consumer problem. threading pet problem