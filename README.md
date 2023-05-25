# CRUD API with Golang

The code provided is a simple implementation of a RESTful API for managing movie data. It uses the Go programming language and the Gorilla Mux package for routing HTTP requests.

The code defines two main structs: `Movie` and `Director`. The `Movie` struct represents a movie entity with properties such as ID, ISBN, Title, and Director. The `Director` struct contains the first name and last name of a movie director.

The code sets up various HTTP request handlers for different endpoints. Here's a summary of the endpoints and their corresponding actions:

- `GET /movies`: Retrieves a list of all movies.
- `GET /movies/{id}`: Retrieves a specific movie by its ID.
- `POST /movies`: Creates a new movie by reading the movie data from the request body.
- `PUT /movies/{id}`: Updates an existing movie with the provided ID by replacing it with the movie data from the request body.
- `DELETE /movies/{id}`: Deletes a movie with the provided ID.

The `main` function initializes a router from Gorilla Mux and registers the endpoints with their respective handler functions. It also initializes a slice of movies with some initial data.

Finally, the server is started on port 8000, and any incoming HTTP requests are handled by the router.

In summary, this code sets up a basic movie API with CRUD (Create, Read, Update, Delete) functionality, allowing users to interact with movie data through HTTP requests.

## Movie CRUD API

This is a simple implementation of a RESTful API for managing movie data using Go and the Gorilla Mux package. The API provides endpoints for basic CRUD (Create, Read, Update, Delete) operations on movie resources.

### Endpoints

- **GET /movies**: Retrieves a list of all movies.
- **GET /movies/{id}**: Retrieves a specific movie by its ID.
- **POST /movies**: Creates a new movie.
- **PUT /movies/{id}**: Updates an existing movie by its ID.
- **DELETE /movies/{id}**: Deletes a movie by its ID.

### Getting Started

To test the API endpoints, you can use a tool like Postman. Here's how you can test the API using Postman:

1. Launch Postman and create a new request.
2. Set the HTTP method to the desired action (GET, POST, PUT, DELETE).
3. Enter the appropriate URL based on the action you want to perform.
4. If required, add the request body in JSON format.
5. Set the request headers as needed.
6. Click the "Send" button to execute the request.
7. Review the response received from the API.

### Example JSON Request Body for Creating a Movie

```json
{
  "id": "3",
  "isbn": "67890",
  "title": "Movie Three",
  "director": {
    "firstname": "John",
    "lastname": "Doe"
  }
}
```

## Setting Up and Running the API

To run the API locally, follow these steps:

1. Clone the repository to your local machine.
2. Make sure you have Go installed.
3. Navigate to the project directory.
4. Run the command `go run main.go` to start the server.
5. The API will be accessible at `http://localhost:8000`.

Make sure to replace any placeholders such as `{id}` with the actual values when making requests to the API.

Feel free to explore and interact with the API endpoints to manage movie data.
