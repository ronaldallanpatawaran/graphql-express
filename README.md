# POC GraphQL using mongodb

## System requirements
1. Nodejs version 12 and up

## Normal Installtion
1. `npm run install`
2. `node server.js`

## Docker Installation
1. `docker build -t poc/graphql-express`
2. `docker run -p 4000/4000 -d poc/graph-express`

## BOOKS

### GET ALL BOOKS

{
	books{
		id,
    name,
    pages,
    author {
			id,
      name,
      age
    }
  }
}

### ADD BOOK
mutation{
	addBook(name: "the little red riding hood", pages: 100, authorID: "5e3148cb5bfa932c48cb4530") {
		name,
    pages
  }
}

### GET BOOK BY ID
{
  book(id: "5e314d7636acdc5064579c6f"){
		id,
    name,
    pages
  }
}

## AUTHORS

### ADD AUTHOR
mutation{
	addAuthor(name: "ronald", age: 25){
	  name,
  	age
  }
}

### GET ALL AUTHORS
{
	authors {
    id,
		name,
    age,
    book {
			name,
      pages
    }
  }
}