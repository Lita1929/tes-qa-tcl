# Test Scenarios (Coverage)

| Endpoint       | Test Case                                    | Type      | Expected Result                    |
|----------------|----------------------------------------------|-----------|------------------------------------|
| GET /posts     | Memvalidasi daftar seluruh data              | Positive  | Status 200 & Response berupa Array |
| GET /posts/1   | Memvalidasi ID yang terdaftar                | Positive  | Status 200 & Data sesuai ID        |
| GET /posts/101 | Memvalidasi ID yang tidak terdaftar          | Negative  | Status 404 Not Found               |
| GET /posts/a   | Memvalidasi ID dengan karakter non-numerik   | Edge Case | Status 404 Not Found               |
| POST /posts    | Menyusun test data dengan data input lengkap | Positive  | Status 201 Created                 |
| POST /posts    | Menyusun test data dengan body kosong        | Negative  | Status 201 Created                 |
| POST /posts    | Menyusun test data dengan input tidak valid  | Negative  | Status 500 Internal Server Error   |
