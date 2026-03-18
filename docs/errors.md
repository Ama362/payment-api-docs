# Errors

The API uses standard HTTP status codes to indicate whether a request was successful or not.

---

## Common Error Codes

| Code | Meaning        | Description                          |
|-----|---------------|--------------------------------------|
| 400 | Bad Request   | The request is invalid or malformed  |
| 401 | Unauthorized  | API key is missing or invalid        |
| 404 | Not Found     | The requested resource does not exist|
| 500 | Server Error  | Something went wrong on the server   |

---

## Example Error Response

```json
{
  "status": "error",
  "message": "Invalid API key"
}
```

---

## Tips

- Always check the status code before processing the response
- Log errors for debugging
- Ensure all required fields are included in your request