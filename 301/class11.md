# EJS
 
  
## Overview
EJS stans for Embeded JavaScript, and it is a simple templating language(like mustache) that lets you generate HTML markup with plain JavaScript. It's great to use because of it's ability to use JavaScript, fast develpment time, simple syntax, and easy debugging.

## Getting Started

### Install
To install, run the following command in the terminal: npm install -S ejs

### Use
To use, in your server.js require ejs , create a variable you want to pass, and pass EJS a template string. I.E.

let ejs = require('ejs');<br>
let people = ['Claudio', 'Kate', 'Paul', 'Gracie'];<br>
let html = ejs.render('<%= people.join(", "); %>', {people: people});<br>





### Reading Links
[Watch EJS tutorial from WalkThroughCode on YouTube, Videos 1-5](https://www.youtube.com/playlist?list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)<br>
[Google Books API Docs](https://developers.google.com/books/docs/v1/using#WorkingVolumes)<br>
[EJS Docs](https://ejs.co/)<br>
[EJS Tutorial](https://scotch.io/tutorials/use-ejs-to-template-your-node-application)<br>
[Source Code for the EJS Tutorial](https://github.com/scotch-io/node-ejs)<br>




[Return to Homepage](https://claudiobailon.github.io/reading-notes/301.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 