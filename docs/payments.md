# Payments

This section explains how to create and retrieve payments using the API.

---

## Create Payment

Creates a new payment request.

### Endpoint

```
POST /payments
```

### Description

This endpoint allows you to initiate a payment. It returns a payment link that you can share with your customer.

---

### Request Body

| Field     | Type    | Required | Description                     |
|----------|--------|----------|---------------------------------|
| amount   | integer | Yes      | Payment amount in kobo          |
| currency | string  | Yes      | Currency code (e.g., NGN)       |
| email    | string  | Yes      | Customer email address          |
| reference| string  | No       | Unique payment reference        |

---

### Example Request

```json
{
  "amount": 5000,
  "currency": "NGN",
  "email": "customer@email.com"
}
```

---

### Example Response

```json
{
  "status": "success",
  "data": {
    "id": "txn_123456",
    "payment_url": "https://pay.payment.com/123456",
    "status": "pending"
  }
}
```

---

## Get Payment

Retrieves the details of a specific payment.

### Endpoint

```
GET /payments/{id}
```

---

### Path Parameter

| Parameter | Description              |
|----------|--------------------------|
| id       | The payment ID           |

---

### Example Request

```bash
curl https://api.payment.com/v1/payments/txn_123456 \
  -H "Authorization: Bearer sk_test_123456789"
```

---

### Example Response

```json
{
  "status": "success",
  "data": {
    "id": "txn_123456",
    "amount": 5000,
    "currency": "NGN",
    "status": "success"
  }
}
```