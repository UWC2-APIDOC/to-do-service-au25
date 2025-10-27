# GET /users/{userId}

Retrieves a single user by their unique identifier.

## Endpoint

`GET /users/{userId}`

## Description

Use this operation to fetch details for a specific user. This is useful when displaying a profile or managing user-specific data.

## Path parameters

| Parameter | Type | Required | Description |
|----------|------|----------|-------------|
| `userId` | integer | Yes | Unique identifier for the user. |

## Response properties

| Property | Type | Description |
|---------|------|-------------|
| `firstName` | string | The user’s given name. |
| `lastName` | string | The user’s last name. |
| `email` | string | Contact email for the user. |
| `id` | integer | Unique identifier for the user. |

## Example request

```shell
curl http://localhost:3000/users/2
```

## Example response

```json
{
  "lastName": "Jones",
  "firstName": "Jill",
  "email": "j.jones@example.com",
  "id": 2
}
```

## Related operations

* [`task` resource](/docs/api/task.md)
* [`user` resource](/docs/api/user.md)