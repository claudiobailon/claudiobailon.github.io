# Spring Authentication(Continued)

## Spring Boot and OAuth2
### Securing the Application with Spring Security
To make your application secure, add Spring Security as a 
dependency. Here is the code:<br>
`<dependency>`<br>
   `<groupId>org.springframework.boot</groupId>`<br>
	`<artifactId>spring-boot-starter-oauth2-client</artifactId>`<br>
`</dependency>`<br>
### Add a new GitHub app
To use GitHub's OAuth2.0 authentication system for login, you must first [add
a new github app](https://github.com/settings/apps). 
Select "New OAuth App" and then the "Register a new OAuth application" page is presented. 
Enter an app name and description, then add a home page at http://localhost:8080. Lastly, 
indicate the Autorization callback URL as http://localhosts:8080/login/oauth2/code/github and click
register application. 
 
  

  



### Reading Links
[OAuth tutorial](https://spring.io/guides/tutorials/spring-boot-oauth2/) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 