# Room

## Save data in a local database using Room

Room provides an abstraction layer over SQLite to allow fluent database access while
harnessing the full power of SQLite.
 
Apps that handle non-trivial amounts of structured data can benefit greatly from 
persisting that data locally. The most common use case is to cache relevant pieces of 
data. That way, when the device cannot access the network, the user can still browse 
that content while they are offline. Any user-intiated content changes are then syned to 
the server after the device is back online. 

Because Room takes care of this for you, it is highly recommneded using Room instead 
of SQLite. 

To use Room in your app, add these dependencies to your app's build.gradle file:
```
dependencies {
  def room_version = "2.2.5"

  implementation "androidx.room:room-runtime:$room_version"
  annotationProcessor "androidx.room:room-compiler:$room_version"

  // optional - RxJava support for Room
  implementation "androidx.room:room-rxjava2:$room_version"

  // optional - Guava support for Room, including Optional and ListenableFuture
  implementation "androidx.room:room-guava:$room_version"

  // optional - Test helpers
  testImplementation "androidx.room:room-testing:$room_version"
}
```
There are 3 major components in Room:
* Database: Contains the database holder and serves as the main access point for the 
underlying connection to your app's persisted, relational data. The class that's 
annotated with `@Databaase` should be an abstract class that extends `RoomDatabase`, 
include the list of entities associated with the database within the annotation, and 
contain an abstract method that has 0 arguments and returns the class that is annotated 
with `@Dao`.
* Entity: Represents a table within the database.
* DAO(Data Access Objects): contains the methods used for accessing the datbase. 

The app uses the Room database to get DAOs associated with that database. The app 
then uses each DAO to get entities from the database and save any changes to those 
entities back to the database. Finally, the app uses an entity to get and set values 
that correspond to table columns within the database.

![Room Achitecture](../images/room_architecture.png)



### Reading Links
[Overview: Saving data with Room](https://developer.android.com/training/data-storage/room) <br>
[Defining entities in Room](https://developer.android.com/training/data-storage/room/defining-data) <br>
[Related entities in Room](https://developer.android.com/training/data-storage/room/relationships) <br>
[Accessing data with Room](https://developer.android.com/training/data-storage/room/accessing-data#java) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 