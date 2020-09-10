[Back](../README.md)

# Change Password

Only valid user and customer able to change password.

**URL** : `/api/user/password/`

**Method** : `PUT`

**Auth required** : YES

## Success Response

**Code** : `202 Accepted`

**Response**

```json
{
  "old_password": "test@12345",
  "new_password": "newpwd@12345"
}
```

## Error Response

**Code** : `404 Not Found`

**Reason** : `No user with the id found`

**Response** :

```json
{
  "detail": "Not found."
}
```

**Code** : `400 Bad Request`

**Reason** : `Password validation error`

**Response** :

```json
{
  "detail": "Old password does not match!"
}
```

**JSON representation of content**

```json
{
  "old_password": "string",
  "new_password": "string"
}
```

**Parameters**

| Field                     | Type   | Description       |
| ------------------------- | ------ | ----------------- |
| old_password `(required)` | string | user old password |
| new_password `(required)` | string | user new password |

[Back](../README.md)
