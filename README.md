# 🔐 Secure REST API with JWT Authentication in Go

This project demonstrates a simple yet secure RESTful API using **Go** and the **Gin** framework, implementing **JWT-based authentication** to protect private endpoints. It’s perfect for learning how to handle user authentication, middleware, and route protection in Go.

---

## 📌 Features

- User registration and login
- JWT-based token generation and validation
- Middleware for protected routes
- Simple, clean, and easy-to-understand structure
- No database or Docker — fully local and lightweight

---

## 🧱 Project Structure

```

.
├── main.go        # Main application
├── go.mod         # Go module file
└── README.md      # Project documentation

````

---

## ⚙️ Technology Stack

- **Go (Golang)**
- **Gin** — HTTP web framework
- **JWT (github.com/golang-jwt/jwt/v5)** — for token handling

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/secure-rest-api-go-jwt.git
cd secure-rest-api-go-jwt
````

### 2. Install dependencies

```bash
go mod tidy
```

### 3. Run the server

```bash
go run main.go
```

The server will start at: `http://localhost:8888`

---

## 📮 API Endpoints

### ➕ Register a new user

```http
POST /register
Content-Type: application/json

{
  "username": "testuser",
  "password": "testpass"
}
```

### 🔐 Login

```http
POST /login
Content-Type: application/json

{
  "username": "testuser",
  "password": "testpass"
}
```

**Response:**

```json
{
  "token": "<your-jwt-token>"
}
```

### 👤 Get Profile (Protected)

```http
GET /profile
Authorization: Bearer <your-jwt-token>
```

---

## 🔒 Security Notes

* ⚠️ Passwords are stored in-memory and in plain text (for learning only).
* 🔐 Use hashed passwords (e.g., bcrypt) in production.
* 🤫 Keep JWT secret keys in environment variables.
* ⏳ Tokens are set to expire in 1 hour.

---

## 📚 References

* [Gin Web Framework](https://gin-gonic.com/)
* [Go Programming Language](https://golang.org/)
* [JSON Web Tokens (JWT)](https://jwt.io/)

---

## 📃 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Umair Ahmed** – BS Artificial Intelligence Student

---

## ⭐ Like this project?

Give it a ⭐ on GitHub or share it with your fellow Go developers!
