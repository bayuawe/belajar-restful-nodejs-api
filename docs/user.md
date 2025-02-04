# User API Spec

## Register User API

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "bayuawe",
  "password": "rahasia",
  "name": "Bayu Aryandi Wijaya"
}
```

Request Body Success :

```json
{
  data : {
    "username" : "bayuawe",
    "name" : "Bayu Aryandi Wijaya"
  } 
}
```

Request Body Errors :

```json
{
  "errors" : "Username already registered"
}
```

## Login User API

Endpoint : POST /api/users/login

Request Body :

```json
{
  "username" : "pzn",
  "password" : "rahasia"
}
```

Response Body Success 👍

```json
{
  "data" : {
    "token" : "unique-token",
   }
}
```

Response Body Errors 👎

```json
{
  "errors" : "username or password wrong"
}

```

## Update User API

Endpoint : PATCH /api/users/current

Headers :

* [X]  Authorization : Token

Requset Body :

```json
{
  "name" : "Bayu Aryandi Wijaya Lagi", //optional 
  "password" : "new password" //optional
}
```

Response Body Success 👍

```json
{
  "data" : {
    "username" : "bayuawe",
    "name" : "Bayu Aryandi Wijaya Lagi"
  }
}
```

Response Body Error 👎

```json
{
  "errors" : "name length max 100"
}
```

## Get User API

Endpoint : GET /api/users/current

Headers :

* [X]  Authorization : Token

Response Body Success 👍

```json
{
  "data" : {
    "username" : "bayuawe",
    "name" : "bayuawe"
  }
}
```

Response Body Error 👎

```json
{
  "errors" : "unauthorized"
}
```

## Logout User API

Endpoint : DELETE /api/users/logout

Headers :

* [X]  Authorization : Token

Response Body Success 👍

```json
{
  "data" : "OK"
}
```

Response Body Error 👎

```json
{
  "errors" : "unauthorized"
}
```
