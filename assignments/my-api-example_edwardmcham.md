# Code examples

**Author:** Edward McHam

## cURL example

Get all the cats.

### cURL command

```shell
curl http://localhost:3000/cats
```

### cURL response

```shell
[
  {
    "Breed": "Himalyan",
    "Hunts": "indoor",
    "Hair": "long",
    "Color": "cream",
    "id": 1
  }
]
```

## Postman example

Get all the dogs.

### Request

**Method**:

```shell
curl --location 'http://localhost:3000/dogs'
```

### Postman response

```shell
[
    {
        "Breed": "Pomeranian",
        "Color": "golden-brown",
        "Hair": "short",
        "Roams": "indoor",
        "id": 1
    }
]
```
