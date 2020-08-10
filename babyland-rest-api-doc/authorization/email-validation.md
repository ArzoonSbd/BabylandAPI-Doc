[Back](../README.md)

# Token Blacklist

Used to validate user email address.

**URL** : `/api/user/activate/`

**Method** : `POST`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

## Error Response

**Condition** : If valid authentication is not provided.

**Code** : `400 Bad Request`

**Content** :

```json
{
  "detail": "Token and identifier are needed."
}
```

**JSON representation**

```json
{
  "token": "string",
  "identifier": "longint",
  "type": "short"
}
```

\*Data example\*\*

```json
{
  "token": "fb3c669bb0bb8580520a25cac35a0a7",
  "identifier": "2256",
  "type": "0"
}
```

**Parameters**
| Field | Type | Description |
| :---------- | :----: | ---------------: |
| token `(required and 10 to 50 characters)` | string | validate user token|
| identifier `(required)`| longint | validate userID|
| type `(required)`| 0 | type must be 0|

[Back](../README.md)
