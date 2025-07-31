# Book-store

**Online Bookstore By using RESTful API Documentation**<br>
Version: 1.0<br>
Base URL: https://api.onlinebookstore.com/v1<br>
Format : JSON<br>
Authentication: None (for assignment purposes)<br>

**Overview**<br>
This RESTful API allows developers to manage a collection of books in an online bookstore. The API supports standard CRUD operations: Create, Read, Update, and Delete.<br>
Endpoints<br>

**1. GET /books**<br>

URL: /books<br>
Method: GET<br>
Response: 200 OK<br>
**Sample Response**<br>
<br>
{<br>
    "id": 1,<br>
    "title": "The Pragmatic Programmer",<br>
    "author": "Andrew Hunt",<br>
    "price": 42.99,<br>
    "isbn": "978-0201616224"<br>
  },<br>
  {<br>
    "id": 2,<br>
    "title": "Clean Code",<br>
    "author": "Robert C. Martin",<br>
    "price": 37.50,<br>
    "isbn": "978-0132350884"<br>
  }<br>

**2. GET /books/{id}**<br>

URL: /books/{id}<br>
Method: GET<br>
Path Parameter:<br>
id (integer) – Unique ID of the book<br>
Response: 200 OK or 404 Not Found<br>
**Sample Response**<br>
{<br>
  "id": 1,<br>
  "title": "The Pragmatic Programmer",<br>
  "author": "Andrew Hunt",<br>
  "price": 42.99,<br>
  "isbn": "978-0201616224"<br>
}<br>

**3. POST /books**<br>

URL: /books<br>
Method: POST<br>
Request Body Example:<br>
Response: 201 Created<br>
**Sample Response**<br>
{<br>
  "title": "Refactoring",<br>
  "author": "Martin Fowler",<br>
  "price": 49.99,<br>
  "isbn": "978-0201485677"<br>
}<br>
Response: 201 Created<br>
{<br>
  "message": "Book added successfully.",<br>
  "id": 3<br>
}<br>

**4. PUT /books/{id}**<br>

URL: /books/{id}<br>
Method: PUT<br>
Path Parameter:<br>
id (integer) – ID of the book to update<br>
Request Body Example:<br>
{<br>
  "title": "Refactoring (2nd Edition)",<br>
  "author": "Martin Fowler",<br>
  "price": 55.00,<br>
  "isbn": "978-0134757599"<br>
}<br>
Response: 200 OK<br>
Sample Response:<br>
{<br>
  "message": "Book updated successfully."<br>
}<br>

**5. DELETE /books/{id}**<br>

URL: /books/{id}<br>
Method: DELETE<br>
Path Parameter:<br>
id (integer) – ID of the book to delete<br>
Response: 200 OK or 404 Not Found<br>
**Sample Response**<br>
{<br>
  "message": "Book deleted successfully."<br>
}<br>
