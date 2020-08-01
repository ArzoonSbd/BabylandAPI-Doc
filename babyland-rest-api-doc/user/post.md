# Create User

To create a user.

**URL** : `/api/user/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

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
        "Ensure this field has no more than 100 characters."
    ]
}
```

**JSON representation**

```json
{
  "id": "integer",
  "first_name": "string",
  "last_name": "string",
  "date_joined": "string",
  "is_active": "boolean",
  "email": "string",
  "password": "string",
  "gender": "string",
  "phone": "string",
  "avatar": "string",
  "role": "integer",
  "last_login": "string"
}
```

**Content examples**

```json
{
  "id": 45,
  "first_name": "arjun",
  "last_name": "subedi",
  "date_joined": "2020-07-12T17:32:33.831257+02:00",
  "is_active": true,
  "email": "arjun.eversoft@gmail.com",
  "gender": "M",
  "phone": "9806633448",
  "avatar": "/media/admin/defaultAvatar.png",
  "role": 0,
  "last_login": "2020-07-13T18:43:55.024820+02:00"
}
```

**Parameters**
| Field | Type | Description |
| :---------- | :----: | ---------------: |
| first_name `(<= 30 characters)` | string | user first name |
| last_name `(<= 150 characters)`| string | user last name |
| date_joined | string | user joined date |
| is_active `(Default: true)` | boolean | user status |
| email `(required)`| string | user email |
| gender `(Enum: "M" "F" "O" "N")`| string | user gender |
| phone `(<= 15 characters)`| string | user phone number |
| role `(-2147483648 .. 2147483647)`| integer | user role |

[Back](../README.md)
