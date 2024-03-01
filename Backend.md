# Backend Documentation 🖥️

This document provides a concise overview of key files and functions used in the backend of the project.

## Key Files 📁

### 1. `server.js`

- **Description**: Entry point of the backend application.
- **Usage**: Initializes and configures the server.

### 2. `routes.js`

- **Description**: Manages API routes and their corresponding handlers.
- **Usage**: Defines routes for user data and post creation.

### 3. `database.js`

- **Description**: Handles database connections and queries.
- **Usage**: Establishes a connection to the MySQL database.

### 4. `middlewares.js`

- **Description**: Contains middleware functions for request handling.
- **Usage**: Implements functions like authentication middleware.

### 5. `controllers.js`

- **Description**: Implements business logic for handling user and post data.
- **Usage**: Contains functions called by route handlers.

## Key Functions 🚀

### 1. `getUserById(userId)`

- **Description**: Retrieves user data based on the provided user ID.
- **Usage**: Used in various routes for fetching user details.

### 2. `createPost(postData)`

- **Description**: Creates a new post with the provided data.
- **Usage**: Called when a user submits a new post.

### 3. `authenticateUser(token)`

- **Description**: Verifies the authenticity of a user based on the provided token.
- **Usage**: Middleware function for route authentication.

### 4. `updateUserDetails(userId, updatedData)`

- **Description**: Updates user details based on the provided user ID and new data.
- **Usage**: Used in routes for handling user profile updates.

### 5. `deletePost(postId)`

- **Description**: Deletes a post based on the provided post ID.
- **Usage**: Called when a user chooses to delete a post.

### 6. `handleError(error)`

- **Description**: Centralized function to handle errors in the backend.
- **Usage**: Utilized across the application to manage error responses.

This documentation provides a quick reference for key files and functions in the backend of the project. For more detailed information, refer to the individual files and their inline comments.
