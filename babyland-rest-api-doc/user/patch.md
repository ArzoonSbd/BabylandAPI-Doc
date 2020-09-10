[Back](../README.md)

# Update Current User

Update the partial fields of user.

**URL** : `/api/user/`

**Method** : `PATCH`

**Auth required** : YES

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

**Code** : `404 Not Found`

**Reason** : `No user with the id found`

**Response** :

```json
{
  "detail": "Not found."
}
```

**Code** : `400 Bad Request`

**Reason** : `Field validation error`

**Response** :

```json
{
    "<fieldname>": "[<Validation Error>]"
}

Example :

{
    "name": [
        "Ensure this field has no more than 150 characters."
    ]
}
```

**JSON representation of content**

```json
{
  "first_name": "string",
  "last_name": "string",
  "email": "string",
  "phone": "string"
}
```

**Content examples**

```json
{
  "first_name": "test",
  "last_name": "user",
  "phone": "9806633448"
}
```

**Parameters**

| Field                                     | Type    | Description                        |
| ----------------------------------------- | ------- | ---------------------------------- |
| first_name `(<= 30 characters)`           | string  | user first name                    |
| last_name `(<= 150 characters)`           | string  | user last name                     |
| date_joined `(read only and default now)` | string  | user joined date                   |
| is_active `(Default: true)`               | boolean | user status                        |
| email `(required and unique)`             | string  | user email                         |
| gender `(Enum: "M" "F" "O" "N")`          | string  | user gender(O: Others, N: No Info) |
| phone `(<= 15 characters)`                | string  | user phone number                  |
| role `(Enum:"0" "1")`                     | integer | user role (0: Admin, 1: Staff)     |

[Back](../README.md)
