# Code examples

**Author:** Lauren March

## cURL example

A GET request to get a list of breads from the database.

### cURL command

```shell
C:\Users\psycl>curl http://localhost:3000/breads
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

\<replace with a description of the example\>

### Request

**Method**: GET

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
