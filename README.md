# Book-store
Online Book store API Documentation

Online Bookstore RESTful API Documentation
Version: 1.0
Base URL: https://api.onlinebookstore.com/v1
Format: JSON
Authentication: None (for assignment purposes)
Overview
This RESTful API allows developers to manage a collection of books in an online bookstore. The API supports standard CRUD operations: Create, Read, Update, and Delete.
Endpoints
1. GET /books
URL: /books
Method: GET
Response: 200 OK
Sample Response:
  {
    "id": 1,
    "title": "The Pragmatic Programmer",
    "author": "Andrew Hunt",
    "price": 42.99,
    "isbn": "978-0201616224"
  },
  {
    "id": 2,
    "title": "Clean Code",
    "author": "Robert C. Martin",
    "price": 37.50,
    "isbn": "978-0132350884"
  }

2. GET /books/{id}
URL: /books/{id}
Method: GET
Path Parameter:
id (integer) – Unique ID of the book
Response: 200 OK or 404 Not Found
Sample Response:
{
  "id": 1,
  "title": "The Pragmatic Programmer",
  "author": "Andrew Hunt",
  "price": 42.99,
  "isbn": "978-0201616224"
}
3. POST /books
URL: /books
Method: POST
Request Body Example:
Response: 201 Created
Sample Response:
{
  "title": "Refactoring",
  "author": "Martin Fowler",
  "price": 49.99,
  "isbn": "978-0201485677"
}
Response: 201 Created
{
  "message": "Book added successfully.",
  "id": 3
}
4. PUT /books/{id}
URL: /books/{id}
Method: PUT
Path Parameter:
id (integer) – ID of the book to update
Request Body Example:
{
  "title": "Refactoring (2nd Edition)",
  "author": "Martin Fowler",
  "price": 55.00,
  "isbn": "978-0134757599"
}
Response: 200 OK
Sample Response:
{
  "message": "Book updated successfully."
}
5. DELETE /books/{id}
URL: /books/{id}
Method: DELETE
Path Parameter:
id (integer) – ID of the book to delete
Response: 200 OK or 404 Not Found
Sample Response: 
{
  "message": "Book deleted successfully."
}
