# Spring Boot
- dev tools helps not to rerun program after making some changes
- first static block will run then, instance then object??
- if adding not camed in code but showing while fetching
  
# Annotations used
1. SpringBootApplication
2. GetMapping
3. PostMapping
4. RequestMapping
5. RestController
6. Component
7. GetWired
8. DeleteMapping
9. PatchMapping
10. OptionsMapping
11. @Document(collection = "journal_entries") for sql queries
12. Service
13. Autowired


# Lombok - library
It aims to reduce the boilerplate code that developers have to write, such as getters, setters, constructors, and more.

LocalDatetime.Now to fetch todays date

We use to String to fetch the details in our model class because it provide the detail in hashcode format 

# Types of AutoWiring Dependency Injection 
1. Constructor based @NoArgsConstructor
2. Setters based when object not mandatory
3. Autowired when have single class to call

# Implements Serializable 
1. When need to controll the data fetching will implements the Serializable.
   
Logginf level
=============
 
WARN---->
 
TRACE--->
 
INFO---->
 
DEBUG--->
 
FATAL/ERROR-->
 
 
REST->SVC>DAO <br>
TRACE->INFO-> DEBUG

jaha fk hogi waha map nahi lagega in relations
jaha fk hogi waha joinColumn lagega
jaha fk hogi waha setObject krna must he
In cascad we persist to only add the data

Annotations for Controller Advice
--
1. ExceptionHandler
2. ControllerAdvice
3. ResponseStatus
4. 

Collectors.toList() returns a mutable List, typically an ArrayList, which allows modifications (e.g., adding or removing elements).
List.toList() returns an immutable List, which cannot be modified after creation.

Criteria Query 
--
Basically used when we need to apply filters in our queries for example mneed to search by first name
Used methods and Constructors
EntityManager
getCriteriaBuilder

