# Code examples

**Author:** Mary Grace Venuto

## cURL example

This is an example of how to GET a task by task ID.

### cURL command

```JSON
curl http://localhost:3000/tasks/1
```

### cURL response

```JSON
[
  {
    "userId": 1,
    "title": "Grocery shopping",
    "description": "eggs, bacon, gummy bears",
    "dueDate": "2025-09-20T17:00",
    "warning": "10",
    "id": 1
  }
]
```

## Postman example

This example shows how to return a task by task ID using Postman.

### Request

**Method**:

```JSON
GET http://localhost:3000/tasks/1
```

### Postman response

```JSON
{
    "userId": 1,
    "title": "Grocery shopping",
    "description": "eggs, bacon, gummy bears",
    "dueDate": "2025-09-20T17:00",
    "warning": "10",
    "id": 1
}
```
