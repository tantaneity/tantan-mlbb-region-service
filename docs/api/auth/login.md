# Login

## Endpoint
`GET /auth/login`

## Request Parameters
| Parameter     | Type   | Required | Description                  |
|--------------|--------|----------|------------------------------|
| `telegram_id`| int    | Yes      | Telegram ID of user         |
| `code`       | int    | Yes      | Verification code           |
| `player_id`  | int    | Yes      | Game player ID             |
| `zone_id`    | int    | Yes      | Player's zone ID           |

## Success Response (200 OK)
```json
{
  "message": "Logged in successfully.",
  "user": {
    "id": 1,
    "telegram_id": 123456789,
    "player_id": 987654321,
    "zone_id": 1,
    "region": "US",
    "added_at": "2023-01-01T00:00:00Z"
  },
  "status": "SUCCESS"
}
```

## Error Responses
- **400**: Invalid parameters
- **404**: User not found
- **500**: Internal server error

Each error returns:
```json
{
  "message": "Error description",
  "status": "ERROR"
}
```
