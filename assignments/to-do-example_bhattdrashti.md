# Code examples

**Author:** Drashti Bhatt

## cURL example

This example demonstrates how to **create a new to-do item** in the To-Do Service using cURL.


### cURL command

```shell
curl -X POST http://localhost:3000/tasks \
     -H "Content-Type: application/json" \
     -d '{"title": "Read a book", "completed": false}'

```

### cURL response

```shell
{
  "id": "a2c3",
  "title": "Read a book",
  "completed": false
}
```

## Postman example

This example demonstrates how to create a new to-do item in the To-Do Service using Postman.

### Request

**Method**:

```shell
curl -X POST http://localhost:3000/tasks \
     -H "Content-Type: application/json" \
     -d '{"title": "Read a book", "completed": false}'

```

### Postman response

```shell
{
  "id": "048c",
  "title": "Read a book",
  "completed": false
}
```
