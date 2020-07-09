# CSS Grid
 
  
## Overview
CSS Grid Layout is the most powerful layout system available in CSS. It is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system. You work with Grid Layout by applying CSS rules both to a parent element (which becomes the Grid Container) and to that element’s children (which become Grid Items).

## Grid Garden Notes
grid-column-start changes start to a differend grid column
 
When grid-column-start is used alone, the grid item by default will span exactly one column. However, you can extend the item across multiple columns by adding the grid-column-end property.grid-column-end 
 
grid-column-end doesn't have to be bigger than start, it will span the difference. 
 
If you want to count grid lines from the right instead of the left, you can give grid-column-start and grid-column-end negative values. For example, you can set it to -1 to specify the first grid line from the right.
 
Instead of defining a grid item based on the start and end positions of the grid lines, you can define it based on your desired column width using the span keyword. Keep in mind that span only works with positive values.
 
grid-column is a shorthand that accepts both grid-column-start and grid-column-end as values, seperated by a slash. i.e. grid-column:2/4;
 
grid-row-start works much like grid-column-start except along the vertical axis.
Likewise, grie-row works just as grid-column.
  
You can use both at the same time to navigate entire grid
  
grid-area accepts four values separated by slashes: grid-row-start, grid-column-start, grid-row-end, followed by grid-column-end.

If grid items aren't explicitly placed with grid-area, grid-column, grid-row, etc., they are automatically placed according to their order in the source code. We can override this using the order property, which is one of the advantages of grid over table-based layout.

By default, all grid items have an order of 0, but this can be set to any positive or negative value, similar to z-index.

grid-template-columns and grid-template-rows divides the page in columns and rows based on percentage. An equal 5x5 grid would look like this:
grid-template-columns: 20% 20% 20% 20% 20%;
grid-template-rows: 20% 20% 20% 20% 20%;

column and row templates can be shorthanded using repeat. The above lines can be written like this:
grid-template-columns: repeat(5, 20%);
grid-template-rows: repeat(5, 20%);

You can also set sizes by pixels or em and a new unit of fr

fr unit allocates one share of the available space. For example, if two elements are set to 1fr and 3fr respectively, the space is divided into 4 equal shares; the first element occupies 1/4 and the second element 3/4 of any leftover space.

grid-template is a shorthand property that combines grid-template-rows and grid-template-columns.
For example, grid-template: 50% 50% / 200px; will create a grid with two rows that are 50% each, and one column that is 200 pixels wide.



### Reading Links




[Return to Homepage](https://claudiobailon.github.io/reading-notes/)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 