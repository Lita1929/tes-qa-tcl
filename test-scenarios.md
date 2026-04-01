# Test Scenarios (Coverage)

| Endpoint       | Test Case                               | Type      | Expected Result                    |
|----------------|-----------------------------------------|-----------|------------------------------------|
| GET /posts     | Validasi daftar semua postingan         | Positive  | Status 200 & Response berupa Array |
| GET /posts/1   | Validasi ID yang terdaftar              | Positive  | Status 200 & Data sesuai ID        |
| GET /posts/101 | Validasi ID yang tidak terdaftar        | Negative  | Status 404 Not Found               |
| GET /posts/a   | Validasi ID dengan karakter non-numerik | Edge Case | Status 404 Not Found               |
| POST /posts    | Membuat data dengan data input lengkap  | Positive  | Status 201 Created & Return ID     |
| POST /posts    | Membuat data dengan body kosong         | Negative  | Status 400 Bad Request             |
| POST /posts    | Membuat data dengan format JSON rusak   | Negative  | Status 400 Bad Request             |
