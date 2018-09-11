# GraphQL
GraphQL Demo 

To run this example either use Spring boot 1.5.8 or 1.5.9 

H2 Console URL  http://localhost:8080/h2-console/login.jsp  

JDBC URL: jdbc:h2:mem:testdb
User Name: sa
Password:


GraphQL Schema accessible using http://localhost:8080/graphql/schema.json

Steps to query using POSTMAN

POST  http://localhost:8080/graphql  using below Body content 

{
	"query":"{findAllBooks { id title } }"
}

GraphiQL is accessible using http://localhost:8080/graphiql

Queries for GraphiQL 


{
  findAllBooks {
    id
    isbn
    title
    pageCount
    author {
      firstName
      lastName
    }
  }
}


mutation {
  newBook(
    title: "Java: The Complete Reference, Tenth Edition",
    isbn: "1259589331",
    author: 1) {
      id title
  }
}



