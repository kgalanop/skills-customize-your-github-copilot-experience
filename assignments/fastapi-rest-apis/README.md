# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a RESTful API using FastAPI and Pydantic models. Students will create endpoints for managing items, validate incoming data, and run the app with Uvicorn.

## 📝 Tasks

### 🛠️ Set up the FastAPI application

#### Description
Create a basic FastAPI application with an instance of `FastAPI` and configure a root endpoint.

#### Requirements
Completed program should:

- Import `FastAPI` from `fastapi`.
- Create an app instance with `FastAPI()`.
- Implement a GET endpoint at `/` that returns a welcome message.
- Include a simple JSON response such as:
  ```json
  {"message": "Welcome to the FastAPI REST API!"}
  ```

### 🛠️ Create CRUD endpoints for item management

#### Description
Add endpoints to retrieve, create, update, and delete items using RESTful paths and methods.

#### Requirements
Completed program should:

- Define a Pydantic model named `Item` with `name`, `description`, `price`, and `in_stock` fields.
- Implement a GET endpoint at `/items/{item_id}` that returns the requested item.
- Implement a POST endpoint at `/items/` that accepts an `Item` payload and returns the created item.
- Implement a PUT endpoint at `/items/{item_id}` that updates the item data and returns the updated item.
- Implement a DELETE endpoint at `/items/{item_id}` that returns a confirmation message.

### 🛠️ Add validation and test the API

#### Description
Use Pydantic validation rules and run the API locally to verify the endpoints work.

#### Requirements
Completed program should:

- Ensure `name` is a non-empty string and `price` is a positive number.
- Return clear validation errors for invalid requests.
- Be runnable with Uvicorn using a command such as:
  ```bash
  uvicorn starter_code:app --reload
  ```
- Example request/response for creating an item:
  ```http
  POST /items/
  Content-Type: application/json

  {
    "name": "Notebook",
    "description": "A spiral notebook for notes.",
    "price": 5.99,
    "in_stock": true
  }
  ```
  ```json
  {
    "name": "Notebook",
    "description": "A spiral notebook for notes.",
    "price": 5.99,
    "in_stock": true
  }
  ```
