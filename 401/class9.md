# WRRC In Java

## A simple Java HTTP request

The HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries. All the classes that are needed are contained in the java.net package.<br>
A HttpUrlConnection instance is created by using the openConnection() method of the URL class. Note that this method only creates a connection object, but does not establish the connection yet.

The HttpUrlConnection class is used for all types of requests by setting the requestMethod attribute to one of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.
If we want to add parameters to a request, we have to set the doOutput property to true, then write a String of the form param1=value¶m2=value to the OutputStream of the HttpUrlConnection instance:

 
  

  



### Reading Links
[High Level HTTP](https://dev.to/dangolant/things-i-brushed-up-on-this-week-the-http-request-lifecycle-) <br>
[Java HTTP request example](https://www.baeldung.com/java-http-request) <br>



[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 