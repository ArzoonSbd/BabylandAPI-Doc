[Back](../README.md)

# Token Blacklist

Used to create a refresh token for validate user.

**URL** : `/api/token/blacklist/`

**Method** : `POST`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

## Error Response

**Condition** : If valid authentication is not provided.

**Code** : `401 Unauthorized`

**Content** :

```json
{
  "detail": "Authentication credentials were not provided."
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
| Field | Type | Description |
| :---------- | :----: | ---------------: |
| refresh `(required)` | string | validate refresh token|

[Back](../README.md)
