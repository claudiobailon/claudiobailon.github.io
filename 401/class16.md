# Spring Authentication

## Spring Authentication Cheat Sheet
### Step 1: Set up a user model and repo<br>
### Step 2: Create a controller for that model<br>
### Step 3: UserDetailsServiceImpl implements UserDetailsService<br>
Gets a user from the database by username (make sure your repository has the method to make this easy!)

### Step 4: ApplicationUser implements UserDetails<br>
Use IntelliJ to implement the methods; make the boolean ones all return true

### Step 5: WebSecurityConfig extends WebSecurityConfigurerAdapter<br>
Has a UserDetailsService<br>
PasswordEncoder bean<br>
Configure AuthManagerBuilder:<br>
`auth.userDetailsService(userDetailsService).passwordEncoder(passwordEncoder());`<br>
Configure HttpSecurity:<br>
cors? csrf?<br>
Matchers for URLs that are allowed<br>
Ensure that login and signup URLs allowed; also consider homepage etc.<br>
formLogin with login page set up<br>
logout<br>
  `  @Override`<br>
    `@Bean`<br>
    `public AuthenticationManager authenticationManagerBean() throws Exception {
        return super.authenticationManagerBean();
    }`<br>
### Step 6: Registration page<br>
Create it with form<br>
Ensure it posts to a route your controller is ready for<br>
Check it's saving in the DB<br>
   `Authentication authentication = new UsernamePasswordAuthenticationToken(newUser, null, new ArrayList<>());`<br>
    `SecurityContextHolder.getContext().setAuthentication(authentication);`
### Step 7: Login page<br>
Create it with a form<br>
Ensure it posts to the route you specified in web config<br>
Try it out!<br>
Add to a template w/ things about the Principal<br>
 
  


### Reading Links
[Spring Security Overview](https://spring.io/guides/topicals/spring-security-architecture/) <br>
[Spring Authentication Cheatsheet](https://github.com/codefellows/seattle-java-401d2/blob/master/SpringAuthCheatSheet.md) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 