# JSONPlaceholder API Testing

## Description

Demo project for testing the JSONPlaceholder API [here](JsonplaceholderApi_postman_collection.json)  
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


## The Cat API

## Description

Demo project for testing the The CatAPI  [here](TheCatAPI.postman_collection.json)

This project shows API testing with The Cat API, including both positive and negative scenarios to check expected behavior and how errors are handled. 

## Positive Tests

Positive tests validate successful CRUD operations and correct HTTP status codes.

This folder contains the following tests: 

- **GET images by limit:** Gets a specified number of images.
- **GET image by ID:** Gets a single image using a valid image ID.
- **GET breeds:** Gets the list of cat breeds.
- **GET breed by ID:** Gets information about a specific breed.
- **POST votes:** Submits a vote for an image (requires a valid API key).

Status codes for positive tests: 200 OK

## Negative Tests

Negative tests focus on invalid inputs, missing authentication, and unusual parameters to ensure proper error handling.

This folder contains the following tests: 

- **GET invalid image ID:** Checks that the API returns an error for non-existent image IDs.
- **GET invalid breed by ID:** Checks that the API returns an error for non-existent breed IDs.
- **GET images with invalid limit:** Tests what happens when an extremely high limit is provided. The API still returns 200 OK because it ignores unreasonable values and enforces an internal maximum. This test shows how the API handles extreme input values.
- **POST without API key:**  Ensures the API enforces authentication when posting votes.

Status codes: 
- 400 Bad Request
- 401 Unauthorized

