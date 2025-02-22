## Contact API Specs

## Create Contact API

Endpoint : POST /api/contacts

Headers:

- Authorization : token

Request Body :

```json
{
        "firstName" : "Bayu",
        "lastName" : "Awe",
        "email" : "bayuawe@gmail.com",
        "phone" : "08123123123"
}
```

Response Body Success: 
```json
{
    "data" : {
        "id" : 1,
        "firstName" : "Bayu",
        "lastName" : "Awe",
        "email" : "bayuawe@gmail.com",
        "phone" : "08123123123"
    }
}
```

Response Body Error:
```json
{
    "errors" : "Email is not valid format"
}
```

## Update Contact API

Endpoint : PUT /api/contacts/:id

Headers:

- Authorization : token

Request Body :
```json
{
        "firstName" : "Bayu",
        "lastName" : "Awe",
        "email" : "bayuawe@gmail.com",
        "phone" : "08123123123"
}
```


Response Body Success:
```json
{
    "data" : {
        "id" : 1,
        "firstName" : "Bayu",
        "lastName" : "Awe",
        "email" : "bayuawe@gmail.com",
        "phone" : "08123123123"
    }
}
```

Response Body Error:
```json
{
    "errors" : "Email is not valid format"
}
```

## Get Contact API

Endpoint : GET /api/contacts/:id

Headers:

- Authorization : token

Response Body Success:
```json
{
    "data" : {
        "id" : 1,
        "firstName" : "Bayu",
        "lastName" : "Awe",
        "email" : "bayuawe@gmail.com",
        "phone" : "08123123123"
    }
}
```

Response Body Error:
```json
{
    "errors" : "Contact is Not found"
}
```

## Search Contact API

Endpoint : GET /api/contacts

Headers:

- Authorization : token

Query Params : 
- name : Search by firstName or lastName, using like, optional
- email : Search by email, using like, optional
- phone : Search by phone, using like, optional
- page : number of page, default 1
- size : size per page, default 10

Response Body Success:
```json
{
    "data" : [
    {
        "id" : 1,
        "firstName" : "Bayu",
        "lastName" : "Awe",
        "email" : "bayuawe@gmail.com",
        "phone" : "08123123123"
    },
    {
        "id" : 2,
        "firstName" : "Bumbum",
        "lastName" : "Xixi",
        "email" : "bayuawe@gmail.com",
        "phone" : "08123123123"
    }
    ],
    "paging" : {
        "page" : 1,
        "total_page" : 3,
        "total_item" : 30
    }
}
```

Response Body Error:

## Remove Contact API

Endpoint : DELETE /api/contacts/:id

Headers:

- Authorization : token

Response Body Success:

```json
{
    "data" : "OK"
}
```

Response Body Error:

```json
{
    "errors" : "Contact not found"
}
```
