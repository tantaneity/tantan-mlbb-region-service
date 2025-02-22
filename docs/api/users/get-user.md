# Get User Documentation

## Endpoint
```
GET /users/get_user
```

## Query Parameters
| Parameter    | Type | Required | Description        |
|-------------|------|----------|--------------------|
| telegram_id | int  | Yes      | User's Telegram ID |

## Response

### Success (200 OK)
```json
{
  "message": "User found successfully",
  "user": {
    "telegram_id": 123456789,
    "player_id": 987654321,
    "zone_id": 1,
    "region": "US"
  },
  "status": "SUCCESS"
}
```

### Errors
- **404 Not Found**: User not found
- **500 Internal Server Error**: Server error

## Example
```http
GET /users/get_user?telegram_id=123456789
```
