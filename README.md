# certifyme

Spring security principal using JWT

In next 15 min, we will learn how to handle authentication and authorization on RESTful Service APIs written with Spring Boot. We will create a simple Spring Boot application that exposes public endpoints, and then we will secure these endpoints with Spring Security and JWT.

JWTs
What is JWT ? 

JSON Web Tokens, commonly known as JWTs, are tokens(String) that are used to authenticate users on applications. This technology has gained popularity over the past few years because it enables backends to accept requests simply by validating the contents of these JWTS. That is, applications that use JWTS no longer have to hold cookies or other session data about their users. This characteristic facilitates scalability while keeping applications secure.

During the authentication process, when a user successfully logs in using their credentials (userid & password), a JSON Web Token is returned and must be saved locally (either in local storage). Whenever the user wants to access a protected route or resource (an endpoint), the user agent must send the JWT, usually in the Authorization header using the Bearer schema, along with the request.

When a backend server receives a request with a JWT, the first thing to do is to validate the token. This consists of a series of steps, and if any of these fails then, the request must be rejected. The following list shows the validation steps needed:

Check that the JWT is well formed
Check the signature
Validate the standard claims
Check the Client permissions (scopes)
The RESTful Spring Boot API Overview
The RESTful Spring Boot API that we are going to secure is a task list manager. The task list is kept globally, which means that all users will see and interact with the same list.

detailed explanation is available on https://youtu.be/4veRFsH7MyI
https://jaykrs.blogspot.com/p/spring-security-with-jwt.html
