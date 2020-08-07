[Back](../README.md)

# Update Customer By ID

Change whole content of a category with given id

**URL** : `/api/customer/{id}/`

**Method** : `PUT`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

## Error Response

**Code** : `404 Not Found`

**Reason** : `No category with the id found`

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
  "address": {
    "name*": "string",
    "addressline": "string",
    "street*": "string",
    "city*": "string",
    "province*": "string",
    "phone": "string",
    "title": "Phone",
    "country": "string"
  },
  "password": "string",
  "gender": "string",
  "phone": "string",
  "avatar": "string",
  "last_login": "string"
}
```

**Content examples**

```json
{
  "id": 57,
  "first_name": "Saroj",
  "last_name": "Gurung",
  "date_joined": "2020-07-19T14:11:09.487710+02:00",
  "is_active": true,
  "email": "grg_prabhu@yahoo.com",
  "address": {
    "name": "Prabhu Gurung",
    "addressline": null,
    "street": "chhorepatan",
    "city": "Pokhara",
    "province": "Province 4 ( प्रदेश नं ४ )",
    "phone": "",
    "country": "India"
  },
  "gender": "M",
  "phone": "9846728507",
  "avatar": "http://dev.babylandworld.com/media/admin/defaultAvatar.png",
  "last_login": null
}
```

**Parameters**
| Field | Type | Description |
| ------------------------------------------------------- | ----------- | ---------------------- |
| first_name `(<= 30 characters)` | string | customer first name |
| last_name `(<= 150 characters)` | string | customer last name |
| date_joined `(read only and default date now)`| Date | customer joined date |
| is_active `(Default: true)` | boolean | customer status |
| email `(required and unique)`| string | customer email |
| address\*\* `(required)` | JSON object | customer address |
| gender `(Enum: "M" "F" "O" "N")`| string | customer gender |
| phone `(<= 15 characters and Nullable)` | string | customer phone number |

**Address Parameters**
| Field | Type | Description |
| ------------------------------------------------------- | ----------- | ---------------------- |
| name `(max 100 characters)` | string | customer address name |
| addressline `(max 100 characters and default Nullable)` | string | customer addressline|
| street `(max 255 characters)` | string | customer street name |
| city `(max 50 characters)` | string | customer city name |
| province `(max 50 characters)` | string | customer province name |
| phone `(<= 15 characters and Nullable)` | string | customer phone number |
| country `(max 50 characters and default value is Nepal)` | string | customer country name |

[Back](../README.md)
