# Address Api Specs

## Create Address API

Endpoint : POST /api/contacts/:contactId/addresses

Headers :

- Authorization : token

Request Body :

```json
{
  "street": "jalan apa",
  "city": "Kota apa",
  "province": "Provinsi apa",
  "country": "Negara apa",
  "postal_code": "Kode Pos"
}
```

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "street": "jalan apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal_code": "Kode Pos"
  }
}
```

Response Body Errors :

```json
{
  "errors": "Country is mandatory"
}
```

## Update Address API

Endpoint : PUT /api/contacts/:contacId/addresses/:addressId

Headers :

- Authorization : token

Request Body :

```json
{
  "street": "jalan apa",
  "city": "Kota apa",
  "province": "Provinsi apa",
  "country": "Negara apa",
  "postal_code": "Kode Pos"
}
```

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "street": "jalan apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal_code": "Kode Pos"
  }
}
```

Response Body Errors :

```json
{
  "errors": "Country is Required"
}
```

## Get Address API

Endpoint : GET /api/contacts/:contactId/addresses/:addressId

Headers :

- Authorization : token

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "street": "jalan apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal_code": "Kode Pos"
  }
}
```

Response Body Errors :
```json
{
  "errors" : "Contact is not found"
}
```

## List Address API

Endpoint : GET /api/contacts/:contactId/addresses

Headers :

- Authorization : token

Response Body Success : 
```json
{
  "data" : [
    {
      "id": 1,
      "street": "jalan apa",
      "city": "Kota apa",
      "province": "Provinsi apa",
      "country": "Negara apa",
      "postal_code": "Kode Pos"
    },
    {
      "id": 2,
      "street": "jalan apa",
      "city": "Kota apa",
      "province": "Provinsi apa",
      "country": "Negara apa",
      "postal_code": "Kode Pos"
    }
  ]
}
```

Response Body Errors : 
```json
{
  "errors" : "Contact is not found"
}
```

## Remove Address API

Endpoint : DELETE /api/contacts/:contactId/addresses/:addressId

Headers :

- Authorization : token

Response Body Success :
```json
{
  "data" : "OK"
}
```

Response Body Errors :****

```json
{
  "errors" : "Contact is not found"
}
```
