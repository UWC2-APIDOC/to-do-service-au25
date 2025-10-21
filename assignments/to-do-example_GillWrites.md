# Code examples

**Author:** \<Gill Deenihan\>

## cURL example

Get request for User 2

### cURL command

```shell
curl http://localhost:3000/Users/2

```

### cURL response

```shell
{
  "lastName": "Jones",
  "firstName": "Jill",
  "email": "j.jones@example.com",
  "id": 2
```

## Postman example

Add a new user

### Request

**Method**: post

```shell
{
  "lastName": "Deenihan",
  "firstName": "Gill",
  "email": "gdeenihan5@gmail.com"
   "id": 8
}
```

### Postman response

```shell
{
    "lastName": "Deenihan",
    "firstName": "Gill",
    "email": "gdeenihan5@gmail.com",
    "id": 8
}
```
