# JSONPlaceholder API Testing – Posts

## Description

Demo project for testing the JSONPlaceholder API (https://jsonplaceholder.typicode.com/).  
This project covers **all CRUD methods** (GET, POST, PUT, DELETE) and includes both **positive** and **negative tests**.

## Endpoints Used

- **GET /posts** – list all posts  
- **GET /posts/{id}** – retrieve a specific post  
- **POST /posts** – create a new post  
- **PUT /posts/{id}** – update an existing post  
- **DELETE /posts/{id}** – delete a post  


## Postman Collection Structure

- Folder `Positive`

In the Positive folder, I included requests for successful CRUD operations that will return 200 OK or 201 created statuses. 
They demonstrate how the API should behave when provided with valid data.”
  - GET: List Posts, Single Post  
  - POST: Create valid post  
  - PUT: Update existing post  
  - DELETE: Delete existing post  

- Folder `Negative`

In the Negative folder, I tested invalid inputs and non-existent IDs that will return 400 Bad Request or 404 Not Found statuses. These requests simulate how the API should respond when provided with incorrect data or IDs that do not exist.

  - GET: Non-existent ID  
  - POST: Invalid or incomplete body  
  - PUT: Update non-existent post or invalid data  
  - DELETE: Delete non-existent post  

## Instructions

1. Open Postman.  
2. Import the collection from the JSON file: `JSONPlaceholder_Posts_Collection.json`.  
3. Run the requests in the desired order for positive or negative tests.  

## Notes
- JSONPlaceholder is a demo API → data is not persistent.  
- Simulated status codes:  
  - `200 OK` → successful GET/PUT/DELETE  
  - `201 Created` → successful POST  
  - Negative tests simulate errors or non-existent IDs  