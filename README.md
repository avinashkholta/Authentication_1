Backend Authentication & User Management API



Overview
This project is a simple and secure authentication and user management API built using Node.js, Express.js, and MongoDB. It provides essential authentication features such as JWT-based login, user registration, and CRUD operations for managing user data. The API does not include any frontend or middleware, focusing solely on the backend logic for handling user authentication and data management.

Features
User Signup
Register a new user by providing a username, email, and password.

User Login with JWT Authentication
Authenticate a user by email and password, and generate a JWT token for subsequent requests.

User Logout
Logout the user by invalidating the session. (Note: In this example, JWT tokens are stateless, so logout is a simple action of not providing a token in future requests.)

CRUD Operations for User Management

Get user details: Retrieve a user's profile using their ID.
Update user details: Modify user data such as username and email.
Delete user: Permanently remove a user from the database.
How to Run the Project
Open the project folder in your preferred code editor (e.g., VS Code).

Open a terminal.

Navigate to the backend folder by running:

bash
Copy code
cd backend
Install dependencies by running:

bash
Copy code
npm install
Start the server:

bash
Copy code
npm run start
This will start the API server on the port defined in the .env file (default is port 5000).

Testing the APIs:
Use Thunder Client, Postman, or any API testing tool to interact with the following endpoints.

API Endpoints
Authentication
POST /signup

Registers a new user.
Request body:
json
Copy code
{
  "username": "john_doe",
  "email": "john@example.com",
  "password": "password123"
}
POST /login

Authenticates the user and returns a JWT token.
Request body:
json
Copy code
{
  "email": "john@example.com",
  "password": "password123"
}
GET /logout

Logs out the user (JWT token invalidation is managed client-side).
User Management
GET /user/:id

Retrieve the user details by their unique ID.
PUT /user/:id

Update user details (username, email, etc.).
Request body:
json
Copy code
{
  "username": "john_updated",
  "email": "john_updated@example.com"
}
DELETE /user/:id

Delete a user permanently from the database.
