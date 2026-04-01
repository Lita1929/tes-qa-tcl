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
1. Import `postman_collection.json` ke Postman
2. Jalankan per request secara manual atau menggunakan Collection Runner

## Test Results Summary
| Endpoint       | Status | Result     |
|----------------|--------|------------|
| GET /posts     | 200 OK | PASS       |
| GET /posts/1   | 200 OK | PASS       |
| GET /posts/101 | 404    | PASS       |
| GET /posts/a   | 404    | PASS       |
| POST /posts    | 201    | PASS       |
| POST /posts    | 201    | PASS (Bug) |
| POST /posts    | 500    | PASS (Bug) |

## Approach
- Test: Meliputi Positive, Negative, dan Edge Cases.
- Validation: Memastikan kode status sesuai (200/201/404), struktur data benar, dan isinya akurat.
- Goal:Memastikan API tetap aman saat diberi input yang salah.

## Bugs & Issues
1. Validation Issue: POST dengan body kosong {} tetap menghasilkan 201 Created. Seharusnya 400 Bad Request.
2. Error Handling Issue: JSON yang strukturnya tidak sesuai menghasilkan 500 Internal Server Error. Seharusnya 400 Bad Request.

## Conclusion
- Hasil test: Semua tes di Postman LULUS (12/12 Pass). API secara fungsional bisa mengirim dan menerima data.
- Bug: API memiliki celah validasi, tetap menerima data kosong (status 201) dan gagal menangani invalid JSON dengan benar (status 500).
