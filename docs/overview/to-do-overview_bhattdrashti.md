# To-Do Service API Overview

> **The easiest way to build and test a task management API.**

The **To-Do Service API** helps developers create, view, and manage to-do lists in the cloud.  
It’s a simple, REST-based service designed to help you build apps that track tasks, set reminders, and stay productive.

---

## Why use the To-Do Service API?

Whether you’re prototyping a productivity app or learning how REST APIs work, the To-Do Service provides an easy way to:

- **Create and manage tasks** with titles, due dates, and completion status.  
- **Store data** in a lightweight, mock cloud environment.  
- **Experiment safely** without setting up a real database or backend.  

Built for beginners and technical writers alike, this service demonstrates how a REST interface works in practice.

---

## Quickstart

Ready to try it?

- [Set up your environment](../before-you-start-a-tutorial.md)  
- [Add your first task](../tutorials/add-a-new-task.md)  
- [Enroll a new user](../tutorials/enroll-a-new-user.md)  


Each tutorial walks you through a common use case using **cURL** or **Postman**.

---

## API at a glance

**Base URL (local testing):** http://localhost:3000


### Available resources

| Resource | Description |
|-----------|--------------|
| `/users` | Represents registered users of the To-Do Service. |
| `/tasks` | Represents individual to-do items created by users. |

### Supported methods
Each resource supports standard HTTP methods:
- `GET` – Retrieve data  
- `POST` – Create new items  
- `PUT` – Update existing items  
- `DELETE` – Remove items  


