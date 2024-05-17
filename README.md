# spring-notes
Notes for Spring and Spring Boot

# Spring Framework goal:
- Make J2EE application development easier.


## What is J2EE
- Comes with: Servlet, JSP(Java Server Pages), RMI, EJB, and etc...
### J2EE Drawbacks:
- Tightly coupled.
- Heavyweight
- Boilerplate code.
- Doesnt support security and transaction.

## Spring advantages
- Make application development easy
- Light weight
- Different dedicated Spring Module example: mvc, batch, jpa, and many more.
- Popular to loosy coupled front end and backend also the unit testable code.

#### Spring core is the base for all spring module for them to have communication with the use of interfaces.

## Spring core fundatmentals
1. Dependency injection
   - Is the process of getting the object from container to have loosely coupled and unit testable code.
   ## Two ways to manage dependencies
   - `Dependency lookup (Manual)`  
   - `Dependency injection (Automatic)`  
   ## 2 Parts of DI
   - `Dependent`: User of aggregate field.
   - `Dependency`: The aggregate field.
   ## 3 Types of DI
   - `Constructor (Prefer way and the only way)`: User of aggregate field.
   - `Setter (Use only in special occations)`: User of aggregate field.
   - `Field (Not Recommended)`: User of aggregate field.
2. Inversion of Control
   - Collaboration of objects and managing the life cycle of object is called IOC.
   - Inversion means get all the dependencies through one class.
     - `Collaboration`: Managing dependencies.
     - `Life Cycle`: Instantiation and Destruction.
   ### Steps on implementing IOC
   i. Configuration
      - Configuration doesn't provide object its just used for spring to understand what object will be created.
      ## 3 ways of Configuration.
      - `XML Config (Manual)`: Low level.
      ### Drawbacks of XML Config and Why you should not used XML Config
         - Need to learn XML
         - Cannot detect error in compile time
         - Hard to read
         - Need to switch between java file and xml file which is tiresome
         - Condition based bean creation are not supported.
   
      - `Java Config (Semi Automatic)`: Mid level.
      - `Annotation Config (Automatic)`: High level.
      ### Advantages of Annotation Config and Why you should use Annotation Config instead of other two
         - Annotation config solves all the drawbacks of both XML and Java config with used of @Component, @Autowired and @ComponentScan ant many more annotations.
   ii. Dependency Injection.
      - The configuration will will be given to the dependency injector
      - It will read/ parse the xml and validate.
      - and create logical memory partition inside JVM
      - and loads all config and place meta data in logical memory partition
      - The logical memory partition created by container is called `IOC` it returns the reference of IOC Container as `BeanFactory`.
      - Basically The logical memory partition is the IOC Container.
   iii. Use beans and used whenever required.
4. Application Context
5. Bean Factory
   - Is the reference of Logical Memory Partition
   - Spring Container contains all the object reference created by dependency injector.
   - If you want an object get it from spring container instead of creating it yourself.
   ## Bean factory heirarchy
   ![Hi](https://github.com/Elleined/spring-notes/assets/111877930/f40d126a-1a5e-4580-910f-8db7f034163e)
6. Aspect Oriented Programming

# When you should use Constructor Injection and Setter Injection.
## Constructor Injection (Preffered)
1. Use `Dependency injection` if the dependency is required
2. If Depedency is final
3. Depedency Cyclic not supported

## Setter Injection
1. If Dependency is optional
2. if depedency is not final
3. Depedency cyclic are supported

# Spring Scopes
- Never inject a shorter lived bean into longer lived bean.

1. Singleton
- Use Singleton if data will be the same for every request.
- Is different from singleton design pattern. Singleton spring is singleton per container/ per bean definition meaning every bean definition are different and singleton on their own not the whole application.

3. Prototype
- Use prototype if data will be different after every request.
- Nutiple object per bean definition.
- Spring container will have no reference to prototype it will just create and destroy.

# [Annotations Notes](https://github.com/Elleined/spring-boot-annotations-notes)


