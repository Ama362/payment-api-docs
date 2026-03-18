# Payment API

## Overview

The Payment API allows developers to integrate secure payment functionality into their applications without building everything from scratch.

With this API, you can:

- Create payment requests for customers
- Check the status of a transaction
- Retrieve payment details when needed

This API is designed to be simple and predictable, making it easy to integrate into web or mobile applications.

All requests are made over HTTPS and responses are returned in JSON format.

---

## Base URL

```
https://api.payment.com/v1
```

All API requests should be sent to this base URL.

---

## Response Format

All responses from the API follow a consistent JSON structure.

Example:

```json
{
  "status": "success",
  "data": {
    "transaction_id": "txn_123456",
    "amount": 5000,
    "currency": "NGN"
  }
}
```

If a request fails, the API will return an error message with a relevant status code.