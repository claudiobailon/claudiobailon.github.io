# jQuery 
 
  
## Overview
jQuery is used to select (query) HTML elements and perform actions on them
Basic syntax is: $('selector').action()
jQuery uses CSS syntax to select elements

Code will run exactly the same in all browsers

jQuery needs to be linked in the html with the following code, above your link to js.
<\script src="https://code.jquery.com/jquery-3.1.1.js"><\/script>

$(function() {
   // jQuery code goes here
});// this makes sure jquery doesn't run until the html page has already loaded
it is the shorthand for the ready code

## Manipulating HTML
the attr method allows you to modify an attribute in HTML from jQuery
the removeAttr method allows you to remove an attribute 

html() and text() methods both grap text from html, with text bringing only text
and html bringing html markup as well as text

the val() method allows us to get and set values of form fields
the append() method inserts content at teh end of the selected elements
the prepend() method inserts content at the beginning of the selected elements
the after() method inserts content after the selected elements
the before() method inserts content before the selected elements.  

## Manipulating CSS
jQuery can also manipulate CSS

the addClass() method adds one or more classes to the selected elements
the removeClass() method removes one or more class names from selected elements
the toggleClass() method toggles between adding/removing classes from the selected elements
this means that if the class exists, it will be deleted, if it doesn't, it will be added

the css() method can be used to get and set css property values

the width() and height() methods can be used to get and set the width and height of html elements, but do not affect margin, border, or padding
innerWidth() and innerHeight() methods include the padding
outerWidth() and outerHeight() methodss include the padding and borders

## Dom manipulation

the parent() method returns the direct parent element of the selected element
the parents() method works like parent() except it selects all ancestors of selected element
the children() method returns all direct children of the selected element
the siblings() method returns all sibling elements of selected element
the next()/nextAll() methods return next/all next sibling elements
the prev()/prevAll() methods return previous/all previous sibling elements of selected element
the eq() method returns element with a specific index number of the selected elements
For example, if the page contains multiple div elements and we want to select the third one:
$("div").eq(2);  the index numbers start at 0, so the third would be 2

We can remove selected elements using the remove() method, which also removes the children of that element
the empty() method is used to remove the child elements of the selected element(s).


## Common Events

The following are the most commonly used events:
#### Mouse Events:
click occurs when an element is clicked.
dblclick occurs when an element is double-clicked.
mouseenter occurs when the mouse pointer is over (enters) the selected element.
mouseleave occurs when the mouse pointer leaves the selected element.
mouseover occurs when the mouse pointer is over the selected element.

#### Keyboard Events:
keydown occurs when a keyboard key is pressed down.
keyup occurs when a keyboard key is released.

#### Form Events:
submit occurs when a form is submitted.
change occurs when the value of an element has been changed.
focus occurs when an element gets focus.
blur occurs when an element loses focus.

#### Document Events:
ready occurs when the DOM has been loaded.
resize occurs when the browser window changes size.
scroll occurs when the user scrolls in the specified element.

## Handling Events

The on() method is used to attach an event to the selected element.
The on() method is useful for binding the same handler function to multiple events. You can provide multiple event names separated by spaces as the first argument. For example, you could use the same event handler for the click and dblclick events.

You can remove event handlers using the off() method. The argument of the off() method is the event name you want to remove the handler for.

We can also trigger events programmatically using the trigger() method. For example, you can trigger a click event without the user actually clicking on an element:
	
The hide() and show() methods are used to hide and show the selected elements.
The toggle() method is used to toggle between hiding and showing elements.

the fadeIn/fadeOut methods fade an element in and out of visibility.
the fadeToggle() method fades in and out.

The slideUp() and slideDown() methods are used to create a sliding effect on elements.
the slideToggle() method switches between the sliding effects and can take two optional parameters: speed and callback.

The animate() method lets you animate to a set value, or to a value relative to the current value.
You need to define the CSS properties to be animated as its parameter in JSON format ("key":"value" pairs).
The second parameter defines the speed of the animation.
For example, the following code animates the width property of the div in 1 second to the value 250px:
$("div").click(function() {
  $("div").animate({width: '250px'}, 1000);
});




### Reading Links
[https://www.codefellows.org/blog/6-reasons-for-pair-programming/](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)
JavaScript and jQuery book by Jon Duckett pages 293-301, 306-331 and 354-357
Skim pages 302-305 and 332-335

[Return to Homepage](https://claudiobailon.github.io/reading-notes/301.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 