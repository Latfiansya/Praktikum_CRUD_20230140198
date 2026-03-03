# Laporan Praktikum 1 Deployment

> Nama  : Latfiansya Dzikri\
> NIM   : 20230140198\
> Kelas : D

| Keterangan | Screenshot |
| --- | --- |
| Hasil Running Web |<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/995a8bc9-7e9e-4656-8651-536d6d1d5dab" />|

# API Documentation

Base URL:

```
http://localhost:8080
```

---

# Create User

Endpoint :

```
POST /api/users
```

Request Header :

```
Content-Type : application/json
```

Request Body :

```json
{
  "name": "Budi Santoso",
  "age": 25
}
```

Response Body (Success) :

Status Code: **201 Created**

```json
{
  "data": {
    "age": 25,
    "id": "70997372-2da8-418a-8424-d9037531d41d",
    "name": "Budi Santoso"
  },
  "status": "success"
}
```

Response Body (Failed) :

```json
{
  "errors": "Validation error message"
}
```

cURL Example :

```bash
curl -X POST http://localhost:8080/api/users \
-H "Content-Type: application/json" \
-d "{\"name\":\"Budi Santoso\",\"age\":25}"
```

---

# Get All Users

Endpoint :

```
GET /api/users
```

Request Header :

```
-
```

Request Body :

```
-
```

Response Body (Success) :

Status Code: **200 OK**

```json
{
  "data": [
    {
      "age": 27,
      "id": "2c0ed7f4-58af-40a6-bb39-eeb3f3104704",
      "name": "Budi Speed"
    },
    {
      "age": 25,
      "id": "70997372-2da8-418a-8424-d9037531d41d",
      "name": "Budi Santoso"
    }
  ],
  "status": "success"
}
```

Response Body (Failed) :

```json
{
  "errors": "Data not found"
}
```

cURL Example :

```bash
curl -X GET http://localhost:8080/api/users
```

---

# Get User By ID

Endpoint :

```
GET /api/users/{id}
```

Request Header :

```
-
```

Request Body :

```
-
```

Response Body (Success) :

Status Code: **200 OK**

```json
{
  "data": {
    "age": 25,
    "id": "70997372-2da8-418a-8424-d9037531d41d",
    "name": "Budi Santoso"
  },
  "status": "success"
}
```

Response Body (Failed) :

```json
{
  "errors": "User not found"
}
```

cURL Example :

```bash
curl -X GET http://localhost:8080/api/users/<ID_USER>
```

---

# Update User

Endpoint :

```
PUT /api/users/{id}
```

Request Header :

```
Content-Type : application/json
```

Request Body :

```json
{
  "name": "Budi Santoso Updated",
  "age": 26
}
```

Response Body (Success) :

Status Code: **200 OK**

```json
{
  "data": {
    "age": 26,
    "id": "2c0ed7f4-58af-40a6-bb39-eeb3f3104704",
    "name": "Budi Santoso Updated"
  },
  "status": "success"
}
```

Response Body (Failed) :

```json
{
  "errors": "User not found or validation failed"
}
```

cURL Example :

```bash
curl -X PUT http://localhost:8080/api/users/<ID_USER> \
-H "Content-Type: application/json" \
-d "{\"name\":\"Budi Santoso Updated\",\"age\":26}"
```

---

# Delete User

Endpoint :

```
DELETE /api/users/{id}
```

Request Header :

```
-
```

Request Body :

```
-
```

Response Body (Success) :

Status Code: **200 OK**

```json
{
  "status": "success delete user with id 67b3eb25-3577-49ca-b7ef-fb7bae63ec82"
}
```

Response Body (Failed) :

```json
{
  "errors": "User not found"
}
```

cURL Example :

```bash
curl -X DELETE http://localhost:8080/api/users/<ID_USER>
```

---
