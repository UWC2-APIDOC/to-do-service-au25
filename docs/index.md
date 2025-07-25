---
# markdownlint-disable
# vale  off
layout: default
nav_order: 1
# tags used by AI files
description: Describes the To-Do Service for a new user
tags: 
    - introduction
categories: 
    - tutorial
ai_relevance: high
importance: 9
prerequisites: []
related_pages: 
    - /before-you-start-a-tutorial 
    - /tutorials/add-a-new-task
    - /tutorials/enroll-a-new-user
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2025-09-03"
# vale  on
# markdownlint-enable
---

# To-Do Service API

This is a mock API to simulate the REST interface of an
imaginary service.

The To-Do Service provides a cloud-hosted task list through which
subscribers can post tasks and receive reminders of those tasks.

## Quickstart

[Post your first task _(coming soon)_](#quickstart) with the To-Do Service to see how easy it is to use!

## Tutorials

Learn how to do common tasks with in the To-Do Service.

First, do this tutorial to set up your development system for these tutorials.
You only have to do this one time per development system.

* [Before you start a tutorial](before-you-start-a-tutorial.md)

After your system is ready, these tutorials show you how to perform common tasks.

* [Enroll a new user](tutorials/enroll-a-new-user.md)
* [Add a new task](tutorials/add-a-new-task.md)
* [Change the due-date of a task _(coming soon)_](#tutorials)
* [Delete a task _(coming soon)_](#tutorials)

## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When run locally for testing, the `{base_url}` is
generally `http://localhost:3000`.

* [user resource](api/user.md)
* [task resource](api/task.md)
