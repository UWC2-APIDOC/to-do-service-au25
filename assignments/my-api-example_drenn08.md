# Code examples

**Author:** David Renn

## cURL example

The cURL example provided in the Assignment 5.3 demo.
A resource instance and accompanying properties of a player listed in the phillies_roster resource.

### cURL command

```shell
curl http://localhost:3000/users/3
curl http://localhost:3000/phillies_roster/1
```

### cURL response

```shell
{
  "lastName": "Martinez",
  "firstName": "Marty",
  "email": "m.martinez@example.com",
  "id": 3
}
```json
{
  "Player Name": "Bryce Harper",
  "Position": "First Base",
  "Hits": "Left-handed",
  "Throws": "Right-handed",
  "id": 1
```

## Postman example

The Postman example provided in the Assignment 5.3 demo.
A resouce instance and accompanying properties of a hiking trail listed
in the chester_county_hiking_trails resource.

### Request

**Method**:

```shell
GET http://localhost:3000/tasks/3
GET http://localhost:3000/chester_county_hiking_trails/1
```

### Postman response

```shell
{
    "userId": 2,
    "title": "Oil change",
    "description": "5K auto service",
    "dueDate": "2025-11-10T09:00",
    "warning": "60",
    "id": 3
```json
{
    "Trail Name": "Hickory and Cattail Loop",
    "Type": "loop",
    "Length": "1.3 miles",
    "Elevation Gain": "68 feet",
    "Difficulty": "easy",
    "id": 1
}
```
