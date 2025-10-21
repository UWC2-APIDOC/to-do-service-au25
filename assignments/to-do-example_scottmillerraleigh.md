# Code examples

**Author:** Scott Miller

## cURL example

to get a specific user

### cURL command

```shell
curl http://localhost:3000/users/1/
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

to get a specific task

### Request

**Method**:

```shell
GET http://localhost:3000/tasks/4
```

### Postman response

```shell
{
    "userId": 3,
    "title": "Get shots for dog",
    "description": "Annual vaccinations for poochy",
    "dueDate": "2025-12-11T14:00",
    "warning": "20",
    "id": 4
}
```
