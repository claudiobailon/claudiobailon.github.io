# Integration Testing

## Enabling Spring in Tests

Any Spring enabled test will run with the help of @RunWith(SpringJUnit4ClassRunner.class); the runner is essentially the entry-point to start using the Spring Test framework.

We also need the @ContextConfiguration annotations to load the context configuration and bootstrap the context that the test will use.
In the @ContextConfiguration we provide the ApplicationConfig.class config class which loads the configuration we need.
 
 `@RunWith(SpringJUnit4ClassRunner.class)
 @ContextConfiguration(classes = { ApplicationConfig.class })
 @WebAppConfiguration
 public class GreetControllerIntegrationTest {
     ....
 }`
## The WebApplicationContext Object
WebApplicationContext(wac) proviides web application configuration.
We can wire the web application context into the test.

## Mocking Web Context Beans
MockMVC provides support for Spring MVC testing. It encapsulates all web app beans and makes them available for testing.
  



### Reading Links
[Sring Integration Testing](https://www.baeldung.com/integration-testing-in-spring) <br>
[Working with Relationships In Spring Data REST](https://www.baeldung.com/spring-data-rest-relationships) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 