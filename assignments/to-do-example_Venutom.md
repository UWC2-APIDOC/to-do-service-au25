# Code examples

**Author:** Mary Grace Venuto

## cURL example

This is an example of how to GET a comment.

### cURL command

```$ 
curl http://localhost:3000/comments
```

### cURL response

```
{
    "id": 1,
    "body": "some comment",
    "postId": 1
  }
```

## Postman example

This is how to get a comment.

### Request

**Method**:

```shell
GET http://localhost:3000/comments
```

### Postman response

```
{
"id": 1,
"body": "some comment",
"postId": 1
}
```
