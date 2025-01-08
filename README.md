# Bookstore-API
Book Store API that provides functionality for managing books and user interactions.

Book Store API with Rate Limiting, Caching, and RBAC
Project Overview
This project implements a Book Store API featuring:

Rate Limiting: Limits users to 10 requests per minute.
Caching: In-memory caching for GET requests with a 60-second expiration.
Role-Based Access Control (RBAC): Controls access based on user roles (Admin and User).
API Structure
Endpoint	Method	Access	Description
/books	POST	Admin	Create a new book
/books	GET	Admin, User	Fetch all books
/books/:id	PUT	Admin	Update a book by ID
/books/:id	DELETE	Admin	Delete a book by ID
Technologies Used
Backend Framework: Node.js/NestJS
Caching: Redis (in-memory cache)
Rate Limiting: express-rate-limit
Authentication: Mock Authentication using custom HTTP headers
Authentication Implementation Details
Header-Based Authentication
The API uses a simplified mock authentication system through custom HTTP headers:

x-user-id: [unique user identifier]
x-role: [admin|user]
Example Request Headers
Admin Request Headers:

{
  "x-user-id": "admin123",
  "x-role": "admin"
