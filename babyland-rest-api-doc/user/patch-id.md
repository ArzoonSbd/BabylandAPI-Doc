[Back](../README.md)

# Patch User By ID

Update the partial fields of user by id.

**URL** : `/api/user/{id}/`

**Method** : `PATCH`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

## Error Response

**Code** : `404 Not Found`

**Reason** : `No user found`

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
| ------------------------------------------------------- | ----------- | ---------------------- |
| first_name `(<= 30 characters)` | string | user first name |
| last_name `(<= 150 characters)`| string | user last name |
| date_joined `(read only and default now)`| string | user joined date |
| is_active `(Default: true)` | boolean | user status |
| email `(required and unique)`| string | user email |
| gender `(Enum: "M" "F" "O" "N")`| string | user gender(O: Others, N: No Info) |
| phone `(<= 15 characters)`| string | user phone number |
| role `(Enum:"0" "1")` | integer | user role (0: Admin, 1: Staff)|

[Back](../README.md)
