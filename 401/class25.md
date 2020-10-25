# Espresso

## Overview
Espresso is used to write concise, beautiful, and reliable Android UI tests.
The core API is small, predictable, and easy to learn, yet remains open for customization.
Espresso tests state expectations, interactions, and assertions clearly without the 
distraction of boilerplate content, custom infrastructure, or messy implementation details 
getting in the way.  
### Synchronization Capabilities
Each time your test invokes onView(), Espresso waits to perform the corresponding UI 
action or assertion until the following synchronization conditions are met:<br>
* The message queue is empty
* There are no instances of AsyncTask currently executing a task.
* All developer-defined idling resources are idle.

By performing these checks, Espresso substantially increases the likelihood that only
one UI action or assrtion can occur at any given time. This capability gives you more 
reliable and dependavle test results.  

### Espresso Test Recorder
The Espresso Test Recorder tool lets you create UI tests for your app without writing 
any test code. By recording a test scenario, you can record your interactions with a 
device and add assertions to verify UI elements in particular snapshots of your app. 
Espresso Test Recorder then takes the saved recording and automatically generates a 
corresponding UI test that you can run to test your app.

Espresso Test Recorder writes tests based on the Espresso Testing framework, an API in 
AndroidX Test. The espresso API encourages you to create concise and reliable UI tests 
based on user actions. By stating expectations, interactions, and assertions without 
directly accessing the underlying app's activities and views, this structure prevents 
test flakiness and ptimized test run speed. 
 
  

  



### Reading Links
[Espresso Testing](https://developer.android.com/training/testing/espresso) <br>
[Ridiculous superpower: the Espresso Test Recorder](https://developer.android.com/studio/test/espresso-test-recorder) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 