# Authentication

To use the Payment API, you need to authenticate your requests using an API key.

This ensures that only authorized users can access the service.

---

## API Key

When you sign up, you will receive a secret API key.

Example:

```
sk_test_123456789
```

Keep this key secure. Do not expose it in public code or client-side applications.

---

## Sending Requests

Include your API key in the request header like this:

```
Authorization: Bearer sk_test_123456789
```

---

## Example Request

```bash
curl https://api.payment.com/v1/payments \
  -H "Authorization: Bearer sk_test_123456789"
```

---

## Important Notes

- Always keep your API key private
- Rotate your keys regularly for security
- Use test keys for development and live keys in production