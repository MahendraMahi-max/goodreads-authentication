Connecting SQLite Database from Node JS to get the books from Goodreads Website


Install the SQL third-party packages sqlite and sqlite3.
Initialize the SQLite Database


Node JS Third-party packages
 Nodemon
The Nodemon is a tool that restarts the server automatically whenever we make changes in the file.

Installation Command: npm install -g nodemon


GoodReads APIs
Get Book
Add Book
Update Book
Delete Book
Get Author Books


1. Get Book
We can use /books/:bookId/ as a path to identify a single book resource, where bookId is a path parameter.

For example,

In http://localhost:3000/books/1/, the bookId is 1.

 
JAVASCRIPT
Note
Any string can be used as a path parameter.
2. Add Book
To add a book to the Database, you need to send a request body in JSON format.

The express.json() is used to recognize the incoming request object as JSON Object and parses it.

The request.body is used to get the HTTP Request body.



3.Update Book
We can use /books/:bookId/ as a path to identify a single book resource, where :bookId is the path parameter.

For example, http://localhost:3000/books/1/.




Get Books API
Let's see how to add Filters to Get Books API

1.1 Filtering Books
Get a specific number of books
Get books based on search query text
Get books in the sorted order
1.1.1 Get a specific number of books
To get specific number of books in certain range we use limit and offset.

Offset is used to specify the position from where rows are to be selected.

Limit is used to specify the number of rows.
and many more...
Query parameters starts with ? (question mark) followed by key value pairs separated by & (ampersand)



1.1.2 Get books based on search query text
We provide query text to search_q key

1.1.3 Get books in the sorted order
We provide sorted order to order key

Ascending: ASC
DESCENDING: DESC

Filtering GET Books API
 


http://localhost:3000/books/?offset=2&limit=3 is same as http://localhost:3000/books?offset=2&limit=3

