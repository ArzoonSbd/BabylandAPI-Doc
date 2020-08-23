[Back](../README.md)

# Show User By ID

Get detail of a user with given id.

**URL** : `/api/user/{id}/`

**Method** : `GET`

**Auth required** : Yes

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 45,
  "first_name": "test",
  "last_name": "user",
  "date_joined": "2020-07-12T17:32:33.831257+02:00",
  "is_active": true,
  "email": "test.user@gmail.com",
  "gender": "M",
  "phone": "9806633448",
  "avatar": "/media/admin/defaultAvatar.png",
  "role": 0,
  "last_login": "2020-07-13T18:43:55.024820+02:00"
}
```

## Error Response

**Code** : `401 Unauthorized`

**Reason** : `No authentication token provided in header`

**Response** :

```json
{
  "detail": "Authentication credentials were not provided."
}
```

**Code** : `404 Not Found`

**JSON representation**

```json
{
  "detail": "Not found."
}
```

**Reason** : `given user ID doesn't exist.`

[Back](../README.md)
