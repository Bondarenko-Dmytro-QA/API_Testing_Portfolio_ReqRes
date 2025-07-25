# API Test Cases for JSONPlaceholder

This document provides examples of manual test cases for the JSONPlaceholder API.

---
### **ID:** API-TC-001
**Title:** Verify successful retrieval of a single post
**Priority:** High

**Request Details:**
*   **Method:** `GET`
*   **Endpoint:** `https://jsonplaceholder.typicode.com/posts/1`

**Expected Result:**
1.  **Status Code:** The response status code is `200 OK`.
2.  **Response Body:** The JSON body contains the data object for the post with `"id": 1`.
3.  **Headers:** The `Content-Type` header is `application/json; charset=utf-8`.

---
### **ID:** API-TC-002
**Title:** Verify successful creation of a new post with valid data
**Priority:** High

**Request Details:**
*   **Method:** `POST`
*   **Endpoint:** `https://jsonplaceholder.typicode.com/posts`
*   **Request Body:**
    ```json
    {
        "title": "My Test Post",
        "body": "This is a test from my QA portfolio.",
        "userId": 1
    }
    ```

**Expected Result:**
1.  **Status Code:** The response status code is `201 Created`.
2.  **Response Body:** The JSON body contains the `title` and `body` values that were sent in the request.
3.  **Response Body:** The response also contains a new unique `id` (e.g., `101`) generated by the server.
