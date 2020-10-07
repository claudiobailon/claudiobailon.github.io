# Spring and Websockets

## Interactive Web Application
This is a tutorial that shows you how to build a server that
accepts a message that carries a user's name. In response, the server
will push a greeting into a queue to which the client is subscibed.
### Getting Started
The following bit of code needs to be added to your spring app:<br>
```implementation 'org.webjars:webjars-locator-core'
   implementation 'org.webjars:sockjs-client:1.0.2'
   implementation 'org.webjars:stomp-websocket:2.3.3'
   implementation 'org.webjars:bootstrap:3.3.7'
   implementation 'org.webjars:jquery:3.1.1-1' 
```
### Create a Resource Representation Class
To model the message that carries the name, you can create
a Java object with a name property and corresponding getName() method.

Upon receiving the message and extracting the name, the service
will process it by creating a greeting and publishing that greeting
on a seperate queue to which the client is subscibed. To model
the greeting representation, add another object with a content property
and corresponding getContent() method. 

Spring will use the Jackson JSON library to automatically
marshal instances of message type into JSON.

### Create a Message-Handling Controller
In Spring's approach to working with STOMP(Streaming Text Oriented Messaging Protocol)
 messaging, STOMP messages can be routed to @Controller classes. 

### Finishing the Tutorial
The tutorial continues, showing you how to configure Spring
for STOMP Messaging, create a browser client, make the application
executable, and test the service.  
 
  

  



### Reading Links
[Real time messaging with websockets](https://spring.io/guides/gs/messaging-stomp-websocket/) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 