# The Call Stack
 
  
## Overview
A call stack is a mechanism for an interpreter to keep track of its place in a script that calls multiple functions: what funtion is currently being run and what functions are called from within that function, etc. Basically, it's a data structure that uses the Last In, First Out(LIFO) principle to temporarily store and manage function invocations.<br>
* When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
* Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
* When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing. 
* If the stack takes up more spave than it had assigned to it, it results in a "stack overflow" error. 

So, we start with an empty call stack. Whenever we invoke a funtion, it is automatically added to the top of the call stack. Once that function has executed all of its code, it is automatically removed from the call stack, eventually leading to an empty call stack.



### Reading Links
[The Call Stack defined on MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)<br>
[Understanding the JavaScript Call Stack](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)<br>
[JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)<br>
[JavaScript errors reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)<br>





[Return to Homepage](https://claudiobailon.github.io/reading-notes/301.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 