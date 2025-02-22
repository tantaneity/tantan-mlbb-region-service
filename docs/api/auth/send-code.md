# Send Code Documentation

## Request
```
GET /auth/send_code
```

### Parameters
| Parameter   | Type   | Required | Description                          |
|-------------|--------|----------|--------------------------------------|
| player_id   | int    | Yes      | Player ID |
| zone_id     | int    | Yes      | Zone ID |

### Example
```
GET /auth/send_code?player_id=12345&zone_id=67890
```

## Responses

### Success (200 OK)
```json
{
  "message": "Code sent successfully.",
  "status": "SUCCESS",
  "timeout": 60
}
```

### Error (400/500)
```json
{
  "message": "Failed to send code.",
  "status": "ERROR"
}
```
