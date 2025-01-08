# Bookstore-API
Book Store API that provides functionality for managing books and user interactions.


Build an API with Rate
Limiting, Caching, and RBAC

Scenario:
You are tasked to build a Book Store API that provides functionality for managing books
and user interactions.


1. Rate Limiting
Implement rate limiting to ensure that no user can make more than 10 requests per
minute to the API. The limit should apply per user (identified by a unique userId).
2. Caching
Add a caching mechanism to optimize performance.
○ Cache the responses for GET requests (e.g., fetching books).
○ Use an in-memory caching mechanism (e.g., Redis or any other preferred
library).
○ Set an expiration time of 60 seconds for cached data.
3. Role-Based Access Control (RBAC)
Implement RBAC to handle access control.
○ Roles: Admin and User.
○ Admin: Can perform all operations (create, update, delete books).
○ User: Can only view books (GET requests).
○ Protect endpoints using middleware or guards based on roles.
