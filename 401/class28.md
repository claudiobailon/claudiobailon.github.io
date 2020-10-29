# Amplify and Cognito

## Overview
The Amplify Auth category provides an interface for authenticating a user. Behind the scenes, 
it provides the necessary authorization to the other Amplify categories. It comes with default, 
build-in support for Amazon Cognito User Pool and Identity Pool. The Amplify CLI helps you to 
create and configure the auth category with an authentication provider. 

## Configure Auth Category
To start provisioning auth resources in the backend, go to your project directory and run the 
following command:
```
amplify add auth
```
Then enter the following when prompted:
```
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`
```
 To push your changes to the cloud, run the `amplify push` command.
 
 When everything is done, `amplifyconfiguration.json` should be updated to reference provisioned 
 backend auth resources. 
 
 ## Install Amplify Libraries
 Add the following dependency to your app's `build.gradle`:
 ```
dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.4.1'
}
```
## Initialize Amplify Auth
Add the Auth plugin in the Prerequisites section:
```
// Add this line, to include the Auth plugin.
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());
```

  



### Reading Links
[Amplify and Cognito](https://docs.amplify.aws/lib/auth/getting-started/q/platform/android) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 