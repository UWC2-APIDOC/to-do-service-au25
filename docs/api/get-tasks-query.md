# GET /tasks - Filter Tasks by Status

Retrieve tasks filtered by their completion status.

## Endpoint
```
GET /tasks?status={value}
```

## Description

Returns tasks that match the specified status filter. This endpoint allows you to retrieve only completed or incomplete tasks.

## Parameters

### Query Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `status` | string | No | Filter tasks by status. Accepts: `complete` or `incomplete` |

## Request Examples

### cURL - Get Completed Tasks
```bash
curl "http://localhost:3000/tasks?status=complete"
```

### cURL - Get Incomplete Tasks
```bash
curl "http://localhost:3000/tasks?status=incomplete"
```

## Response Format

### Success Response

**Status Code:** `200 OK`

**Content-Type:** `application/json`

## Response Examples

### Filter by Status: Complete

**Request:**
```bash
curl "http://localhost:3000/tasks?status=complete"
```

**Response:**
```json
[
  {
    "id": "2",
    "title": "Walk the dog",
    "status": "complete"
  }
]
```

### Filter by Status: Incomplete

**Request:**
```bash
curl "http://localhost:3000/tasks?status=incomplete"
```

**Response:**
```json
[
  {
    "id": "1",
    "title": "Grocery shopping",
    "status": "incomplete"
  },
  {
    "id": "3",
    "title": "Finish API documentation",
    "status": "incomplete"
  }
]
```

### No Filter (All Tasks)

**Request:**
```bash
curl "http://localhost:3000/tasks"
```

**Response:**
```json
[
  {
    "id": "1",
    "title": "Grocery shopping",
    "status": "incomplete"
  },
  {
    "id": "2",
    "title": "Walk the dog",
    "status": "complete"
  },
  {
    "id": "3",
    "title": "Finish API documentation",
    "status": "incomplete"
  }
]
```

## Notes

- The `status` parameter is optional. If omitted, all tasks are returned
- Valid values for `status` are: `complete` or `incomplete`
- The parameter is case-sensitive
- Invalid status values will return all tasks (no error)
- Results are returned as a JSON array

## Related Endpoints

- [GET /tasks](get-tasks.md) - Get all tasks
- [GET /tasks/{id}](get-task-by-id.md) - Get specific task by ID
- [POST /tasks](post-tasks.md) - Create a new task
- [PUT /tasks/{id}](put-tasks.md) - Update an existing task
- [DELETE /tasks/{id}](delete-tasks.md) - Delete a task