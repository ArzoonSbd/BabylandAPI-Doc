[Back](../README.md)

# Partial Update Customer By ID

Update the partial fields of customer with given id.

**URL** : `/api/customer/{id}/`

**Method** : `PATCH`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 3,
  "first_name": "Auto - 0oamaOM1",
  "last_name": "Auto - op0Ds2FD",
  "date_joined": "2020-08-22T15:34:36.027572+02:00",
  "is_active": true,
  "email": "customer@customer.com",
  "address": {
    "name": "Auto - mzMfjnm",
    "addressline": null,
    "street": "Randy Inlet",
    "city": "Mikelshire",
    "province": "4",
    "phone": null,
    "country": "Burkina Faso"
  },
  "gender": "M",
  "phone": null,
  "avatar": "http://dev.babylandworld.com/media/admin/defaultAvatar.png",
  "last_login": null,
  "dob": null,
  "email_verified": true
}
```

## Error Response

**Code** : `404 Not Found`

**Reason** : `No customer found`

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

**JSON representation of Content**

```json
{
  "first_name": "string",
  "last_name": "string",
  "email": "string",
  "address": {
    "name*": "string",
    "addressline": "string",
    "street*": "string",
    "city*": "string",
    "province*": "string",
    "phone": "string",
    "country": "string"
  },
  "password": "string",
  "gender": "string",
  "phone": "string"
}
```

**Content examples**

```json
{
  "first_name": "Auto - 0oamaOM1",
  "last_name": "Auto - op0Ds2FD",
  "email": "test@customer.com",
  "address": {
    "name": "Auto - mzMfjnm",
    "street": "Randy Inlet",
    "city": "Mikelshire",
    "province": "4",
    "country": "Burkina Faso"
  },
  "password": "tst@1234",
  "gender": "M"
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
| password `(required)` | string | customer password |
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
