# Book-store

**Online Bookstore RESTful API Documentation**<br>
Version: 1.0<br>
Base URL: https://api.onlinebookstore.com/v1<br>
Format: JSON<br>
Authentication: None (for assignment purposes)<br>
Overview<br>
This RESTful API allows developers to manage a collection of books in an online bookstore. The API supports standard CRUD operations: Create, Read, Update, and Delete.<br>
Endpoints<br>
**1. GET /books**<br>
URL: /books<br>
Method: GET<br>
Response: 200 OK<br>
**Sample Response**<br>
<sub><br>
{<br>
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
  }</sub>

**2. GET /books/{id}**
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
