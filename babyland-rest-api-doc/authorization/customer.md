[Back](../README.md)

# Obtain Token

Used to create a token for registered customer. This can be called for customer login purpose.

**URL** : `/api/customer/token/obtain/`

**Method** : `POST`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

## Error Response

**Condition** : If 'username' and 'password' combination is wrong.

**Code** : `401 Unauthorized`

**Content** :

```json
{
  "detail": "No active account found with the given credentials"
}
```

**JSON representation**

```json
{
  "username": "string",
  "password": "string"
}
```

**Data example**

```json
{
  "username": "arjun.eversoft@gmail.com",
  "password": "admin12345"
}
```

**Content example**

```json
{
  "access": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNTk5MTQ2NjUyLCJqdGkiOiIyMDhmODhhODYwOGU0YjJhYTNhZmViNGI4ZmY4MzFjMSIsInVzZXJfaWQiOjF9.yf2U89GNZoU-9drIwLCYD0uMmxIcrxdMYQrIhU1dNs8",
  "refresh": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTYwMzQ2NjY1MiwianRpIjoiMjQzOWYwYWEzODMwNGU5MmE5NDhmZTJjNjYyYWU4MTQiLCJ1c2VyX2lkIjoxfQ.GIu3mCkRtmYfratr1eoTglwxpZhWwPoqjc3NE3NnZOI"
}
```

**Parameters**

| Field                 |  Type  |   Description |
| :-------------------- | :----: | ------------: |
| email `(required)`    | string |    user email |
| password `(required)` | string | user password |

[Back](../README.md)
