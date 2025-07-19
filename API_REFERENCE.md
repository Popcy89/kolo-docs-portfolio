# 🧾 KOLO API Reference

> These APIs simulate how KOLO's backend communicates with the mobile app.

## 🔐 Authentication

All endpoints require a Bearer token:

```
Authorization: Bearer YOUR_API_KEY
```

### 🔹 `POST /api/v1/users/signup`

**Create a new user**

```json
Request:
{
  "phone": "08034567890",
  "bvn": "22345678901"
}

Response:
{
  "user_id": "user_abc123",
  "otp_sent": true
}
```

### 🔹 `POST /api/v1/cards/link`

**Link user debit card**

```json
Request:
{
  "user_id": "user_abc123",
  "card_number": "**** **** **** 1234",
  "expiry": "12/26",
  "cvv": "123"
}

Response:
{
  "status": "linked",
  "daily_debit_set": false
}
```

### 🔹 `POST /api/v1/savings/start`

**Activate daily debit**

```json
Request:
{
  "user_id": "user_abc123",
  "daily_amount": 100
}

Response:
{
  "status": "active",
  "next_debit_date": "2025-06-12"
}
```

### 🔹 `GET /api/v1/savings/summary`

**Get savings balance and history**

```json
Response:
{
  "total_saved": 11500,
  "debits": [
    {"date": "2025-06-10", "amount": 100},
    {"date": "2025-06-09", "amount": 100}
  ]
}
```
