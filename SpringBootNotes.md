--
.\mvnw
--
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

Model Mapper
--
config file 


Github
--
https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbE9IV2FZN0ZtTzF6cWpWcml4ZHltTTlPdTdlQXxBQ3Jtc0ttS0JYaDRvVUYydElyVG5wRzlrSnBodHRsQnRYUnppTUxHaUR3dHUwOXR2LXpEVHN3dnF0bEJJYXBfd3kxc29tZ3p5SF9WdFh3SjE4QWRxRENxazlWTDVZMmx4N2FOc3lsNlZmc1N4VF9fdzZrcWd1UQ&q=https%3A%2F%2Fwww.learncodewithdurgesh.com%2Fblogs%2Fmaven-tutorial&v=ybQAmFsVQqA

Testing
--
1. Unit Testing - multiple components individual testing<br> 
test driven development - with dev test<br>
JU - java unit<br>
SpringBootTestAnnotation - works as an application context.<br>
@Test<br>
@ParametrizedTest<br>
AssertTrue, Equal and more.<br>
CsvSource, ValueSource, CsvFile, EnumSource, ValueSource.<br>
CodeCoverage plugin to install.<br>
@BeforeEach, BeforeAll, AfterEach, AfterAll;

Functional interface lambda, bean lifecycle.

less than 5 sec = sync 
Spring Profile

<h2> 1. Spring Profile Configuration </h2>
spring.profiles.active = dev

<h2>Mockito</h2>
1. Mockito is a framework used for creating mock objects in unit tests. It’s generally used for testing individual components in isolation.
2. 
@RunWith(MockitoJUnitRunner.class)
public class MyServiceTest {

    @Mock
    private MyRepository myRepository;

    @InjectMocks
    private MyService myService;

    @Test
    public void testServiceMethod() {
        // Arrange
        when(myRepository.someMethod()).thenReturn(someValue);

        // Act
        myService.serviceMethod();

        // Assert
        verify(myRepository).someMethod();
    }
}

2. WebMockMvc

WebMockMvc (commonly known as MockMvc) is a class provided by Spring Test to test Spring MVC controllers. It allows you to perform integration tests on your web layer.

JUnit5 = JUnit Platform + JUnit Jupiter + JUnit Vintage.

@DisplayName

--
Swagger
---
-> Open API Specification
It defines a standardized format for describing APIs comprehensively
<br>

Swagger is an open-source framework used for designing, building, documenting, and consuming RESTful APIs. It provides a standardized way to describe the structure of an API, making it easier for developers to understand, integrate, and consume the API.

<br>
<b>Springfox</b>

Springfox is a Java library used to integrate Swagger with Spring Boot applications. It automatically generates Swagger documentation from your Spring controllers and models.
springfox-boot-starter: A starter dependency to quickly set up and integrate Springfox into a Spring Boot project.

<br>
<b>For latest version Springdoc Open API</b>

Springdoc OpenAPI is an alternative to Springfox. It is designed to generate API documentation from Spring Boot applications using the OpenAPI 3 specification, which is the latest iteration of the Swagger specification.
springdoc-openapi-ui: A module that integrates Spring Boot applications with Swagger UI using the OpenAPI 3
specification.
<br>
localhost:8081/swagger-ui/index.html

1. It scans our Spring Boot application for REST controllers and generates the corresponding API documentation
It automatically generates API documentation without additional configuration

2. Springdoc OpenAPI also scans our application for
classes that are used as request bodies or response
bodies.

--
For Customization of swagger
--
1. to create configuration file - info, servers, tags(for ordering)
2. @Tag to change heading of every method
3. @Operation in controller

--
File I/O
--
1. FileInputStream
   - Usage: Reads bytes from a file.
   - When to Use: When you need to read data from a local file.
3. ByteArrayInputStream
   - Usage: Reads bytes from a byte array.
   - When to Use: When you have data already in memory and want to treat it as an input stream.
4.  BufferedInputStream
   - Usage: Buffers input to provide efficient reading of bytes.
   - When to Use: When reading from a slow source (like a file or network) to improve performance.
5. DataInputStream
   - Usage: Allows reading primitive data types from an underlying input stream.
   - When to Use: When you need to read Java primitives (like int, float) from a stream.
6. PipedInputStream
   - Usage: Provides an input stream connected to a piped output stream.
   - When to Use: For inter-thread communication, allowing one thread to read data written by another.
7. ServletInputStream
   - Usage: Used in servlets to read binary data from HTTP requests.
   - When to Use: In web applications to handle file uploads or binary data in requests.
8. URLConnection.getInputStream()
   - Usage: Retrieves an input stream for reading data from a URL.
   - When to Use: When you need to read data from a web resource.
8. ObjectInputStream
   - Usage: Reads objects from an input stream.
   - When to Use: When deserializing objects from a stream.

No manipulation of data required - transferTo
--
Design patterna
--
creational, structural, behavioural


--
Golang
--
processor -> parallelism
concurrency -> multiple processes at single processor

threads virtual or in object form 


ttl 

type safety

