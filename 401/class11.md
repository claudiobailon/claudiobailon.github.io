# Spring MVC

## Getting Started
Clone the following repository:<br>
git clone https://github.com/spring-guides/gs-serving-web-content.git

cd into gs-serving-web-content/initial

## Create a Web Controller
In spring, HTTP requests are handled by a controller. You can identify the controller by the @Controller annotation.


    @Controller
    public class GreetingController {

    @GetMapping("/greeting")
	public String greeting(@RequestParam(name="name", required=false, defaultValue="World") String name, Model model) {
		model.addAttribute("name", name);
		return "greeting";
	}
The @GetMapping annotation ensures that HTTP GET requests to /greeting are mapped to greeting() method.<br>
@RequestParam binds the value of the query string parameter name to the name parameter of the greeting() method. The implementation of the method body relies on Thymeleaf to perform server-side rendering of the HTML. Tymeleaf parses the greeting.html template and evaluates the th:text expression to render the value of the ${name} parameter.
 
  

  



### Reading Links
[Spring App Basics](https://spring.io/guides/gs/serving-web-content/) <br>
[Spring MVC adn Thymeleaf](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 