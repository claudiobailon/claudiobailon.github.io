# Google Teamwork and CSS Animations

## CSS Animations
### The Transform property
Elements can be transformed  on both a two-dimensional and three-dimensional plane.  2d transforms work on the x and y axes, while 3d works on x, y, and z axes.  The transform property in CSS accepts a handful of different values.  The rotate value provides the ability to rotate an element from 0 to 360 degrees. A positive value will rotate an element clockwise, while a negative value will rotate it counter-clockwise.  The rotate value is taken in like this: "transform: rotate(90deg)"; this will rotate 90 degrees clockwise.

The scale value allows you to change the appeared size of an element.  1 is the default, values between .01 and .99 will make it smaller, and values greater than 1 will make it larger. It is implemented like this: "transform: scale(1.5)", which will make the element 1.5 times larger.  You can also scale just the width with scaleX, just the height with scaleY, or both with a normal scale but passing in the x scale factor first, followed by a comma and y scale factor. "transform: scale(.5, 1.5)" would bake the width shrink in half and the height grow 1.5 times.

You can move the position of an element with the translate value.  You can move the x or y position alone with translateX or translateY value, or both by passing in the x then the y.  The value can be passed in as both a pixel or percentage. Positive values will push an element down and to the right, while negative values do the opposite.   "transform: translate(-20px, 50%)" would move the element to the left 20 pixels and down half of the height of the element.

The skew value is used to distort an element on it x axis, y axis, or both, with similar syntax to the translate and scale values. The distance calculation of the skew value is measured in units of degrees, like the rotate value.   

You can combine values by listing the transform values within the transform property one after the other without the use of commas. " transform: rotate(25deg) scale(.75) skew(10deg, 20deg) translateX(20px)" would rotate an element 25 degrees clockwise, scale it down to 75% of it's size, skew it's x-axis 10 degrees and y axis 20 degrees, and moves it down 20 pixels.




[Return to Homepage](https://claudiobailon.github.io/reading-notes/)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training  
