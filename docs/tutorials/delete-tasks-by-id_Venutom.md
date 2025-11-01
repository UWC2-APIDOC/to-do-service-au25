# Delete tasks by task ID

When a task is complete or no longer relevant, the To-Do API allows users to delete existing tasks by task ID. By the end of this tutorial, you will be able to delete a task by task ID using the Postman app.

Postman is an all-in-one API platform used by developers to build, test, and manage APIs. It has been chosen for this tutorial due to its user-friendly interface.

## Before you begin

You can only delete a task from an existing task list. If you need to create a task list first, see the [add a new task](https://uwc2-apidoc.github.io/to-do-service-au25/tutorials/add-a-new-task/) tutorial.

## How to delete a task

Step 1: Start the local service by running the following command:

```shell
     cd <your-github-workspace>/to-do-service/api
     json-server -w to-do-db-source.json
```

Step 2: Open the Postman app on the desktop.

Step 3: In the Postman app, go to the command line and press the down arrow on the dropdown menu of methods.

Step 4: Select `DELETE`

Step 5: Insert URL {{base_url}}/tasks followed by the task ID you intend to delete.

Example:

```shell
    http://localhost:3000/tasks/2
```

Step 6: Select send to submit the request.

## Verification

To verify that the task has been deleted, the response body should return an empty JSON object.

```JSON
JSON
    {}
```

## Learn more

Additional tutorials can be found in the To-Do API [repository](https://github.com/Venutom/to-do-service-au25/tree/main/docs/tutorials).
