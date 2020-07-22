# Sending Form Data
 
  
## Overview
A client sends a request to a server using HTTP protocol, then the server answeres the request using the same protocol.  An HTML form on a web stie is a way to configue an HTTP request to send data to a server.  This allows the user to provide information to be delivered in the HTTP request.

## Defining How to Send the Data
The <\form> element defines how the data will be sent.  It's attributes are designed to let you configure the request to be sent when a user hits a submit button.  For what we are doing, the most important attributes are action and method.  

### Action
The action attribute defines where the data gets sent. Its value must be a valid realative or absolute URL.  If it is undefines, the data will be sent to the URL of the current page. How this data is sent depends on the method attribute.

### Method
The method attribute defines how data is sent.  The HTTP protocol provides several ways to perfrom a request; GET, POST, PUT, and DELETE.
GET grabs information, POST creates it, PUT updates it, and DELETE deletes it.  In html, you have to have the middleware of methodOveride to use PUT or DELETE.  



### Reading Links
[Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)<br>
[HTML% Forms Reference](https://htmlreference.io/forms/)<br>
[Video series on Styling HTML5 Forms](https://www.youtube.com/playlist?list=PL4cUxeGkcC9g5_p_BVUGWykHfqx6bb7qK)<br>




[Return to Homepage](https://claudiobailon.github.io/reading-notes/301.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 