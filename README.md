# 🛍️ Product API – Express.js CRUD Server

A RESTful API built with Express.js that supports full CRUD operations, middleware, and error handling.

---

## 🚀 How to Run the Server

1. **Install dependencies**  
   bash
   npm install //in bash//

2. **Start the server**

node server.js //in bash//

3. **Server will run at:**

http://localhost:3000
Make sure to include the header x-api-key: 12345 for protected routes.

**API Documentation**

 GET /api/products- Description: Get all products
- Query Parameters (optional):
- **category**: Filter by category
- **search**: Search by name
- **page**: Page number
- **limit**: Items per page 

 **POST /api/products- Description: Create a new product**
- Headers: x-api-key: 12345
- Body:

**JSON**
{
  "name": "Gaming Mouse",
  "description": "RGB mouse with 8 buttons",
  "price": 45,
  "category": "electronics",
  "inStock": true
}


**🔹 PUT /api/products/:id- Description: Update a product**
- Headers: x-api-key: 12345
- Body: Partial or full product object

**🔹 DELETE /api/products/:id- Description: Delete a product**
- Headers: x-api-key: 12345

**🔹 GET /api/products/stats/count-by-category**


## Example Requests & Responses :

**http**

POST /api/products
Headers:
  Content-Type: application/json
  x-api-key: 12345

Body:
{
  "name": "Mechanical Keyboard",
  "description": "Tactile keys with RGB lighting",
  "price": 89,
  "category": "electronics",
  "inStock": true
}


**Response:**

{
  "id": "4",
  "name": "Mechanical Keyboard",
  "description": "Tactile keys with RGB lighting",
  "price": 89,
  "category": "electronics",
  "inStock": true
}

**Unauthorized Request** 

POST /api/products
Headers:
  Content-Type: application/json

Body:
{ ... }

 **Response:**

{
  "error": "Unauthorized"
}

