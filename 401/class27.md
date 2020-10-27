# GraphQL

## @connection
The `@connection` directive enables you to specify relationships between 
`@model` types.  Currently, this supports one-to-one, one-to-many, and 
many-to-one relationships. You may implement many-to-many relationships 
using two one-to-many connections and joining `@model` type. 

Relationships between types are specified by annotating fields on an `model` 
object type with the `@connection` directive. The `fields` argument can be 
provided and indicates which fields can be queried by to get connected objects. 
The `keyName` argument can optionally be used to specify the name of secondary 
index (an index that was set up using @key) that should be queried from the other 
type in the relationship.  

When specifying a `keyName`, the `fields` argument should be provided to indicate 
which field(s) will be used to get connected objects. If `keyName` is not provided, 
then `@connection` queries the target table's primary index. 


 
  

  



### Reading Links
[GraphQL](https://docs.amplify.aws/cli/graphql-transformer/connection) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 