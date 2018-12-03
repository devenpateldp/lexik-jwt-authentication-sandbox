LexikJWTAuthenticationBundle Sandbox
=====================================

This is a sample application for experimenting/demonstrating features of the powerful LexikJWTAuthenticationBundle bundle which provides authentication through JWT.

What's inside
--------------

- [Symfony](https://github.com/symfony/symfony) ~3.1
- [LexikJWTAuthenticationBundle](https://github.com/lexik/LexikJWTAuthenticationBundle) ~2.0

Get started
------------

Clone the project:
```sh
$ git clone https://github.com/chalasr/lexik-jwt-authentication-sandbox
$ cd lexik-jwt-authentication-sandbox
$ git checkout symfony-3.4
```


Usage
------

Run the web server:
```sh
$ php bin/console server:run 0.0.0.0:8080
```


Get a JWT token:


```
curl -X POST -H "Content-Type: application/json" http://localhost:8080/api/login_check -d '{"username":"admin","password":"password"}'
-> { "token": "[TOKEN]" }  
```

Access a secured route:
```
$ curl -H "Authorization: Bearer [TOKEN]" http://localhost:8000/api
-> Logged in as admin
```
