# QA TEST

API tested:
https://jsonplaceholder.typicode.com

Endpoints:
- GET /posts
- GET /posts/{id}
- POST /posts

## Tools Used
- Postman

## How to Run

1. Import `postman_collection.json` into Postman
2. Run each request manually or using Collection Runner

## 🧪 Test Coverage

### 1. GET /posts
- Validate status code (200)
- Validate response is array
- Validate response structure

### 2. GET /posts/{id}
- Valid ID → returns correct data
- Invalid ID → returns error
- Non-numeric ID → returns 404

### 3. POST /posts
- Valid data → returns 201
- Missing field → should fail
- Empty field → should fail
- Invalid JSON → should fail

---

## 📊 Test Results Summary

| Endpoint | Result |
|--------|--------|
| GET /posts | PASS |
| GET /posts/1 | PASS |
| GET /posts/101 | PASS |
| GET /posts/a | PASS |
| POST valid | PASS |
| POST empty body | PASS (with note) |
| POST missing field | FAIL |
| POST invalid JSON | FAIL |

---
