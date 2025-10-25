# My API Code Examples

**Author:** Lauren March

## cURL example

A GET request to get a list of breads from the database.

### cURL command

```shell
curl http://localhost:3000/breads
```

### cURL response

```shell
[
  {
    "type": "sourdough",
    "scoring": true,
    "sweet": false,
    "id": 1
  },
  {
    "type": "cinnamon-raisin",
    "scoring": false,
    "sweet": true,
    "id": 2
  }
]
```

## Postman example

A GET request, get a pastry with ID = 1.

### Request

**Method**: `GET`

```shell
http://localhost:3000/pastries/1
```

### Postman response

```shell
{
    "type": "short crust",
    "use": [
        "Pie",
        "Quiche",
        "Tart"
    ],
    "id": 1
}
```
