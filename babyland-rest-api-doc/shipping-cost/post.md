[Back](../README.md)

# Create Shipping Cost

This API is used to create shipping cost by district and only customer token is valid.

**URL** : `/apps/my-shipping-cost/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Response** :

```json
{
  "shipping_cost": "500.0"
}
```

## Error Response

**Code** : `400 Bad Request`

**Reason** : `If district is not provided`

**Response** :

```json
{
  "detail": "Please provide district"
}
```

**Code** : `401 Unauthorized`

**Reason** : `No authentication token provided in header`

**Response** :

```json
{
  "detail": "Authentication credentials were not provided."
}
```

**JSON representation of content**

```json
{
  "district": "string"
}
```

**Content examples**

```json
{
  "district": "Kathmandu"
}
```

**Parameters**

| Field                 | Type   | Description                |
| --------------------- | ------ | -------------------------- |
| district `(required)` | string | district name from 77 list |

[Back](../README.md)
