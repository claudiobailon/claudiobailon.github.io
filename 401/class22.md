# Intents, Activities, and SharedPreferences

## Tasks and the Back Stack
A task is a collection of activities that users interact with when performing
a certain job. The activities are arranged in a stack, the back stack,in the 
order in which each activity is opened. Example: an email app might have one 
activity to show a lists of new messages and when a user selects a message, a 
new activity opens to view that message. This new activity is added to the back 
stack. If the user presses the back button, that new activity is finished and 
popped off the back stack. 

When apps are running simultaneously in a multi-windowed environment, the system 
manages tasks separetely for each window, so each window may have multiple tasks.


 
  

  



### Reading Links
[Android Tasks and the Back Stack](https://developer.android.com/guide/components/activities/tasks-and-back-stack) <br>
[Android SharedPreferences](https://developer.android.com/training/data-storage/shared-preferences) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 