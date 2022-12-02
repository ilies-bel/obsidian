# Cheatsheet : Spring boot
## Spring annotations
 - `@Configuration`  
   Mark a class as a source of some `@Bean` definitions.
   All `@Bean` within this class will be available in the Spring Context.
 
 - `@Bean`  
   Mark an object to be wired with other **beans** and **components** through dependency injection.
   A method marked with the `@Bean` annotation is a bean producer.
 
 - `@Component`
   Mark a class to be a **component**.
   A component is a class that is instanced into a bean by spring.
   A component is basically a singleton.
   Spring will handle the life cycle of the components for you.
 - `@Repository`  
    Basically the same as `@Component`, but reserved for components of the **persistence layer**
 - `@Service`  
    Basically the same as `@Component`, but reserved for components of the **service layer**
 - `@Controller`  
   Basically the same as `@Component`, but reserved for components of the **presentation layer**
 - `@ComponentScan("com.package")`  
   On a class with `@Configuration`. Tell spring to scan the classpath, into some packages,
   to discover all the classes annotated with `@Component` (or `@Repository`, `@Service`, `@Controller`, ...)
 - `@Autowired`  
   Core of the Spring dependency Injection.
   Put above a field, a setter or the constructor of a bean, instruct spring to provide a bean of the requested type.
   To see the different `@Autowired` possibilities, go to this [guide](https://www.baeldung.com/spring-autowire).
 - `@EnableAutoConfiguration`  
   Spring automatically configures the application based on the dependencies contained the classpath. Already in `@SpringBootApplication`, so do not put both.
 - `@SpringBootApplication`  
   Combination of `@Configuration`, `@EnableAutoConfiguration` & `@ComponentScan` annotations.
 - `@Aspect`  
   Indicates that this is an Aspect.
 - `@Around`  
   Indicates that the method will run before and after the all methods matching with pointcut expression
 - `@Target`  
   Tell us where our annotation will be applicable (`ElementType.METHOD`, `ElementType.FIELD`, `ElementType.CONSTRUCTOR`,...)
 - `@Retention`  
   Whether the annotation will be available to the JVM at runtime or not
## Spring MVC Annotations
 - `@RequestMapping("/controllerMapping")`  
    Should annotate a `@Controller`. Binds the controller to the url `/controllerMapping`.
    
 - `@GetMapping(value = "/endpoint",  produces = "application/json")`  
    On a `Controller` method. Call the method when `HTTP GET controllerMapping/endpoint` is requested.
 - `@PostMapping(value = "/endpoint",  produces = "application/json")`  
    On a `Controller` method. Call the method when `HTTP POST controllerMapping/endpoint` is requested.
  
 - `@PutMapping(value = "/endpoint",  produces = "application/json")`  
    On a `Controller` method. Call the method when `HTTP PUT controllerMapping/endpoint` is requested.
 - `@PatchMapping(value = "/endpoint",  produces = "application/json")`  
    On a `Controller` method. Call the method when `HTTP PATCH controllerMapping/endpoint` is requested.
     
 - `@DeleteMapping(value = "/endpoint",  produces = "application/json")`  
    On a `Controller` method. Call the method when `HTTP DELETE controllerMapping/endpoint` is requested.
    
 - `@ResponseBody`  
    On a `Controller` method. Indicates that the return value of the method should be send on the HTTP response's body
 
| <sub>contact us: <[formation@takima.io](mailto://formation@takima.io)></sub> | <sub>© Takima 2019</sub> |
| --- | ---:|