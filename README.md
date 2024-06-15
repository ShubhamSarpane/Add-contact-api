---
# Add-contact-api

## Overview

The Add-contact-api is a Node.js application that provides a simple API for managing contacts. It uses MongoDB for data storage and supports both JSON responses. This Docker image packages the Add-contact-api and makes it easy to deploy the application in any environment that supports Docker.

## Features

- **RESTful API**: Provides endpoints to create, read, update, and delete contacts.
- **MongoDB Integration**: Uses MongoDB as the database to store contact information.
- **JSON Responses**: Supports both HTML and JSON responses based on the request headers.
- **Dockerized**: Easily deployable using Docker.
  
## Requirements

- Docker installed on your system
- (Optional) Docker Compose for managing multi-container applications
  
## Getting Started

### Clone the Repository

```sh
git clone https://github.com/your-username/Add-contact-api.git
cd Add-contact-api
```

### Using Postman for API Testing

1. **Open Postman**: Launch Postman.
   
2. **Perform CRUD Operations**

   - **Create a Contact**
   - **Use locathost:5000 to perform the API in Local Machine with PostMan**
     - **Endpoint:** `POST localhost:5000/api/contacts`
     - **Request Body (Form data - Key Value Pair):**
       ```
        {
         "name": "John Doe",
         "phoneNumbers": ["1234567890", "9876543210"],
         "imageUrl": Select file / "https://example.com/xyz.jpg",
       }
       ```
       
   - **Update a Contact**
     - **Endpoint:** `PUT localhost:5000/api/contacts/:id`
     - **Request Body (Form data - Key Value Pair):**
       ```
       {
         "name": "Updated Name",
         "phoneNumbers": ["9999999999"],
         "imageUrl": Select file / "https://example.com/xyz.jpg",
       }
       ```
       
   - **Fetch All Contacts**
     - **Endpoint:** `GET localhost:5000/api/contacts`
    
    - **Delete a Contact**
      - **Endpoint:** `DELETE localhost:5000/api/contacts/:id`
      
   - **Search Contacts by Name or Phone Number**
     - **Endpoint:** `GET localhost:5000/api/contacts/search?q=query`
     - Replace `query` with the name or phone number to search for.
       
   - **Export Contacts as CSV File**
     - **Endpoint:** `GET localhost:5000/api/contacts/export/csv`
     - Csv file will be saved inside the local machine.
      
3. **Verify Responses**: Check the response in Postman's "Response" section to ensure the operation was successful.



---
