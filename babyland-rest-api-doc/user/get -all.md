# Show All User

**URL** : `/api/user/all/`

**Method** : `GET`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

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
| first_name | string | user first name |
| last_name | string | user last name |
| date_joined | string | user joined date |
| is_active | boolean | user status |
| email | string | user email |
| gender | string | user gender |
| phone | string | user phone number |
| avatar | string | user image |
| role | integer | user role |
| last_login | string | user last login information |
