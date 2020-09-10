[Back](../README.md)

# Refresh Token

Used to create a refresh token for registered user.

**URL** : `/api/token/refresh/`

**Method** : `POST`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

## Error Response

**Condition** : If previous refresh token is not provided.

**Code** : `400 Bad Request`

**Content** :

```json
{
  "refresh": ["This field is required."]
}
```

**JSON representation**

```json
{
  "refresh": "string"
}
```

**Data example**

```json
{
  "refresh": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTYwNTcwODQyNCwianRpIjoiMDRlNzNmZjRiM2I1NDUyMWEwOWRkZGY1YzczNTY0OGQiLCJ1c2VyX2lkIjo5NX0.l6-AeMT0tKFB_sPcpp2hVRLWROYw98c16htIpw6mG2s"
}
```

**Parameters**

| Field                |  Type  |            Description |
| :------------------- | :----: | ---------------------: |
| refresh `(required)` | string | validate refresh token |

[Back](../README.md)
