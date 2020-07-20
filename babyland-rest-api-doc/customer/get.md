# Get Customer List

**URL** : `/api/customer/`

**Method** : `GET`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

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
    },
```

**Parameters**
| Field | Type | Description |
| :---------- | :----: | ---------------: |
| id | integer | customer id |
| first_name | string | customer first name |
| last_name | string | customer last name |
| date_joined | string | customer joined date |
| is_active | boolean | customer status |
| email | string | customer email |
| address | object | customer address |
| gender | string | customer gender |
| phone | string | customer phone number |
| avatar | string | customer image |
| last_login | string | customer last login information |
