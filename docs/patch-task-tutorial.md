# Tutorial: Updating a task with PATCH

Use the PATCH method to update specific fields on an existing task. 
PATCH is useful when you want to change part of a resource instead of replacing the entire task.

This tutorial should take about 5 minutes to complete.

## Description and goal

The following procedure show you how to update one or more fields on an
existing task using the `PATCH /tasks/{taskId}` endpoint.

## Prerequisites

* Complete the [Before you start a tutorial](before-you-start-a-tutorial.md)
topic on your development system. 

* The `to-do-db-source.json` service is running.

## Procedure: Updating the task

1. Open a terminal.

2. Run the `cURL` command using the PATCH method:
    ```bash
    curl -X PATCH http://localhost:3000/tasks/3 \
    -H "Content-Type: application/json" \
    -d '{
        "description": "5K auto service at new shop",
        "warning": 30
    }'
    ```
3. Confirm that the JSON response includes the updated fields.

## Completion and validation

1. Run the following query to confirm the changes:

    ```bash
    curl http://localhost:3000/tasks/3
    ```
    
    The system returns the changes:
    ```json
    "description": "5K auto service at new shop",
    "dueDate": "2025-11-10T09:00",
    "warning": 30,
    ```