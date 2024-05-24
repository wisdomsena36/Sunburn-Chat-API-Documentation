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
