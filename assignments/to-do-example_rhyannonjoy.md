# Examples

**Author:** Rhyannon Rodriguez

## cURL

Get user 1 with cURL.

### Command

```shell
curl http://localhost:3000/users/1
```

### cURL response

```shell
{
  "lastName": "Smith",
  "firstName": "Ferdinand",
  "email": "f.smith@example.com",
  "id": 1
}
```

## Postman example

Get user 2 with Postman.

### Request

**Method**: GET

```shell
http://localhost:3000/users/2
```

### Postman response

```shell
{
    "lastName": "Jones",
    "firstName": "Jill",
    "email": "j.jones@example.com",
    "id": 2
}
```
