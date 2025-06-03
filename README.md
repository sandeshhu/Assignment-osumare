# Assignment-osumare
This is task of osumare 


backend work here
how task api work, purpose, dependencies 
# Task API

simple RESTful API for managing a collection of tasks built with Node.js and Express.js. The API supports basic CRUD operations and stores data in memory.

## Table of Contents

- [Installation](#installation)
- [API Endpoints](#api-endpoints)
- [Sample Requests](#sample-requests)
- [Running the API Locally](#running-the-api-locally)
- [Error Handling](#error-handling)
- [Bonus Features](#bonus-features)

## Installation

1. Clone the repository:
   ```
   git clone <repository-url>
   cd task-api
   ```

2. Install the dependencies:
   ```
   npm install
   ```

## API Endpoints

### GET /tasks
Retrieve a list of all tasks.

**Response:**
- Status: 200 OK
- Body: Array of task objects

### GET /tasks/:id  (id=1)
Retrieve a specific task by ID.

**Response:**
- Status: 200 OK
- Body: Task object

**Error Response:**
- Status: 404 Not Found

### POST /tasks
Create a new task.

**Request Body:**
```json
{
  "title": "Task Title",
  "description": "Task Description"
}
```

**Response:**
- Status: 201 Created
- Body: Created task object

**Error Response:**
- Status: 400 Bad Request

### PUT /tasks/:id
Update an existing task by ID.

**Request Body:**
```json
{
  "title": "Updated Task Title",
  "description": "Updated Task Description"
}
```

**Response:**
- Status: 200 OK
- Body: Updated task object

**Error Response:**
- Status: 404 Not Found
- Status: 400 Bad Request

### DELETE /tasks/:id
Delete a task by ID.

**Response:**
- Status: 204 No Content

**Error Response:**
- Status: 404 Not Found

## Sample Requests

You can test the API using tools like Postman or curl. Here are some sample requests:

1. **Get all tasks:**
   ```
   GET /tasks
   ```

2. **Create a new task:**
   ```
   POST /tasks
   Content-Type: application/json

   {
     "title": "New Task",
     "description": "This is a new task."
   }
   ```

3. **Update a task:**
   ```
   PUT /tasks/1
   Content-Type: application/json

   {
     "title": "Updated Task",
     "description": "This task has been updated."
   }
   ```

4. **Delete a task:**
   ```
   DELETE /tasks/1
   ```

## Running the API Locally

To run the API locally, use the following command:

```
npm start
```

The API will be available at `http://localhost:3000`.

## Error Handling

The API includes basic error handling to manage unexpected issues and return appropriate status codes.

## Bonus Features

- Pagination for the GET /tasks endpoint.
- Sorting and filtering options for task retrieval.
- Authentication and authorization mechanisms for protecting certain endpoints.
