---
# markdownlint-disable
# vale  off
layout: default
nav_order: 3
parent: Tutorials
# tags used by AI files
description: Update a `task` resource in the service
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites:
    - /before-you-start-a-tutorial
    - /api/user
    - /api/task
related_pages: []
examples: []
api_endpoints:
    - GET /tasks
    - GET /tasks/{taskId}
    - PUT /tasks
version: "v1.0"
last_updated: "2025-10-25"
# vale  on
# markdownlint-enable
---

# Tutorial: Update a task

In this tutorial, you learn to update an existing task.
It takes about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md) first.
This way, the system is ready and you can get started with the service right away.

## Update a task

Updating an existing task in the service requires the `PUT` method.
This overwrites the existing [`task`](../api/task.md) details.

### Update a task in Postman

To update a task in Postman:

1. Make sure your local service is running, or start it by using this command in your terminal.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

2. Open the Postman app on your desktop.
3. If you already know the ID of the task you wish to update, skip this step.
If you do not, start with a GET request in Postman to see all existing tasks:
    * **METHOD**: GET
    * **URL**: `{base_url}/tasks`
        > **_Note:_** Here, `{base_url}` is `http://localhost:3000`.

    The expected output for each task looks like the following.
    Note that the **task ID** is the **last element**.:

    ```js
    {
      "userId": 1,
      "title": "Piano recital",
      "description": "Daughter's first concert appearance",
      "dueDate": "2025-10-02T15:00",
      "warning": "30",
      "id": 2
    }
    ```

4. To update a chosen task in Postman, create a new request with the values shown below.
Make sure to substitute `taskId` for the ID of your chosen task with no curly brackets around the number.
    * **METHOD**: PUT
    * **URL**: `{base_url}/tasks/{taskId}`
    * **Request body**:
        You can change the values of each property as you'd like.
        For example, changing only the `userId` would assign the original task of recital to a new person.
        As it stands now, this person would miss out on the piano recital and get soda instead.

        ```js
        {
          "userId": 1,
          "title": "Buy cherry cola",
          "description": "Buy cherry cola while it's on discount.",
          "dueDate": "2025-10-02T15:00",
          "warning": "30",
          "id": 2
        }
        ```

5. In the Postman app, choose **Send** to make the request.
6. Take a look at the response body.
It should be identical to your request body.
7. If the response body was identical to the request body, this step is **not** necessary.
   You updated the task.
But if you are a person who likes to double-check everything, you can repeat step number 3.
You can also run the GET request but with `{base_url}/tasks/{taskId}`.
This request only shows you the updated task.

### Update a task in the terminal

If you prefer to use the terminal instead, you can send the same request with the `curl` command.
Writing a request body is a bit more complicated, but the logic is the same.

1. Make sure your local service is running, or start it by using this command in your terminal.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

2. Open another terminal window since the first one is busy running json-server.
3. If you already know the ID of the task you wish to update, skip this step.
If you do not, start with requesting all existing tasks.
Similarly to Postman, you are running a **GET** call on the `tasks` resource.
Thus, the whole request would look like this:

   ```shell
   curl http://localhost:3000/tasks
   ```

    The expected output for each task looks like the following.
    Note that the **task ID** is the **last element**:

    ```js
    {
      "userId": 1,
      "title": "Piano recital",
      "description": "Daughter's first concert appearance",
      "dueDate": "2025-10-02T15:00",
      "warning": "30",
      "id": 2
    }
    ```

4. To update a task, you use a **PUT** request.
When doing it in a terminal window, you add the request body right away.
This is the same cola example from Postman, but in a terminal:

   ```shell
   curl -X PUT http://localhost:3000/tasks/2 \
   -H "Content-Type: application/json" \
   -d "{
     \"userId\": 1,
     \"title\": \"Buy cherry cola\",
     \"description\": \"Buy cherry cola while it's on discount.\",
     \"dueDate\": \"2025-10-02T15:00\",
     \"warning\": \"30\",
     \"id\": 2
   }"
   ```

   To break it down:
   * Backslashes are just for readability - to break a long command into separate lines.
   * `-X PUT` followed by an endpoint tells curl which HTTP method to use.
   * `-H` specifies the header. This is different from how Postman does it.
   * `-d "{...}"` defines the body data.
   * Backslashes in the request body escape double quotes.
   Otherwise, the shell would interpret double quotes as part of code.
5. Take a look at the output to make sure that all the fields are correct.
If so, your request was successful.
