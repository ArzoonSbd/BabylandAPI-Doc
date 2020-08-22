[Back](../README.md)

# Show User By ID

Get detail of a user with given id.

**URL** : `/api/user/{id}/`

**Method** : `GET`

**Auth required** : Yes

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

[Back](../README.md)
