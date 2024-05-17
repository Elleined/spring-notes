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
      - `Java Config (Semi Automatic)`: Mid level.
      - `Annotation Config (Automatic)`: High level.
   ii. Dependency Injection.
      - The configuration will will be given to the dependency injector
      - It will read/ parse the xml and validate.
      - and create logical memory partition inside JVM
      - and loads all config and place meta data in logical memory partition
      - The logical memory partition created by container is called `IOC` it returns the reference of IOC Container as `BeanFactory`.
      - Basically The logical memory partition is the IOC Container.
   iii. Use beans and used whenever required.
3. Application Context
4. Bean Factory
   - Is the reference of Logical Memory Partition
6. Aspect Oriented Programming

