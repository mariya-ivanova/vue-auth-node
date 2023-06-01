# JSONServer + JWT Auth

A Fake REST API using json-server with JWT authentication. 

Implemented End-points: login,register

## Install

```bash
$ npm install
$ npm run start
```

Might need to run
```
npm audit fix
```

## How to login/register?

You can login/register by sending a POST request to

```
POST http://localhost:8000/auth/login
POST http://localhost:8000/auth/register
```
with the following data 

```
{
  "email": "testuser@testuser.com",
  "password":"testuser"
}
```

You should receive an access token with the following format 

```
{
   "access_token": "<ACCESS_TOKEN>"
}
```


You should send this authorization with any request to the protected endpoints

```
Authorization: Bearer <ACCESS_TOKEN>
```

This is simplified version of the Fake REST API server: 
https://github.com/techiediaries/fake-api-jwt-json-server
(The current siplified server contains only functionality for authentication, plus slight modification of the server in order to get the current updated verion of users on each request.)

