# Gin JWT REST API Example

A simple REST API in Go using the Gin framework with JWT authentication middleware.

## Features
- User registration (`/register`)
- User login with JWT token (`/login`)
- Protected route (`/profile`) requiring JWT

## Getting Started

### Prerequisites
- Go 1.21 or newer

### Install dependencies
```
go mod tidy
```

### Run the server
```
go run main.go
```

### Endpoints
- `POST /register` — `{ "username": "user", "password": "pass" }`
- `POST /login` — `{ "username": "user", "password": "pass" }` → `{ "token": "..." }`
- `GET /profile` — Requires `Authorization: Bearer <token>` header

