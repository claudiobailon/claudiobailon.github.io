# RecyclerView

## Overview
If your app need to display a scrolling list of elements based on large 
data sets, you should use RecyclerView.

The RecyclerView widget is a more advanced and flexible version of ListView.

In the RecyclerView model, several different components work together to
display your data. The overall container for your user interface is a RecyclerView
object that you add to your layout. The RecyclerView fills itself with views 
provided by a layout manager that you provide. you can use one of the standard 
layout managers, or implement your own.

The views in the list are represented by view holder objects. These objects are 
instances of a class you define by extending RecyclerView.ViewHolder. Each view 
holder is in charge of displaying a single item with a view. For example, if your 
list shows music collection, each view holder might represent a single album. The 
RecyclerView creates only as many view holders as are needed to display the on-screen 
portion of the dynamic content, plus a few extra. As the user scrolls through the list, 
the RecyclerView takes the off-screen views and rebinds them to the data which is 
scrolling onto the screen.

The view holder objects are managed by an adapter, which you create by extending 
RecyclerView.Adapter. The adapter creates view holders as needed. The adapter also binds 
the view holders to their data. It does this by assigning the view holder to a position, 
and calling the adapter's onBindViewHolder() method. That method uses the view holder's 
position to determine what the contents should be, based on its list position.
 
  

  



### Reading Links
[RecylcerView For Displaying Lists of Data](https://developer.android.com/guide/topics/ui/layout/recyclerview#java) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 