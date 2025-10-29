---
# markdownlint-disable
# vale  off
layout: default
parent: task resource
nav_order: 2
# tags used by AI files
description: GET the `task` resource with the specified ID from the service
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites:
    - /api/user
related_pages: []
examples: []
api_endpoints:
    - GET /users
version: "v1.0"
last_updated: "2025-10-27"
# vale  on
# markdownlint-enable
---

# Get a task by ID

Returns a JSON object containing details of a single `task` object specified by the `id` parameter.

## URL

```shell

{server_url}/tasks/{id}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the task to return |

## Request headers

None

## Request body

None

## Return body

```json
[
{
        "userId": 1,
        "title": "Piano recital",
        "description": "Daughter's first concert appearance",
        "dueDate": "2025-10-02T15:00",
        "warning": "30",
        "id": 2
    },
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Properties returned

Each `GET /tasks/{id}` call returns a task object that includes the following properties:

| Property      | Type      | Description   |
| ------------  | -------   | ------------- |
| `userid`      | int       | Unique identifier of the user associated with the task. |
| `title`       | string    | The title of the task. |
| `description` | string    | The description of the task |
| `dueDate`     | date-time | The timestamp of when the task is due to be completed. |
| `warning`     | string    | A warning notification set to a specific time (i.e. 30 minutes before a task is due)|
| `id`          | int       | Unique identifier of the task. |

## Example

This example is using the `GET` method to call a task with an ID of 3.

### Request

```shell
GET http://localhost:3000/tasks/3
```

### Response

```json
[   
    {
        "userId": 2,
        "title": "Oil change",
        "description": "5K auto service",
        "dueDate": "2025-11-10T09:00",
        "warning": "60",
        "id": 3
    }   
]
```

## Related pages

[Task resource](task.md)
