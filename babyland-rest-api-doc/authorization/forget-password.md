[Back](../README.md)

# Forget Password

Used to send forget password to a email of existing user/customer. Mail is only sent if there is no old valid token of forget password for the user. Token is valid for 24 hours.

**URL** : `/api/user/forget/`

**Method** : `POST`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

**Content** :

```json
{
  "detail": "Email sent"
}
```

## Error Response

**Condition** : If required fields arenot provided.

**Code** : `404 Not found`

**Content** :

```json
{
  "detail": "Email address needed."
}
```
**Condition** : If token is already sent.

**Code** : `400 Bad Request`

**Content** :

```json
{
  "detail": "Token already generated in last 24 hours. Please check your email."
}
```

**Condition** : If user isnot found.

**Code** : `400 Bad Request`

**Content** :

```json
{
  "detail": "User not found"
}
```

**JSON representation**

```json
{
  "email": "email",
}
```

**Data example**

```json
{
  "email": "example@example.com"
}
```

**Parameters**
| Field | Type | Description |
| :---------- | :----: | ---------------: |
| example `(required)` | email | email of the user/customer|

[Back](../README.md)
