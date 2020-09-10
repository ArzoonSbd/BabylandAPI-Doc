[Back](../README.md)

# Reset password

Used to reset the user/customer password through token.

**URL** : `/api/user/reset/`

**Method** : `POST`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

**Content** :

```json
{
  "detail": "Password changed"
}
```

## Error Response

**Condition** : If required fields arenot provided.

**Code** : `404 Not found`

**Content** :

```json
{
  "detail": "Token and identifier are needed."
}
```

**Condition** : If token is expired.

**Code** : `400 Bad Request`

**Content** :

```json
{
  "detail": "Token expires."
}
```

**Condition** : If new password doesn't satisfy minimum requirement.

**Code** : `400 Bad Request`

**Content** :

```json
{
  "detail": "Password must be at least 8 characters long."
}
```

**JSON representation**

```json
{
  "token": "string",
  "identifier": "longint",
  "type": "short",
  "new_password": "string"
}
```

**Data example**

```json
{
  "token": "fb3c669bb0bb8580520a25cac35a0a7",
  "identifier": "2256",
  "type": "1",
  "new_password": "newPass12@"
}
```

**Parameters**

| Field                                                                         |  Type   |         Description |
| :---------------------------------------------------------------------------- | :-----: | ------------------: |
| token `(required and 10 to 50 characters)`                                    | string  | validate user token |
| identifier `(required)`                                                       | longint |     validate userID |
| type `(required)`                                                             |    1    |     value must be 1 |
| new_password `(required and at least 8 characters with 1 digit and 1 number)` | string  |  valid new password |

[Back](../README.md)
