# Spring Framework
Spring is a framework designed to move away from the tightly-coupled world of EJBs. It provides service locators, IoC (Inversion of Control) Containers, and Dependency Injectors to help separate business logic from code unrelated to the business process (logging, exception handling, instantiations).

### Service locator
A library Spring uses to register and list available functions and services as Beans to instantiate.

### Inversion of Control
A way for Spring to deal with abstraction, to insert behavior, and let the framework call and connect your code.

### Dependency Injection
This is a form of IoC where dependencies are passed to us at time of instantiation. 

## Benefits
- Depcouple task execution from implementation
- Separation of concerns, modularity, focus on business logic
- Loose coupling where code is unaffected by changes in other files

## Configuration
- XML (in a beans.xml)
- Annotations (@Component, @Bean, @RestController)
- Main goal is to configure the Spring Container with registered beans (POJOs) and configuration metadata

## Spring Core
- spring-core, spring-beans, spring-context, spring-aop*
- core/beans are essential for IoC behavior (BeanFactory)
- context contains ApplicationContext, essentially a superset of BeanFactory for more enterprise specific functionality

### BeanFactory
Now a rarely used interface for sophisticated implementation of the factory pattern. It lazily instantiates beans by programmatically creating singletons.

### ApplicationContext
Extends BeanFactory to eagerly instantiate beans, can be instantiated itself with
```java
ApplicationContext ac = new ClassPathXmlApplicationContext("file");
ApplicationContext ac = new FileSystemXmlApplicationContext("C:\\file");
ApplicationContext ac = new XmlWebApplicationContext("file");
```

## Beans
Objects managed by Spring, named similarly to EJBs (Enterprise Java Beans) which functioned similarly in JEE spec.

#### Defining beans
- XML: 
```xml
<bean name="animal" class="com.revature.beans.Animal"></bean>
```
- Annotations:
```java
@Component(name="animal")
public class Animal {...}
```
Annotations use stereotypes:
- @Component: Generic for spring-managed objects
- @Repository: for DAOs
- @Service: for services
- @Controller: for UI controllers

## Bean Lifecycle
ApplicationContext is in charge of the lifecycle of bean objects. First it goes through a setup process where the object is instantiated, dependencies are handled, any custom init methods are called, and then the bean is made ready for use. Once the ApplicationContext is shutting down, then any custom destroy methods are called.
### Actual lifecycle steps:
1. Instantiate Bean
1. Populate Bean
1. if BeanNameAare
    1. SetBeanName()
1. if BeanFactoryAware
    1. SetBeanFactory()
1. BeanPostProcessor Pre-Initialization
1. afterPropertiesSet() Initialization
1. Optional custom init methods
1. BeanPostProcessor Post-Initialization
1. Bean is ready for use
1. destroy() then custom destroy called when container shuts down

Mostly, we let Spring handle this in the background, but it's possible to override some of it.
We can implement:
- org.springframework.beans.factory.InitializingBean and then override afterPropertiesSet()
- org.springframework.beans.factory.DisposableBean and then override destroy()

But these are bad ideas because it tightly-couples your code with Spring. So instead we define custom methods
- XML
```xml
<beans>
    <bean name="animal" 
    class="com.revature.beans.Animal" 
    init-method="customInit" 
    destroy-method="myDestroyMethod"></bean>
</beans>
```
- Annotations
    - @PostConstruct
    - @PreDestroy