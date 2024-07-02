# Sunburn Chat API Documentation

## Overview
The Sunburn Chat API allows developers to integrate conversational AI capabilities into their applications. It processes user input and returns a predefined response, facilitating simple interactions and automated replies.

## Base URL
`https://sunburnchatapi.onrender.com`

## Endpoints

### Chat Endpoint

#### Description
The Chat Endpoint processes a given prompt and returns a conversational reply.

#### URL
`https://sunburnchatapi.onrender.com/chat`

#### Method
`POST`

#### Request Headers
- `Content-Type: application/json`

#### Request Body
The request body should be a JSON object containing the `prompt` field.

##### Example Request Body
```json
{
    "prompt": "Hello"
}
```

#### Response
The response will be a JSON object containing the `reply` field with the corresponding reply to the given prompt.

##### Example Response
```json
{
    "reply": "Hello, how are you?"
}
```

#### Usage Example

##### Request
```sh
curl -X POST https://sunburnchatapi.onrender.com/chat \
    -H "Content-Type: application/json" \
    -d '{"prompt": "Hello"}'
```

##### Response
```json
{
    "reply": "Hello, how are you?"
}
```

Certainly! Here's a simplified version focusing solely on the API endpoint documentation for sending receipt emails using Flask:

---

## API Endpoint: `/send_receipt`

Sends a receipt email to the specified email address with the total purchase amount.

### Request

- **URL:** `/send_receipt`
- **Method:** POST
- **Request Body:**
  ```json
  {
      "email": "user@example.com",
      "total_amount": 60.00
  }
  ```
  - `email` (str, required): Recipient email address.
  - `total_amount` (float, required): Total amount of the purchase.

### Response

- **Success Response:**
  - Status Code: 200 OK
  - Content:
    ```json
    {
        "message": "Receipt email sent successfully"
    }
    ```

- **Error Response:**
  - Status Code: 500 Internal Server Error
  - Content:
    ```json
    {
        "error": "Error message"
    }
    ```

### Example

#### Example Request

```sh
curl -X POST http://localhost:5000/send_receipt \
-H "Content-Type: application/json" \
-d '{
    "email": "user@example.com",
    "total_amount": 60.00
}'
```

#### Example Response (Success)

```json
{
    "message": "Receipt email sent successfully"
}
```

#### Example Response (Error)

```json
{
    "error": "Failed to send email: SMTP Authentication Error"
}
```

## Error Handling
The API returns standard HTTP status codes to indicate the success or failure of an API request. Common status codes include:

- `200 OK`: The request was successful and the server returned the expected response.
- `400 Bad Request`: The request was malformed or contains invalid parameters.
- `500 Internal Server Error`: The server encountered an error processing the request.

## Notes
- Ensure that the `Content-Type` header is set to `application/json` when sending a request.
- The current implementation provides a static response for the given example prompt. Future updates may include more dynamic and context-aware responses.

## Contact
For further assistance, please contact support at [support@sunburnchatapi.com](mailto:support@sunburnchatapi.com).

---
