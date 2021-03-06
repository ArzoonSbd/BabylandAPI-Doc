[Back](../README.md)

# Token Validation

Used to validate the token provided for given purpose and given user.

**URL** : `/api/token/valid/`

**Method** : `POST`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

**Content** :

```json
{
  "detail": "valid"
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

**JSON representation**

```json
{
  "token": "string",
  "identifier": "longint",
  "type": "short"
}
```

**Data example**

```json
{
  "token": "fb3c669bb0bb8580520a25cac35a0a7",
  "identifier": "2256",
  "type": "0"
}
```

**Parameters**

| Field                                      |   Type    |                                                        Description |
| :----------------------------------------- | :-------: | -----------------------------------------------------------------: |
| token `(required and 10 to 50 characters)` |  string   |                                                validate user token |
| identifier`(required)`                     |  longint  |                                                    validate userID |
| type `(required)`                          | ENUM[0,1] | where 0 is Email_Verification_Token and 1 is Forget_Password_Token |

[Back](../README.md)
