# User API Spec

## Register User API

Endpoint : POST /api/users

Request Body :

```json
{
    "username" : "Leonardo",
    "password" : "Rahasia",
    "name" : "Leo"
}
```

Response Body Success : 

```json
{
    "data" : {
        "username" : "Leonardo",
        "name" : "Leo"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Username Already Registered"
}
```

## Login User API

Endpoint : POST /api/users/login

Request Body :

```json
{
    "username" : "Leonardo",
    "password" : "Rahasia",
}
```

Response Body Success : 

```json
{
    "data" : {
        "token" : "unique-token"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Username or Password Wrong"
}
```

## Update User API

Endpoint : PATCH /api/users/current

Headers :
- Authorization : token

Request Body :

```json
{
    "name" : "Programer Zaman Now Lagi",
    "password" : "New Password",
}
```

Response Body Success : 

```json
{
    "data" : {
        "username" : "Leonardo",
        "name" : "Leo"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Name Length Max 100"
}
```

## Get User API

Endpoint : GET /api/users/current

Headers :
- Authorization : token

Response Body Success : 

```json
{
    "data" : {
        "username" : "Leonardo",
        "name" : "Leo"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Unauthorized"
}
```

## Logout User API

Endpoint : DELETE /api/users/Logout

Headers :
- Authorization : token

Response Body Success : 

```json
{
    "data" : "OK"
}
```

Response Body Error :

```json
{
    "errors" : "Unauthorized"
}
```
