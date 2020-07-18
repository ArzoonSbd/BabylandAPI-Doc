# Update Current User

**URL** : `/api/user/`

**Method** : `PATCH`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

## Error Response

**Code** : `400 Bad Request`

**JSON representation**

```json
{
  "id": "integer",
  "first_name": "string",
  "last_name": "string",
  "date_joined": "string",
  "is_active": "boolean",
  "email": "string",
  "password": "string",
  "gender": "string",
  "phone": "string",
  "avatar": "string",
  "role": "integer",
  "last_login": "string"
}
```

**Content examples**

```json
{
  "id": 45,
  "first_name": "arjun",
  "last_name": "subedi",
  "date_joined": "2020-07-12T17:32:33.831257+02:00",
  "is_active": true,
  "email": "arjun.eversoft@gmail.com",
  "gender": "M",
  "phone": "9806633448",
  "avatar": "/media/admin/defaultAvatar.png",
  "role": 0,
  "last_login": "2020-07-13T18:43:55.024820+02:00"
}
```

**Parameters**
| Field | Type | Description |
| :---------- | :----: | ---------------: |
| id | string | user id |
| first_name (<= 30 characters) | string | user first name |
| last_name (<= 150 characters)| string | user last name |
| date_joined | string | user joined date |
| is_active (Default: true) | boolean | user status |
| email (required)| string | user email |
| password (required and >= 8 characters)| string | user email |
| gender (Enum: "M" "F" "O" "N")| string | user gender |
| phone (<= 15 characters)| string | user phone number |
| avatar | string | user image |
| role | integer | user role |
| last_login | string | user last login information |
