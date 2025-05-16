# 📄 requirements.md

## ✅ 1. User Authentication

### API Endpoints

| Method | Endpoint             | Description                        |
|--------|----------------------|------------------------------------|
| POST   | `/api/auth/register` | Register new user (host or guest) |
| POST   | `/api/auth/login`    | Login with email & password        |
| GET    | `/api/auth/me`       | Get current authenticated user     |

### Input/Output Specifications

**POST /api/auth/register**

#### Input:
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "StrongPass123!",
  "role": "host" // or "guest"
}


Validation Rules

    Valid email format

    Password: min 8 characters, must include uppercase, lowercase, and number

    Email must be unique

Performance Criteria

    Response time: ≤ 500ms

    Rate limiting: 5 login attempts per minute per IP
