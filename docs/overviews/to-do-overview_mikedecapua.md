# To-Do Service API

## Manage cloud-hosted task lists with a simple REST interface

The To-Do Service API lets you create tasks, set due dates, and automate reminders through straightforward HTTP requests. Whether you're building a productivity app, integrating task management into your workflow, or learning API development, this service provides the tools you need.

This mock API simulates a production-ready service, making it ideal for learning API integration, testing client applications, or exploring REST principles.

## What you can do

- Manage users - Enroll new subscribers and manage user accounts
- Create and organize tasks - Post tasks with descriptions, due dates, and priorities
- Track progress - Update task status and modify details as work progresses
- Stay on schedule - Leverage automated reminders for upcoming deadlines

## Get started

New to the To-Do Service? Start here:

1. Quickstart - Post your first task and see the API in action. (coming soon)
2. Before you start a tutorial - Set up your development environment. (one-time setup)

## Learn by doing

Follow these hands-on tutorials to master common workflows:

- [Enroll a new user](tutorials/enroll-a-new-user.md)
- [Add a new task](tutorials/add-a-new-task.md)
- [Change the due-date of a task _(coming soon)_](#tutorials)
- [Delete a task _(coming soon)_](#tutorials)

## API reference docs

Explore detailed documentation for each resource:

- [User resource](api/user.md)
- [Task resource](api/task.md)

Base URL: When testing locally, the API runs at `http://localhost:3000`.

Note: The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.
