[Back](../README.md)

# Get Customer List

Get details of current customer.

**URL** : `/api/customer/`

**Method** : `GET`

**Auth required** : Yes

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
    },
```

## Error Response

**Code** : `401 Unauthorized`

**Reason** : `No authentication token provided in header`

**Response** :

```json
{
  "detail": "Authentication credentials were not provided."
}
```

[Back](../README.md)
