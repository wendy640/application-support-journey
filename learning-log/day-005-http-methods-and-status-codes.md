# Day 5: Understanding HTTP Methods and Status Codes

Today, I learned about HTTP methods and HTTP status codes—two essential concepts that define how clients communicate with servers.

## HTTP Methods

HTTP methods tell the server what action the client wants to perform.

### GET
Retrieves data from the server.

Example:
- View a user's profile.
- Fetch a list of products.

### POST
Creates a new resource on the server.

Example:
- Register a new user.
- Submit a contact form.

### PUT
Updates an entire resource.

Example:
- Replace all details of a user's profile.

### PATCH
Updates part of a resource.

Example:
- Change only a user's email address.

### DELETE
Removes a resource from the server.

Example:
- Delete a user account.

## HTTP Status Codes

Status codes indicate whether a request was successful or if an error occurred.

### 200 OK
The request was successful.

### 201 Created
A new resource was successfully created.

### 400 Bad Request
The request contains invalid data.

### 401 Unauthorized
Authentication is required or has failed.

### 403 Forbidden
The user is authenticated but does not have permission.

### 404 Not Found
The requested resource could not be found.

### 500 Internal Server Error
An unexpected error occurred on the server.

## Why This Matters for Application Support

As an Application Support Specialist, understanding HTTP methods and status codes makes troubleshooting much easier.

For example:
- A 404 error may indicate an incorrect URL.
- A 401 error may point to an authentication issue.
- A 500 error often requires investigation on the server side.

## Key Takeaway

HTTP methods tell the server **what to do**, while HTTP status codes tell us **how the request went**.

## Next Step

Learn how to test APIs using Postman.
