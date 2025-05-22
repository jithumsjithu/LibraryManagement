Java Version: 17
Spring boot :2.7.5
Maven
Packaging :jar
Using Postman

API -For getting details based on the request body
http://localhost:8089/api/v1/books/search
{
  "publicationYearFrom": 1970,
  "publicationYearTo": 1980
}

output
 {
        "id": 3,
        "isbn": "ISBN-0345539438",
        "title": "Cosmos",
        "genre": "SCIENCE",
        "publicationYear": 1980,
        "publisher": "Random House",
        "totalCopies": 2,
        "author": {
            "id": 1,
            "name": "Sagan",
            "biography": "BIO",
            "birthDate": "1998-11-24"
        }
    },
    {
        "id": 4,
        "isbn": "ISBN-0345539439",
        "title": "The End",
        "genre": "FICTION",
        "publicationYear": 1978,
        "publisher": "Willam Rocks",
        "totalCopies": 5,
        "author": {
            "id": 2,
            "name": "Steev",
            "biography": "ABC",
            "birthDate": "1999-05-04"
        }

API -For getting details based on the request body
http://localhost:8089/api/v1/books/search
{
  "isbn": "ISBN-0345539439"
}

output
 {
        "id": 4,
        "isbn": "ISBN-0345539439",
        "title": "The End",
        "genre": "FICTION",
        "publicationYear": 1978,
        "publisher": "Willam Rocks",
        "totalCopies": 5,
        "author": {
            "id": 2,
            "name": "Steev",
            "biography": "ABC",
            "birthDate": "1999-05-04"
        }
API- For based on book reserved
http://localhost:8089/api/v1/books/searchRes

output
{
        "bookId": 4,
        "isbn": "ISBN-0345539439",
        "title": "The End",
        "reservedMemberId": "MEM-AB1235",
        "authorId": 2,
        "authorName": "Steev",
        "authorBiography": "ABC",
        "authorBirthDate": "1999-05-04"
    }
