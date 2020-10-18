# Android Basics

## Application Fundamentals
Android apps can be written using Kotlin, Java, and C++. The android
SDK tools compile your code along with any data and resource files into an
APK (Android Package), which is an archive file with an .apk suffix. One APK 
file contains all the contents of an Android app and is the file that Android-
powered devices use to install the app.<br>

Each Android app is protected by these security features:
* The Android operating system is a multi-user Linux system where
each app is a different user.
* By default, the system assigns each app an unique Linux user ID and sets permissions
for all the files in an app so that only the user ID assigned to that app can access them.
* Each process has its own virtual machine, so an app's code runs in isolation from other apps.
* By default, every app runs in its own Linux process. The android system starts the process when
any of the app's components need to be executed, and then shuts it down when it's no longer needed
or when the system must recover memory for other apps.

The Android system implements the priciple of least privilege, where each app, by default, only
has access to the components that it requires to do its work, and nothing else, which creates a secure
environment. 

An app can share data with other apps and access system services.  It can be 
arranged so that two apps share the same Linux user ID adn therefore access each other's files.
An app can also request permission to access device data such as teh device's location, camera, and
Bluetooth connection, but the user has to explicitly grand these permissions. 

## App components
App components are the essential building blocks of an Android app. Each component is an entry point 
through which the system, or a user, can enter your app. Some components depend on others.

There are four different types of app components, and each type serves a distinct purpose and has a 
distinct lifecycle that defines how the component is created and destroyed. 
### Activities
An activity is the entry point for interacting with the user. It represents a single screen with a user 
interface. For example, an email app might have one activity that shows a list of new emails, another to
compose an email, and another for reading emails. Each activity works with the rest to form a cohesive 
user experience, but is also independent of the others. Therefor, a different app can start any one activity
if it's app allows it. 

You implement an activity as a subclass of the `Activity` class.
### Services
A service is a general-purpose entry point for keeping an app running in the 
background for all kinds of reasons. It is a component that runs in the background
to perform long-running operations or to perform work for remote processes. A service does not provide
a user interface. For example, a service might play music in the background while the user is in a 
different app, or fetch data over the network without blocking user interaction with an activity. Another 
component, like an activity, can start teh service and let it run or bind to it in order to interact with it.


There are two very distinct semantics services tell the system about how to manage an app. 
* Started services tell the system to keep them running until their work is completed. There are two different types of started services, 
one that the user is aware of, like music playing, and another that the user isn't directly aware of so the system 
can stall it or kill it if need be without the user being affected. 
* Bound services run because some other app (or the system) has said that it wants to make use of the service. 
This is basically the service providing an API to another process.  The system thus knows there is a dependency between
these processes, so if process A is bound to a service in process B, it knows that it needs to keep process B (and its service) running for A.
Further, if process A is something the user cares about, then it also knows to treat process B as something the user also cares about. 
Because of their flexibility (for better or worse), services have turned out to be a really useful building block for all kinds of 
higher-level system concepts. Live wallpapers, notification listeners, screen savers, input methods, accessibility services, and many 
other core system features are all built as services that applications implement and the system binds to when they should be running.

A service is implemented as a subclass of `Service`.
### Broadcast Receivers
A broadcast reciever is a component that enables the system to deliver events to the app outside of a regular user flow, allowing 
the app to respond to system-wide broadcast announcements. Because broadcast recievers are another well-defined entry into the app, 
the system can deliver broadcasts even to apps that aren't currently running. So, an app can schedule an alarm to post a notification to tell
the user about an upcoming event, and by delivering that alarm to  a Broadcast Reciever of the app, these is no need for the app to remain
running until the alarm goes off. Many broadcasts orginate from the system. For example, a broadcast announcing the screen has been turned off,
the battery is low, or a picture was taken.  But apps can also initiate broadcasts, like to let other apps know that some data
has been downloaded to the device and is available for them to use. Although broadcast recievers don't display a user interface,
they can create a status bar notification to alert the user when a broadcast event occurs. 

A broadcast reciever is implemented as a subclass of `BroadcastReceiver` and a broadcast is delivered as an `Intent` object.
### Content Providers
A content provider manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, 
or on any other persistent storage location that your app can access. Through the content provider, other apps can query or 
modify the data if the content provider allows it. For example, the Android system provides a content provider that manages 
the user's contact information. Therefore, any app with the proper permissions can query the content provider, such as `ContactsContract.Data`, 
to read and write information about a particular person. 

To the system, a content provider is an entry point into an app for publishing named data items, identified by a URI scheme. 
So an app can decide how it wants to map the data it contains to a URI namespace, handing out those URIs to other entities 
which can in turn use them to access the data. There are a few things this allows the system to do in managing an app:
* Assigning a URI doesn't require that the app remain running, so URI's can persists after their owning apps have exited.
* Use URI's to provide an important security model.  
Content providers are also useful for reading and writing data that is private to your app and not shared.

A content provider is implemented as a subclass of `ContentProvider` an dmust implement a standard set of APIs that enable other 
apps to perform transactions. 
 
  

  



### Reading Links
[Application Fundamentals](https://developer.android.com/guide/components/fundamentals ) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 